# ETL Pipeline Interoperability Chain  
(With Table of Contents, Links, and Complete Example)

ETL = Extract → Transform → Load  
Each phase uses its own interoperability layers and standards.

---

# Table of Contents

## Extract Phase
1. [Source System](#1-source-system)  
2. [Protocol](#2-protocol)  
3. [Data Format](#3-data-format)  
4. [Serialization Layer](#4-serialization-layer)  
5. [Transport Layer](#5-transport-layer)  
6. [Extraction Layer](#6-extraction-layer)  
7. [Parsing Layer](#7-parsing-layer)  

## Transform Phase
8. [Validation Layer](#8-validation-layer)  
9. [Type Normalization Layer](#9-type-normalization-layer)  
10. [Shape Normalization Layer](#10-shape-normalization-layer)  
11. [Schema Compliance Layer](#11-schema-compliance-layer)  
12. [Transformation Logic](#12-transformation-logic)  
13. [Semantic Validation](#13-semantic-validation)  

## Load Phase
14. [Output Data Format](#14-output-data-format)  
15. [Destination Protocol](#15-destination-protocol)  
16. [Batch / Stream Loading Layer](#16-batch--stream-loading-layer)  
17. [Transaction Boundary](#17-transaction-boundary)  
18. [Persistence Layer](#18-persistence-layer)  
19. [Storage Model](#19-storage-model)  
20. [Indexing / Constraints](#20-indexing--constraints)  
21. [Metadata / Catalog](#21-metadata--catalog)  

## Example
22. [Example: Full End-to-End ETL Pipeline](#22-example--full-end-to-end-etl-pipeline)

---

# PHASE 1: EXTRACT  
(Where data originates + how it enters the pipeline)

---

## 1. Source System
**References**
- SQL Databases: https://www.postgresql.org/docs/current/  
- NoSQL: https://www.mongodb.com/docs/  
- REST APIs: https://restfulapi.net  
- GraphQL: https://graphql.org/learn  
- gRPC: https://grpc.io/docs/  
- SOAP: https://www.w3.org/TR/soap/  
- CSV/JSON/XML: https://www.rfc-editor.org/rfc/rfc4180  
- Parquet: https://parquet.apache.org/  
- Kafka Streams: https://kafka.apache.org/documentation/streams/  
- SaaS Connectors: https://www.fivetran.com/docs  

---

## 2. Protocol
**References**
- REST / HTTP: https://developer.mozilla.org/en-US/docs/Web/HTTP  
- JDBC: https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/  
- ODBC: https://learn.microsoft.com/en-us/sql/odbc/  
- SFTP/FTP: https://datatracker.ietf.org/doc/html/rfc959  
- Kafka Protocol: https://kafka.apache.org/protocol  
- gRPC Protocol: https://github.com/grpc/grpc/blob/master/doc/PROTOCOL-HTTP2.md  

---

## 3. Data Format
**References**
- JSON: https://www.json.org  
- CSV: https://www.rfc-editor.org/rfc/rfc4180  
- XML: https://www.w3.org/XML/  
- Parquet: https://parquet.apache.org/documentation/latest/  
- Protobuf: https://protobuf.dev  
- Avro: https://avro.apache.org/docs/current/  

---

## 4. Serialization Layer
**References**
- UTF-8: https://www.rfc-editor.org/rfc/rfc3629  
- Avro Encoding: https://avro.apache.org/docs/current/spec.html  
- Protobuf Encoding: https://protobuf.dev/programming-guides/encoding/  
- Parquet Encoding: https://parquet.apache.org/docs/file-format/  

---

## 5. Transport Layer
**References**
- HTTP/1.1: https://www.rfc-editor.org/rfc/rfc2616  
- TCP: https://www.rfc-editor.org/rfc/rfc793  
- SFTP: https://datatracker.ietf.org/doc/html/draft-ietf-secsh-filexfer-13  
- Kafka Transport: https://kafka.apache.org/documentation/#design  

---

## 6. Extraction Layer
**References**
- Airbyte: https://docs.airbyte.com  
- Fivetran: https://www.fivetran.com/docs/getting-started  
- Airflow Scheduler: https://airflow.apache.org/docs/  
- Kafka Offsets: https://kafka.apache.org/documentation/#consumerconfigs_offsets  

---

## 7. Parsing Layer
**References**
- CSV Parser: https://docs.python.org/3/library/csv.html  
- JSON Parser: https://www.json.org/json-en.html  
- XML Parser (XSD): https://www.w3.org/TR/xmlschema11-1/  
- Avro Decoder: https://avro.apache.org/docs/current/getting-started-java/  
- Parquet Reader: https://parquet.apache.org/docs/how-to/  

---

# PHASE 2: TRANSFORM  
(Cleaning, normalizing, validating, enriching the data)

---

## 8. Validation Layer
**References**
- Fowler Data Validation: https://martinfowler.com/articles/data-validation.html  
- JSON Schema: https://json-schema.org/learn  
- Avro Schema Validation: https://avro.apache.org/docs/current/spec.html  

---

## 9. Type Normalization Layer
**References**
- SQL Casting: https://www.postgresql.org/docs/current/typeconv.html  
- Pandas Type System: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.astype.html  
- Spark Casting: https://spark.apache.org/docs/latest/api/sql/index.html  

---

## 10. Shape Normalization Layer
**References**
- Spark JSON Flattening: https://spark.apache.org/docs/latest/sql-data-sources-json.html  
- Delta Schema Evolution: https://docs.delta.io/latest/delta-schema-evolution.html  
- SQL Deduplication: https://www.postgresql.org/docs/current/queries-with.html  

---

## 11. Schema Compliance Layer
**References**
- JSON Schema: https://json-schema.org  
- Avro Schema Spec: https://avro.apache.org/docs/current/spec.html  
- Delta Lake Enforcement: https://docs.delta.io/latest/delta-schema-enforcement.html  
- Warehouse Star Schema: https://www.databricks.com/glossary/star-schema  

---

## 12. Transformation Logic
**References**
- SQL Joins/Aggregations: https://www.postgresql.org/docs/current/queries.html  
- Spark Transformations: https://spark.apache.org/docs/latest/sql-programming-guide.html  
- DBT Transformations: https://docs.getdbt.com/docs/introduction  

---

## 13. Semantic Validation
**References**
- ISO 8601 Dates: https://www.iso.org/standard/70907.html  
- ISO 4217 Currencies: https://www.iso.org/iso-4217-currency-codes.html  
- Referential Integrity: https://www.postgresql.org/docs/current/ddl-constraints.html  

---

# PHASE 3: LOAD  
(Writing the transformed data into the final system)

---

## 14. Output Data Format
**References**
- Parquet: https://parquet.apache.org/  
- ORC: https://orc.apache.org/  
- Avro: https://avro.apache.org/  
- Delta Lake: https://docs.delta.io/latest/  

---

## 15. Destination Protocol
**References**
- JDBC: https://docs.oracle.com/javase/8/docs/technotes/guides/jdbc/  
- ODBC: https://learn.microsoft.com/en-us/sql/odbc/  
- BigQuery Ingest: https://cloud.google.com/bigquery/docs/loading-data  
- Snowflake Ingest: https://docs.snowflake.com/en/user-guide/data-load-intro  
- S3 PutObject: https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html  
- GCS Upload: https://cloud.google.com/storage/docs  

---

## 16. Batch / Stream Loading Layer
**References**
- Spark Structured Streaming: https://spark.apache.org/docs/latest/structured-streaming-programming-guide.html  
- Kafka Streams: https://kafka.apache.org/documentation/streams/  
- Snowpipe Streaming: https://docs.snowflake.com/en/user-guide/data-load-snowpipe  
- BigQuery Streaming: https://cloud.google.com/bigquery/streaming-data-into-bigquery  

---

## 17. Transaction Boundary
**References**
- ACID Transactions: https://en.wikipedia.org/wiki/ACID  
- Idempotence: https://cloud.google.com/architecture/idempotent-design-considerations  
- Upserts / MERGE: https://docs.snowflake.com/en/sql-reference/sql/merge  
- Delta Lake Logs: https://docs.delta.io/latest/delta-transaction-log.html  

---

## 18. Persistence Layer
**References**
- BigQuery: https://cloud.google.com/bigquery  
- Snowflake: https://docs.snowflake.com  
- Redshift: https://docs.aws.amazon.com/redshift/  
- Databricks: https://docs.databricks.com/  
- Iceberg / Hudi / Delta: https://iceberg.apache.org | https://hudi.apache.org | https://delta.io  

---

## 19. Storage Model
**References**
- Columnar Storage: https://cloud.google.com/bigquery/docs/storage-overview  
- Partitioning: https://cloud.google.com/bigquery/docs/partitioned-tables  
- Clustering / Z-order: https://docs.databricks.com/en/delta/clustering.html  

---

## 20. Indexing / Constraints
**References**
- BigQuery Clustering: https://cloud.google.com/bigquery/docs/clustered-tables  
- Snowflake Micro-partitions: https://docs.snowflake.com/en/user-guide/tables-clustering-micropartitions  
- Redshift Sort Keys: https://docs.aws.amazon.com/redshift/latest/dg/t_Sorting_data.html  

---

## 21. Metadata / Catalog
**References**
- Hive Metastore: https://cwiki.apache.org/confluence/display/Hive/Design  
- AWS Glue Data Catalog: https://docs.aws.amazon.com/glue/latest/dg/catalog.html  
- BigQuery Information Schema: https://cloud.google.com/bigquery/docs/information-schema-intro  
- Unity Catalog: https://docs.databricks.com/en/data-governance/unity-catalog/index.html  

---

# 22. EXAMPLE: Full End-to-End ETL Pipeline

### Example: Shopify → Airbyte → Spark → Snowflake

**Extract**  
1. Shopify API (REST JSON)  
2. Retrieved via HTTPS  
3. JSON format  
4. UTF-8 text serialization  
5. Transport: HTTP/2  
6. Extraction: Airbyte connector  
7. Parsing: JSON parser → row objects  

**Transform**  
8. Validate: required fields (order_id, total_price)  
9. Normalize types: `"42"` → integer  
10. Shape normalize: flatten `customer.address.*`  
11. Schema enforce: Avro/warehouse schema  
12. Transform logic: join orders + customers  
13. Semantic checks: ensure currency = USD  

**Load**  
14. Output format: Parquet  
15. Destination protocol: Snowflake ingest API  
16. Micro-batch load (every 5 min)  
17. Idempotent MERGE (upsert)  
18. Snowflake warehouse stores data  
19. Columnar + partitions by date  
20. Clustering by `customer_id`  
21. Metadata stored in Snowflake Catalog  

This pipeline is typical of modern SaaS → warehouse systems.
