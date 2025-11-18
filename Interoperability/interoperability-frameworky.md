# Appendix to Hierarchical Taxonomy

---

## Diagnostic Framework

### Step 1: Identify the Layer

Use these diagnostic questions:

| Question | Layer | Action |
|----------|-------|--------|
| Can System B parse messages from System A? | Interface | Check 1.X categories |
| Do messages physically arrive at System B? | Transport | Check 2.X categories |
| Can System B process messages fast enough? | Processing | Check 3.X categories |

### Step 2: Narrow to Category (1.X, 2.X, 3.X)

**Interface Layer (1.X)**:
- Schema mismatches → 1.1
- Protocol incompatibility → 1.2
- API contract violations → 1.3
- Data type conflicts → 1.4

**Transport Layer (2.X)**:
- Message too large → 2.1
- Network problems → 2.2
- Too many requests → 2.3

**Processing Layer (3.X)**:
- System overloaded → 3.1
- Timing issues → 3.2
- Need to slow down → 3.3

### Step 3: Identify Constraint Type (1.X.Y)

Navigate to the specific category and identify which constraint type is violated.

### Step 4: Pinpoint Source Constraint (1.X.Y.Z)

Find the exact atomic constraint causing the failure.

---

## Constraint Mapping Template

Use this template to map constraints between two systems:

```
Integration: [System A] ↔ [System B]
Date: [YYYY-MM-DD]
Owner: [Name]

┌─────────────────────────────────────────────────────────────────┐
│ INTERFACE LAYER (1.X)                                           │
├─────────────────────────────────────────────────────────────────┤
│ 1.1 Schema Compliance                                           │
│   1.1.1 Field Types                                             │
│     System A: JSON with string dates                            │
│     System B: Requires Unix timestamp integers                  │
│     Status: ✗ MISMATCH                                          │
│     Solution: Add transformer (1.4.3.2)                         │
│                                                                 │
│ 1.2 Protocol Compatibility                                      │
│   1.2.1 HTTP-Based Protocols                                    │
│     Both: REST over HTTPS                                       │
│     Status: ✓ COMPATIBLE                                        │
│                                                                 │
│ 1.3 Interface Contracts                                         │
│   1.3.1 Versioning                                              │
│     System A: /v1/                                              │
│     System B: /v2/ (v1 deprecated)                              │
│     Status: ✗ MISMATCH                                          │
│     Solution: Update System A to v2                             │
│                                                                 │
│ 1.4 Data Typing Alignment                                       │
│     Covered by 1.1.1 above                                      │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│ TRANSPORT LAYER (2.X)                                           │
├─────────────────────────────────────────────────────────────────┤
│ 2.1 Payload Size Constraints                                    │
│   2.1.1 HTTP Request Limits                                     │
│     System A: Sends up to 50MB                                  │
│     System B: Max 10MB (nginx limit)                            │
│     Status: ✗ MISMATCH (5x oversized)                           │
│     Solution: Implement chunking (2.1.3) or compression (2.1.5) │
│                                                                 │
│ 2.2 Bandwidth Limits                                            │
│   2.2.2 Latency                                                 │
│     Cross-region: ~150ms RTT                                    │
│     Requirement: <100ms for real-time                           │
│     Status: ✗ EXCEEDS (1.5x too slow)                           │
│     Solution: Regional caching or async processing              │
│                                                                 │
│ 2.3 Rate Limiting                                               │
│   2.3.1 Request Rate Limits                                     │
│     System A: Sends 1000 req/s                                  │
│     System B: Limits to 100 req/s                               │
│     Status: ✗ MISMATCH (10x over limit)                         │
│     Solution: Implement queuing + backoff (2.3.4)               │
└─────────────────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────────────────┐
│ PROCESSING LAYER (3.X)                                          │
├─────────────────────────────────────────────────────────────────┤
│ 3.1 Computational Overhead                                      │
│   3.1.3 Schema Validation Cost                                  │
│     Validation time: 500ms per message                          │
│     Requirement: <100ms per message                             │
│     Status: ✗ EXCEEDS (5x too slow)                             │
│     Solution: Simplify schema or move to async (3.2)            │
│                                                                 │
│ 3.2 Processing Windows                                          │
│   3.2.4 SLA Timing                                              │
│     Current: Hourly batch (3600s)                               │
│     Requirement: 5-minute SLA (300s)                            │
│     Status: ✗ MISMATCH (12x too slow)                           │
│     Solution: Switch to micro-batch (3.2.2)                     │
│                                                                 │
│ 3.3 Throttling                                                  │
│   3.3.4 Circuit Breakers                                        │
│     System B: Opens at 10k queue depth                          │
│     System A: No backpressure handling                          │
│     Status: ✗ NOT CONFIGURED                                    │
│     Solution: Implement backpressure listener (3.3.3)           │
└─────────────────────────────────────────────────────────────────┘

SUMMARY:
- Total Constraints Checked: 12
- Compatible: 2
- Mismatches: 10
- Critical Blockers: 4 (1.1.1, 2.1.1, 2.3.1, 3.1.3)
- Priority: Fix Interface layer first, then Transport
```

