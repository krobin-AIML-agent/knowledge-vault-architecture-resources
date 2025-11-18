# Maximum Interoperability Chain (With Links)

---

# 1. External Actor
- **User**: A human interacting through a UI or app.  
- **System**: Another backend service calling your API.  
- **Device**: Phones, tablets, sensors.  
- **Service**: External SaaS or APIs.  

(No standards: conceptual category.)

---

# 2. Interaction Method
- **HTTP request**: https://developer.mozilla.org/en-US/docs/Web/HTTP  
- **WebSocket message**: https://www.rfc-editor.org/rfc/rfc6455  
- **Mobile SDK call**: (platform-specific; example) https://firebase.google.com/docs/reference  
- **CLI request**: https://en.wikipedia.org/wiki/Command-line_interface  
- **IoT signal (MQTT)**: https://mqtt.org  

---

# 3. Protocol
- **REST**: https://restfulapi.net  
- **GraphQL**: https://graphql.org/learn  
- **gRPC**: https://grpc.io/docs/what-is-grpc/core-concepts  
- **SOAP**: https://www.w3.org/TR/soap/  
- **Webhooks**: https://webhooks.fyi  
- **Kafka / Streams**: https://kafka.apache.org/documentation/  
- **SSE (Server-Sent Events)**: https://html.spec.whatwg.org/multipage/server-sent-events.html  

---

# 4. API Interface Layer
- **Contract definition** (OpenAPI): https://swagger.io/specification  
- **Endpoint shape** (URI spec): https://www.rfc-editor.org/rfc/rfc3986  

---

# 5. Data Format
- **JSON**: https://www.json.org  
- **XML**: https://www.w3.org/XML  
- **Protobuf**: https://protobuf.dev  
- **Avro**: https://avro.apache.org/docs/current/  
- **CSV**: https://www.rfc-editor.org/rfc/rfc4180  
- **Multipart**: https://www.rfc-editor.org/rfc/rfc2388  

---

# 6. Serialization
- **UTF-8**: https://www.rfc-editor.org/rfc/rfc3629  
- **Binary**: (general) https://en.wikipedia.org/wiki/Binary_data  
- **Base64**: https://www.rfc-editor.org/rfc/rfc4648  
- **MessagePack**: https://msgpack.org  
- **CBOR**: https://cbor.io  

---

# 7. Transport Layer
- **HTTP/1.1**: https://www.rfc-editor.org/rfc/rfc2616  
- **HTTP/2**: https://http2.github.io  
- **HTTP/3 / QUIC**: https://www.rfc-editor.org/rfc/rfc9000  
- **WebSockets**: https://www.rfc-editor.org/rfc/rfc6455  
- **MQTT**: https://mqtt.org  
- **Kafka**: https://kafka.apache.org/documentation/  

---

# 8. Network Constraints
- **Latency**: https://en.wikipedia.org/wiki/Latency_(engineering)  
- **Jitter**: https://en.wikipedia.org/wiki/Jitter  
- **Timeouts**: https://developer.mozilla.org/en-US/docs/Web/HTTP/Timeouts  
- **Chunking**: https://www.rfc-editor.org/rfc/rfc7230#section-4.1  
- **MTU/MSS**: https://en.wikipedia.org/wiki/Maximum_transmission_unit  
- **Body size limits** (NGINX): https://nginx.org/en/docs/http/ngx_http_core_module.html#client_max_body_size  

---

# 9. Gateway / Middleware
- **API Gateway**: https://aws.amazon.com/api-gateway/  
- **Load balancer**: https://www.cloudflare.com/learning/performance/what-is-load-balancing/  
- **Reverse proxy**: https://nginx.org/en/docs/  
- **CDN edge**: https://www.cloudflare.com/learning/cdn/what-is-a-cdn/  

---

# 10. Authentication & Authorization
- **Tokens**: https://datatracker.ietf.org/doc/html/rfc6750  
- **OAuth2**: https://oauth.net/2/  
- **JWT**: https://jwt.io/introduction  
- **HMAC signatures**: https://www.rfc-editor.org/rfc/rfc2104  

---

# 11. Rate / Quota Controls
- **Rate limiting**: https://cloudflare.com/learning/bots/what-is-rate-limiting/  
- **Circuit breakers**: https://martinfowler.com/bliki/CircuitBreaker.html  

---

# 12. Request Parsing
- **JSON parsing**: https://www.json.org/json-en.html  
- **Protobuf decode**: https://protobuf.dev/programming-guides/  
- **Multipart parsing**: https://www.rfc-editor.org/rfc/rfc7578  

---

# 13. Request Validation
- **Schema validation**: https://json-schema.org/  
- **OWASP input validation**: https://owasp.org/www-community/controls/Input_Validation_Cheat_Sheet  

---

