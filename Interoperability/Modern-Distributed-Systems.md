# Modern Distributed Systems Components 

These components appear in modern microservices, high-scale SaaS platforms, and enterprise distributed systems.

---

## 1. Network Constraints Handling
Managing latency, jitter, timeouts, packet limits, retries, backoff, and congestion.

**Official References**
- Latency fundamentals: https://en.wikipedia.org/wiki/Latency_(engineering)
- Jitter: https://en.wikipedia.org/wiki/Jitter
- Exponential backoff (Google): https://cloud.google.com/storage/docs/exponential-backoff
- TCP congestion control: https://www.rfc-editor.org/rfc/rfc5681
- Timeouts (MDN HTTP): https://developer.mozilla.org/en-US/docs/Web/HTTP/Timeouts

---

## 2. Load Balancers
Distribute traffic across services and nodes for availability, performance, and failover.

**Official References**
- Concepts overview (Cloudflare): https://www.cloudflare.com/learning/performance/what-is-load-balancing/
- NGINX load balancing: https://nginx.org/en/docs/http/load_balancing.html
- AWS Elastic Load Balancer: https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-elastic-load-balancing.html
- Envoy Proxy load balancing: https://www.envoyproxy.io/docs/envoy/latest/intro/arch_overview/load_balancing/overview

---

## 3. Replication / Journaling / ACID Semantics
Ensures durability, consistency, and resilience in distributed databases.

**Official References**
- Write-Ahead Log (Postgres): https://www.postgresql.org/docs/current/wal-intro.html
- Replication models (logical/physical): https://www.postgresql.org/docs/current/logical-replication.html
- ACID definition: https://en.wikipedia.org/wiki/ACID
- Eventual vs strong consistency (Jepsen): https://jepsen.io/consistency
- Dynamo-style consistency model: https://www.allthingsdistributed.com/files/amazon-dynamo-sosp2007.pdf

---

## 4. Read Model / Query Model (CQRS Pattern)
Splitting read model and write model for scalability and system decoupling.

**Official References**
- CQRS pattern (Microsoft): https://learn.microsoft.com/en-us/azure/architecture/patterns/cqrs
- Event sourcing overview: https://martinfowler.com/eaaDev/EventSourcing.html
- Materialized views: https://www.postgresql.org/docs/current/rules-materializedviews.html
- Query optimization (Postgres): https://www.postgresql.org/docs/current/using-explain.html

---

## 5. Event / Message Emission
Propagating domain events, integrating systems, and enabling asynchronous workflows.

**Official References**
- Apache Kafka: https://kafka.apache.org/documentation/
- Webhooks: https://webhooks.fyi
- gRPC streaming: https://grpc.io/docs/what-is-grpc/core-concepts/#server-streaming-rpc
- Domain events (DDD): https://martinfowler.com/eaaDev/DomainEvent.html
- Event-driven architecture (AWS): https://docs.aws.amazon.com/lambda/latest/dg/with-s3-example.html