---

## Cross-Layer Interaction Matrix

Understanding how constraints in one layer affect others:

### Interface → Transport

| Interface Constraint | Transport Impact | Constraint Path |
|---------------------|------------------|-----------------|
| Large nested schemas (1.1.3.2) | Increases payload size | → 2.1.1.1 |
| Complex validation rules (1.1.4) | Increases validation time | → 3.1.3 |
| JSON vs Protocol Buffers (1.2) | Affects bandwidth usage | → 2.2.1 |
| Many optional fields (1.1.2.2) | Variable payload size | → 2.1 |

### Transport → Processing

| Transport Constraint | Processing Impact | Constraint Path |
|---------------------|-------------------|-----------------|
| Rate limiting (2.3.1) | Creates processing queues | → 3.3.2 |
| High latency (2.2.2) | Triggers timeouts and retries | → 3.2.4 |
| Large payloads (2.1) | Increases decompression cost | → 3.1.4 |
| Network unreliability (2.2.5) | Requires retry logic | → 2.3.4 → 3.1 |

### Processing → Interface

| Processing Constraint | Interface Impact | Constraint Path |
|----------------------|------------------|-----------------|
| Slow validation (3.1.3) | May require simpler schemas | → 1.1 |
| Processing delays (3.2) | May need versioning for gradual rollout | → 1.3.1 |
| High CPU cost (3.1.1) | May force protocol change | → 1.2 |

### Bidirectional Dependencies

| Constraint A | Constraint B | Interaction |
|-------------|-------------|-------------|
| Backpressure (3.3.3) | Rate limiting (2.3) | Processing slowdown triggers transport throttling |
| Schema complexity (1.1) | All processing (3.1) | Complex schemas increase CPU, memory, validation time |
| Compression (2.1.5) | Decompression (3.1.4) | Transport optimization creates processing cost |

---

## Diagnostic Decision Tree