# 14. Type Normalization
- **ECMAScript coercion rules**: https://262.ecma-international.org/#sec-type-conversion  
- **RFC3339 timestamps**: https://www.rfc-editor.org/rfc/rfc3339  

---

# 15. Shape Normalization
- **Canonicalization definition**: https://en.wikipedia.org/wiki/Canonicalization  

---

# 16. Schema Compliance
- **JSON Schema**: https://json-schema.org  
- **XML Schema (XSD)**: https://www.w3.org/XML/Schema  
- **Protobuf schema**: https://protobuf.dev/programming-guides/proto3  

---

# 17. Version Compatibility
- **API versioning best practices**: https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design#versioning  

---

# 18. Semantic Validation
- **ISO 8601 dates**: https://www.iso.org/standard/70907.html  
- **Email validation (RFC5322)**: https://www.rfc-editor.org/rfc/rfc5322  
- **E.164 phone format**: https://www.itu.int/rec/T-REC-E.164/en  

---

# 19. Business Logic
- **DDD (domain logic)**: https://www.domainlanguage.com/ddd  
- **Business rules patterns**: https://martinfowler.com/bliki/BusinessRules.html  

---

# 20. Domain Modeling
- **Domain modeling (DDD)**: https://martinfowler.com/tags/domain.html  

---

# 21. ORM / Mapping Layer
- **Prisma**: https://www.prisma.io/docs  
- **Hibernate**: https://hibernate.org  
- **SQLAlchemy**: https://docs.sqlalchemy.org  
- **ActiveRecord**: https://guides.rubyonrails.org/active_record_basics.html  

---

# 22. Transaction Boundary
- **Database transactions**: https://en.wikipedia.org/wiki/Database_transaction  
- **ACID**: https://en.wikipedia.org/wiki/ACID  
- **Isolation levels**: https://www.postgresql.org/docs/current/transaction-iso.html  

---

# 23. Persistence Layer
- **SQL CRUD**: https://www.postgresql.org/docs/current/tutorial-sql.html  
- **MongoDB CRUD**: https://www.mongodb.com/docs/manual/crud/  
- **DynamoDB writes**: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html  

---

# 24. Database Storage Model
- **Relational (Postgres)**: https://www.postgresql.org/docs/current/storage.html  
- **Document model (MongoDB)**: https://www.mongodb.com/docs/manual/core/document  
- **Key-value (DynamoDB)**: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html  
- **Columnar (BigQuery)**: https://cloud.google.com/bigquery/docs/storage-overview  
- **Columnar (ClickHouse)**: https://clickhouse.com/docs/en/architecture/storage  

---

# 25. Indexing / Partitioning / Constraints
- **Postgres indexing**: https://www.postgresql.org/docs/current/indexes.html  
- **MySQL indexing**: https://dev.mysql.com/doc/refman/8.0/en/mysql-indexes.html  
- **Partitioning**: https://www.postgresql.org/docs/current/ddl-partitioning.html  
- **Constraints**: https://www.postgresql.org/docs/current/ddl-constraints.html  

---

# 26. Replication / Journaling / ACID
- **WAL (Write-Ahead Log)**: https://www.postgresql.org/docs/current/wal-intro.html  
- **Replication models**: https://www.postgresql.org/docs/current/logical-replication.html  
- **Consistency models**: https://jepsen.io/consistency  

---

# 27. Read Model / Query Model
- **SQL**: https://www.postgresql.org/docs/current/sql-select.html  
- **Views**: https://www.postgresql.org/docs/current/sql-createview.html  
- **Materialized views**: https://www.postgresql.org/docs/current/rules-materializedviews.html  

---

# 28. Caching Layer
- **Redis**: https://redis.io/docs  
- **Memcached**: https://memcached.org  
- **Application caching**: https://martinfowler.com/bliki/Cache.html  

---

# 29. Event / Message Emission
- **Kafka**: https://kafka.apache.org/documentation/  
- **Webhooks**: https://webhooks.fyi  
- **gRPC streams**: https://grpc.io/docs/what-is-grpc/core-concepts/#server-streaming-rpc  
- **Domain events (DDD)**: https://martinfowler.com/eaaDev/EventSourcing.html  

---

# 30. Data Warehouse / Lake Sync
- **BigQuery**: https://cloud.google.com/bigquery  
- **Snowflake**: https://docs.snowflake.com  
- **AWS S3**: https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html  
- **Google Cloud Storage**: https://cloud.google.com/storage/docs  

---

# 31. Downstream Consumer Systems
- **Analytics dashboards** (Looker): https://cloud.google.com/looker/docs  
- **ML pipelines (TensorFlow)**: https://www.tensorflow.org/  
- **Downstream APIs**: (varies by integration)  
- **Business intelligence tools**: https://www.tableau.com  
