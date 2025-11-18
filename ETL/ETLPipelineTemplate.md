# (ETL → Layers → Multi vs Single)
## PHASE 1: EXTRACT
**1. Protocols: [MULTI-SELECT]**

Used to pull data from systems.
| Item           | Link                                                                               | Tags                        |
| -------------- | ---------------------------------------------------------------------------------- | --------------------------- |
| REST           | [https://restfulapi.net](https://restfulapi.net)                                   | Cloud, Apps, SaaS           |
| GraphQL        | [https://graphql.org/learn](https://graphql.org/learn)                             | Apps, SaaS                  |
| gRPC           | [https://grpc.io/docs](https://grpc.io/docs)                                       | API/MS, Distributed Systems |
| SOAP/XML       | [https://www.w3.org/TR/soap/](https://www.w3.org/TR/soap/)                         | Enterprise                  |
| Webhooks       | [https://webhooks.fyi](https://webhooks.fyi)                                       | SaaS                        |
| Kafka Protocol | [https://kafka.apache.org/documentation/](https://kafka.apache.org/documentation/) | Streaming, ETL/DS           |
| MQTT           | [https://mqtt.org](https://mqtt.org)                                               | IoT, Monitoring             |

**2. Transport Formats: [SINGLE-SELECT]**

Each request/event uses one format.
| Format   | Link                                                                             |
| -------- | -------------------------------------------------------------------------------- |
| JSON     | [https://www.json.org](https://www.json.org)                                     |
| XML      | [https://www.w3.org/XML](https://www.w3.org/XML)                                 |
| Protobuf | [https://protobuf.dev](https://protobuf.dev)                                     |
| Avro     | [https://avro.apache.org/docs/current](https://avro.apache.org/docs/current)     |
| CSV      | [https://www.rfc-editor.org/rfc/rfc4180](https://www.rfc-editor.org/rfc/rfc4180) |

**3. Serialization: [SINGLE-SELECT]**
   
| Format      | Link                                                                             | Tags                  |
| ----------- | -------------------------------------------------------------------------------- | --------------------- |
| UTF-8       | [https://www.rfc-editor.org/rfc/rfc3629](https://www.rfc-editor.org/rfc/rfc3629) | Cloud, Apps           |
| Base64      | [https://www.rfc-editor.org/rfc/rfc4648](https://www.rfc-editor.org/rfc/rfc4648) | File transfer         |
| MessagePack | [https://msgpack.org](https://msgpack.org)                                       | High-performance APIs |
| CBOR        | [https://cbor.io](https://cbor.io)                                               | IoT                   |
| Binary      |:                                                                                | IoT, RPC              |

**4. Authentication: [MULTI-SELECT]**

| Type     | Link                                                                                           | Tags                  |
| -------- | ---------------------------------------------------------------------------------------------- | --------------------- |
| OAuth2   | [https://oauth.net/2](https://oauth.net/2)                                                     | Apps, SaaS, Cloud     |
| JWT      | [https://jwt.io](https://jwt.io)                                                               | Apps, API/MS          |
| API Keys | [https://datatracker.ietf.org/doc/html/rfc6750](https://datatracker.ietf.org/doc/html/rfc6750) | SaaS                  |
| HMAC     | [https://www.rfc-editor.org/rfc/rfc2104](https://www.rfc-editor.org/rfc/rfc2104)               | Finance, API security |

**5. Ingestion Methods: [MULTI-SELECT]**

| Method              | Link                                                 | Tags        |
| ------------------- | ---------------------------------------------------- | ----------- |
| Batch ingestion     |:                                                    | ETL/DS      |
| Streaming (Kafka)   | [https://kafka.apache.org](https://kafka.apache.org) | ETL/DS      |
| Micro-batch (Spark) | [https://spark.apache.org](https://spark.apache.org) | ETL/DS      |
| API ingestion       |:                                                    | Cloud, Apps |
| Webhook ingestion   |:                                                    | SaaS        |

**6. Parsing: [SINGLE-SELECT]**
- JSON parser
- XML parser
- CSV parser
- Avro/Protobuf decoder

## PHASE 2: TRANSFORM
**7. Validation (Structural): [SINGLE-SELECT]**
- Required fields
- Nullability
- Type correctness

**8. Type Normalization: [SINGLE-SELECT]**
- String → int
- String → date
- Float precision fixes
- Boolean coercion

**9. Shape Normalization: [SINGLE-SELECT]**
- Flatten nested objects
- Normalize arrays
- Dedup rows
- Remove schema drift

**10. Schema Enforcement: [SINGLE-SELECT]**
| Schema          | Link                                                                         | Tags          |
| --------------- | ---------------------------------------------------------------------------- | ------------- |
| JSON Schema     | [https://json-schema.org](https://json-schema.org)                           | Apps, SaaS    |
| Avro Schema     | [https://avro.apache.org/docs/current](https://avro.apache.org/docs/current) | ETL/DS        |
| Protobuf Schema | [https://protobuf.dev](https://protobuf.dev)                                 | Microservices |
| Delta Schema    | [https://docs.delta.io](https://docs.delta.io)                               | ETL/DS        |

**11. Semantic Validation: [SINGLE-SELECT]**
- Valid date ranges
- Correct currencies
- Referential rules

**12. Business Logic: [SINGLE-SELECT]**
| Item                        | Link                                                                     | Tags             |
| --------------------------- | ------------------------------------------------------------------------ | ---------------- |
| Domain-Driven Design        | [https://www.domainlanguage.com/ddd](https://www.domainlanguage.com/ddd) | Apps, Enterprise |
| Workflow Engines (Temporal) | [https://temporal.io](https://temporal.io)                               | SaaS, Cloud      |.

## PHASE 3: LOAD
**13. Output Destinations: [MULTI-SELECT]**
| Destination | Link                                                                                                             | Tags       |
| ----------- | ---------------------------------------------------------------------------------------------------------------- | ---------- |
| BigQuery    | [https://cloud.google.com/bigquery](https://cloud.google.com/bigquery)                                           | Cloud, ETL |
| Snowflake   | [https://docs.snowflake.com](https://docs.snowflake.com)                                                         | ETL/DS     |
| S3          | [https://docs.aws.amazon.com/AmazonS3/latest/userguide/](https://docs.aws.amazon.com/AmazonS3/latest/userguide/) | Cloud      |
| GCS         | [https://cloud.google.com/storage/docs](https://cloud.google.com/storage/docs)                                   | Cloud      |
| Postgres    | [https://www.postgresql.org/docs/current](https://www.postgresql.org/docs/current)                               | Apps       |
| MySQL       | [https://dev.mysql.com/doc](https://dev.mysql.com/doc)                                                           | Apps       |
| Redis       | [https://redis.io/docs](https://redis.io/docs)                                                                   | Caching    |
| Kafka       | [https://kafka.apache.org](https://kafka.apache.org)                                                             | Streaming  |

**14. Storage Model: [SINGLE-SELECT per dataset]**
| Model      | Link                                                                                                               | Tags       |
| ---------- | ------------------------------------------------------------------------------------------------------------------ | ---------- |
| Columnar   | [https://cloud.google.com/bigquery/docs/storage-overview](https://cloud.google.com/bigquery/docs/storage-overview) | ETL/DS     |
| Document   | [https://www.mongodb.com/docs](https://www.mongodb.com/docs)                                                       | Apps       |
| Relational | [https://www.postgresql.org/docs/current](https://www.postgresql.org/docs/current)                                 | Apps, SaaS |
| Key-value  | [https://redis.io/docs](https://redis.io/docs)                                                                     | Cloud      |

**15. Database Constraints: [SINGLE-SELECT per engine]**
| Constraint        | Link                                                                                                                         |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| PK/FK             | [https://www.postgresql.org/docs/current/ddl-constraints.html](https://www.postgresql.org/docs/current/ddl-constraints.html) |
| Unique            | same as above                                                                                                                |
| Check constraints | same                                                                                                                         |
| Partition keys    | [https://cloud.google.com/bigquery/docs/partitioned-tables](https://cloud.google.com/bigquery/docs/partitioned-tables)       |

**16. Observability: [MULTI-SELECT]**
    | Tool          | Link                                                                     | Tags       |
| ------------- | ------------------------------------------------------------------------ | ---------- |
| Prometheus    | [https://prometheus.io](https://prometheus.io)                           | Monitoring |
| Grafana       | [https://grafana.com](https://grafana.com)                               | Monitoring |
| OpenTelemetry | [https://opentelemetry.io](https://opentelemetry.io)                     | Cloud      |
| CloudWatch    | [https://aws.amazon.com/cloudwatch/](https://aws.amazon.com/cloudwatch/) | Cloud      |