```
START: Integration Failure Detected
│
├─→ Can System B parse the message?
│   ├─→ NO: INTERFACE LAYER (1.X)
│   │   ├─→ Schema error in logs?
│   │   │   └─→ Check 1.1 (Schema Compliance)
│   │   │       ├─→ Type mismatch? → 1.1.1
│   │   │       ├─→ Missing required field? → 1.1.2
│   │   │       ├─→ Wrong structure? → 1.1.3
│   │   │       └─→ Validation failed? → 1.1.4
│   │   │
│   │   ├─→ Protocol error?
│   │   │   └─→ Check 1.2 (Protocol Compatibility)
│   │   │       ├─→ REST vs gRPC? → 1.2.1 vs 1.2.2
│   │   │       ├─→ WebSocket issue? → 1.2.4
│   │   │       └─→ Message queue problem? → 1.2.5
│   │   │
│   │   ├─→ API contract violation?
│   │   │   └─→ Check 1.3 (Interface Contracts)
│   │   │       ├─→ Wrong version? → 1.3.1
│   │   │       ├─→ Bad endpoint? → 1.3.2
│   │   │       ├─→ Wrong HTTP method? → 1.3.3
│   │   │       └─→ Auth failure? → 1.3.4
│   │   │
│   │   └─→ Data type issue?
│   │       └─→ Check 1.4 (Data Typing Alignment)
│   │           ├─→ String/number mismatch? → 1.4.1
│   │           ├─→ Boolean problem? → 1.4.2
│   │           ├─→ Date format wrong? → 1.4.3
│   │           ├─→ NULL handling? → 1.4.4
│   │           └─→ Decimal precision? → 1.4.5
│   │
│   └─→ YES: Message parsed successfully
│       │
│       ├─→ Did the message arrive?
│       │   ├─→ NO: TRANSPORT LAYER (2.X)
│       │   │   ├─→ Message too large error?
│       │   │   │   └─→ Check 2.1 (Payload Size)
│       │   │   │       ├─→ Exceeds HTTP limit? → 2.1.1
│       │   │   │       ├─→ Exceeds queue limit? → 2.1.2
│       │   │   │       └─→ Need chunking? → 2.1.3
│       │   │   │
│       │   │   ├─→ Network timeout?
│       │   │   │   └─→ Check 2.2 (Bandwidth Limits)
│       │   │   │       ├─→ Low throughput? → 2.2.1
│       │   │   │       ├─→ High latency? → 2.2.2
│       │   │   │       ├─→ Packet loss? → 2.2.5
│       │   │   │       └─→ Cross-region? → 2.2.4
│       │   │   │
│       │   │   └─→ Rate limit error (429)?
│       │   │       └─→ Check 2.3 (Rate Limiting)
│       │   │           ├─→ Too many requests? → 2.3.1
│       │   │           ├─→ Too many connections? → 2.3.2
│       │   │           ├─→ Burst limit hit? → 2.3.3
│       │   │           └─→ Quota exceeded? → 2.3.6
│       │   │
│       │   └─→ YES: Message arrived
│       │       │
│       │       └─→ Was it processed successfully?
│       │           ├─→ NO: PROCESSING LAYER (3.X)
│       │           │   ├─→ System overloaded?
│       │           │   │   └─→ Check 3.1 (Computational Overhead)
│       │           │   │       ├─→ High CPU? → 3.1.1
│       │           │   │       ├─→ Expensive transform? → 3.1.2
│       │           │   │       ├─→ Slow validation? → 3.1.3
│       │           │   │       ├─→ Memory pressure? → 3.1.6
│       │           │   │       └─→ Database slow? → 3.1.7
│       │           │   │
│       │           │   ├─→ Timing issue?
│       │           │   │   └─→ Check 3.2 (Processing Windows)
│       │           │   │       ├─→ Batch too slow? → 3.2.1
│       │           │   │       ├─→ Micro-batch wrong? → 3.2.2
│       │           │   │       ├─→ SLA violation? → 3.2.4
│       │           │   │       ├─→ Out of order? → 3.2.5
│       │           │   │       └─→ Arrived too late? → 3.2.6
│       │           │   │
│       │           │   └─→ System throttling?
│       │           │       └─→ Check 3.3 (Throttling)
│       │           │           ├─→ Dynamic slowdown? → 3.3.1
│       │           │           ├─→ Queue backing up? → 3.3.2
│       │           │           ├─→ Backpressure signal? → 3.3.3
│       │           │           ├─→ Circuit breaker open? → 3.3.4
│       │           │           ├─→ Degraded mode? → 3.3.5
│       │           │           └─→ Priority dropped? → 3.3.6
│       │           │
│       │           └─→ YES: SUCCESS
│       │               └─→ Monitor for constraint drift
```

---

## The Onion Test Pattern

Test integration from inside out, layer by layer:

### Phase 1: Interface Layer Testing (Static)

**Goal**: Verify semantic and syntactic compatibility without moving data.

```
Test 1.1: Schema Compliance
  ├─ Generate sample message from System A
  ├─ Validate against System B's schema
  └─ Result: PASS/FAIL + specific constraint violations

Test 1.2: Protocol Compatibility
  ├─ Verify both systems speak same protocol
  ├─ Check HTTP methods, gRPC services, etc.
  └─ Result: PASS/FAIL

Test 1.3: Interface Contracts
  ├─ Version compatibility check
  ├─ Endpoint availability verification
  └─ Result: PASS/FAIL

Test 1.4: Data Typing Alignment
  ├─ Test type coercion rules
  ├─ Verify datetime, boolean, null handling
  └─ Result: PASS/FAIL
```

**If Phase 1 fails**: Stop. Fix Interface Layer before proceeding.

### Phase 2: Transport Layer Testing (Dynamic)

**Goal**: Verify physical message delivery without processing.

```
Test 2.1: Payload Size
  ├─ Send minimum payload
  ├─ Send maximum expected payload
  ├─ Send oversized payload (expect failure)
  └─ Result: Max successful size = X MB

Test 2.2: Bandwidth
  ├─ Measure latency (p50, p95, p99)
  ├─ Measure throughput
  ├─ Test with packet loss simulation
  └─ Result: Latency = X ms, Throughput = Y Mbps

Test 2.3: Rate Limiting
  ├─ Send at expected rate
  ├─ Send burst above limit
  ├─ Test retry/backoff behavior
  └─ Result: Limit = X req/s, Burst = Y req
```

**If Phase 2 fails**: Fix Transport Layer. Don't proceed to processing tests.

### Phase 3: Processing Layer Testing (Load)

**Goal**: Verify system can handle processing demands.

```
Test 3.1: Computational Overhead
  ├─ Measure per-message CPU cost
  ├─ Measure per-message memory cost
  ├─ Measure validation time
  └─ Result: CPU = X ms/msg, Memory = Y MB/msg

Test 3.2: Processing Windows
  ├─ Test batch completion time
  ├─ Test real-time processing latency
  ├─ Test with late-arriving data
  └─ Result: P95 latency = X ms

Test 3.3: Throttling
  ├─ Load test to trigger backpressure
  ├─ Verify circuit breaker behavior
  ├─ Test graceful degradation
  └─ Result: Breaks at X req/s, Recovers in Y seconds
```

### Onion Test Scorecard

```
┌──────────────────────────────────────────────────────┐
│ Integration Readiness Scorecard                      │
├──────────────────────────────────────────────────────┤
│ Phase 1: Interface Layer                             │
│   1.1 Schema Compliance           [✓] PASS           │
│   1.2 Protocol Compatibility      [✗] FAIL           │
│   1.3 Interface Contracts         [✓] PASS           │
│   1.4 Data Typing Alignment       [⚠] WARN           │
│   Phase 1 Status: BLOCKED - Fix 1.2                  │
│                                                       │
│ Phase 2: Transport Layer                             │
│   Status: NOT TESTED (blocked by Phase 1)            │
│                                                       │
│ Phase 3: Processing Layer                            │
│   Status: NOT TESTED (blocked by Phase 1)            │
│                                                       │
│ Overall: NOT READY                                   │
│ Next Action: Resolve protocol compatibility (1.2)    │
└──────────────────────────────────────────────────────┘
```

---

## Common Failure Patterns and Solutions

### Pattern 1: The Cascading Mismatch

**Symptom**: Fix one issue, another appears immediately.

**Example**:
1. Fix schema to match (1.1) → Now payload too large (2.1)
2. Add compression (2.1.5) → Now decompression takes too long (3.1.4)
3. Move to async processing (3.2) → Now violates SLA (3.2.4)

**Root Cause**: Solving at constraint level without considering cross-layer impacts.

**Solution**: Use constraint mapping (see template above) to identify all impacts before implementation.

### Pattern 2: The Wrong Layer Fix

**Symptom**: Solution reduces symptoms but doesn't address root cause.

**Example**: Hit rate limit (2.3.1) → Add compression (2.1.5)
- Compression is a Transport solution (2.1.5)
- Rate limiting is also Transport (2.3.1)
- But compression doesn't reduce request count!

**Root Cause**: Confusing payload size with request frequency.

**Solution**: 
- Identify the actual constrained resource (request count, not bandwidth)
- Apply correct solution (batching = 3.2, queuing = 3.3, backoff = 2.3.4)

### Pattern 3: The Premature Optimization

**Symptom**: Complex solution for non-existent problem.

**Example**: Build sophisticated retry logic (2.3.4) when schema doesn't match (1.1)
- No amount of retries will fix a schema mismatch
- Retries only make sense after Interface Layer is satisfied

**Root Cause**: Skipping The Onion Test, not testing layers in order.

**Solution**: Always validate Interface → Transport → Processing in order.

### Pattern 4: The Hidden Bottleneck

**Symptom**: System works perfectly in testing, fails in production.

**Example**: 
- Test with 1 message: ✓ (all constraints satisfied)
- Test with 100 messages: ✓ (3.1 constraints satisfied)
- Production with 10,000 messages: ✗ (3.3.2 queue depth exceeded)

**Root Cause**: Not testing at scale, missing Processing Layer constraints.

**Solution**: Load test at expected production volume + 2-3x safety margin.

---

## Anti-Patterns to Avoid

### 1. Treating Integration as Binary

**Wrong**:
```
if (integration_works) {
  deploy();
} else {
  debug_everything();
}
```

**Right**:
```
test_interface_layer();
if (interface_failed) {
  fix_constraints_1_X();
  retest();
}

test_transport_layer();
if (transport_failed) {
  fix_constraints_2_X();
  retest();
}

test_processing_layer();
if (processing_failed) {
  fix_constraints_3_X();
  retest();
}

deploy_with_monitoring();
```

### 2. Layer Confusion

**Wrong**: "We have a latency problem" → Buy more bandwidth (assumes Transport 2.2)

**Right**: Diagnose first:
- Is it network latency (2.2.2)?
- Is it processing latency (3.1)?
- Is it queueing latency (3.2)?

Different diagnoses require different solutions.

### 3. Ignoring Cross-Layer Effects

**Wrong**: Optimize Processing Layer (3.1.3) by removing validation → Now Interface Layer breaks (1.1.4)

**Right**: Evaluate ripple effects before implementing changes. Use the Cross-Layer Interaction Matrix.

### 4. Documentation Mismatch

**Wrong**: Document System A's capabilities, assume System B can handle them.

**Right**: Document constraint matrix for both systems, identify mismatches proactively.

---

## Monitoring Strategy

### Layer-Specific Metrics

**Interface Layer (1.X) - Health Metrics**:
```
- schema_validation_failure_rate (1.1)
- protocol_negotiation_errors (1.2)
- api_version_distribution (1.3.1)
- type_coercion_error_count (1.4)
```

**Transport Layer (2.X) - Performance Metrics**:
```
- payload_size_p50_p95_p99 (2.1)
- request_latency_p50_p95_p99 (2.2.2)
- rate_limit_hit_count (2.3.1)
- retry_attempt_distribution (2.3.4)
```

**Processing Layer (3.X) - Capacity Metrics**:
```
- cpu_per_message_avg (3.1.1)
- validation_time_p95 (3.1.3)
- queue_depth_current (3.3.2.1)
- circuit_breaker_state (3.3.4)
- processing_latency_p99 (3.2.4)
```

### Alert Thresholds

```yaml
alerts:
  interface:
    - metric: schema_validation_failure_rate
      constraint: 1.1
      threshold: >5%
      severity: critical
      action: "Check schema compatibility immediately"
  
  transport:
    - metric: rate_limit_hit_count
      constraint: 2.3.1
      threshold: >10/min
      severity: warning
      action: "Implement backoff or increase limit"
    
    - metric: payload_size_p99
      constraint: 2.1.1.1
      threshold: >80% of max
      severity: warning
      action: "Consider chunking or compression"
  
  processing:
    - metric: queue_depth_current
      constraint: 3.3.2.1
      threshold: >1000
      severity: warning
      action: "Scale processing or implement backpressure"
    
    - metric: circuit_breaker_state
      constraint: 3.3.4
      threshold: "open"
      severity: critical
      action: "Integration is down, investigate immediately"
```

---

## Quick Reference: Constraint Lookup

### By Error Message

| Error Message | Likely Constraint | Check |
|--------------|-------------------|-------|
| "Invalid JSON" | 1.1.1 | Field types |
| "Missing required field" | 1.1.2 | Required constraints |
| "Request entity too large" | 2.1.1 | HTTP request limits |
| "429 Too Many Requests" | 2.3.1 | Request rate limits |
| "Gateway timeout" | 2.2.2 or 3.1 | Latency or processing |
| "Circuit breaker open" | 3.3.4 | Circuit breakers |
| "Schema validation failed" | 1.1.4 | Validation rules |
| "Unsupported method" | 1.3.3 | Allowed verbs |

### By Symptom

| Symptom | Likely Constraint | Check |
|---------|-------------------|-------|
| Messages not parsed | 1.X | Entire Interface Layer |
| Messages not arriving | 2.X | Entire Transport Layer |
| Messages piling up in queue | 3.3.2 or 3.2 | Queue depth or windows |
| Intermittent failures | 2.3 or 3.3 | Rate limiting or throttling |
| Slow processing | 3.1 | Computational overhead |
| Wrong data format | 1.4 | Data typing alignment |

---

## Version History

**Version 1.0** - November 2025
- Initial hierarchical decomposition
- 3 layers, 12 categories, 80+ constraint types, 200+ source constraints
- Diagnostic framework and practical patterns

---

**Framework**: Interoperability Constraint Model  
**Documentation**: Practical Applications Guide  
**Maintained By**: Framework
