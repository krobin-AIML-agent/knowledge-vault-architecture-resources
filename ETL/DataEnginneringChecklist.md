# DATA ENGINEERING MASTER WORKFLOW CHECKLIST 
_Pre → Ingest → Process → Store → Serve → Govern_

---

# PHASE 0: SCOPING

## 0.1 Define the Data Source  
- [Multi-select]  
  - [ ] SaaS API  
  - [ ] Database extraction via
    - **CDC** → https://debezium.io/  
  - [ ] Event/stream → 
    - **Kafka** https://kafka.apache.org
    - **Kinesis** https://aws.amazon.com/kinesis
    - **Pub/Sub** https://cloud.google.com/pubsub  
  - [ ] Batch files (CSV, Parquet, JSONL)  
  - [ ] Internal microservice  
  - [ ] Partner/3rd-party feed  

## 0.2 Define Data Movement Pattern  
- [Single-select]  
  - [ ] Batch ETL  
  - [ ] Streaming/real-time  
  - [ ] Micro-batch (Databricks) → https://www.databricks.com/

## 0.3 Define SLA & Latency  
- [Single-select]  
  - [ ] Real-time (sub-second)  
  - [ ] Near real-time  
  - [ ] Batch  

---

# PHASE 1: PRE (Before Ingestion)

## 1.1 Select Ingestion Method  
- [Single-select]  
  - [ ] API ingestion  
  - [ ] CDC extraction (Debezium → https://debezium.io/ , AWS DMS → https://aws.amazon.com/dms/)  
  - [ ] File ingestion (S3 → https://aws.amazon.com/s3/ , GCS → https://cloud.google.com/storage , ADLS → https://learn.microsoft.com/azure/storage/)  
  - [ ] Stream ingestion (Kafka → https://kafka.apache.org/ , Kinesis → https://aws.amazon.com/kinesis/ , Pub/Sub → https://cloud.google.com/pubsub)

## 1.2 Select Data Format  
- [Single-select]  
  - [ ] JSON  
  - [ ] Parquet → https://parquet.apache.org/  
  - [ ] Protobuf → https://protobuf.dev/  
  - [ ] Avro → https://avro.apache.org/  
  - [ ] CSV  
  - [ ] XML  

## 1.3 Define Schema Contract  
- [Single-select]  
  - [ ] JSON Schema → https://json-schema.org/  
  - [ ] Avro Schema → https://avro.apache.org/docs/current/spec.html  
  - [ ] Protobuf `.proto` → https://protobuf.dev/  
  - [ ] Parquet schema  
  - [ ] DB schema extraction  

- [Multi-select]  
  - [ ] Request schema  
  - [ ] Response schema  
  - [ ] Event schema  
  - [ ] CDC change schema  

## 1.4 Define Semantic Meaning  
- [Multi-select]  
  - [ ] Field meanings  
  - [ ] Timestamp standards (ISO8601 → https://www.iso.org/iso-8601-date-and-time-format.html)  
  - [ ] Enum normalization  
  - [ ] Currency & units  
  - [ ] Reference data mappings  
  - [ ] Golden source identification  

## 1.5 Pre-Ingestion Validation  
- [Multi-select]  
  - [ ] Required fields  
  - [ ] Type validation  
  - [ ] Nullability  
  - [ ] Domain constraints  
  - [ ] Schema validation (Avro/Protobuf/JSON)  
  - [ ] Version compatibility  
  - [ ] Early anomaly detection  

---

# PHASE 2: INGEST (Data in Motion / Cloud Pipelines)

## 2.1 Ingestion Mechanism  
- [Single-select]  
  - [ ] API →
    - **AWS Lambda** https://docs.aws.amazon.com/lambda
    - **GCP Cloud Functions** https://cloud.google.com/functions  
  - [ ] Kafka → https://kafka.apache.org/  
  - [ ] Kinesis → https://aws.amazon.com/kinesis/  
  - [ ] Pub/Sub → https://cloud.google.com/pubsub  
  - [ ] File triggers (S3/GCS events)  
  - [ ] CDC (Debezium/DMS)  

## 2.2 Transport Controls  
- [Multi-select]  
  - [ ] Batch size  
  - [ ] Ordering guarantees → Kafka partitions  
  - [ ] Retry policy  
  - [ ] DLQ → https://aws.amazon.com/sqs/features/#Dead_Letter_Queues  
  - [ ] Backpressure management → https://nightlies.apache.org/flink/flink-docs-stable/  
  - [ ] Checkpointing → Flink / Spark Structured Streaming  

## 2.3 Parsing & Decoding  
- [Multi-select]  
  - [ ] JSON parsing  
  - [ ] CSV parsing  
  - [ ] Parquet reading  
  - [ ] Protobuf decoding  
  - [ ] Avro decoding  
  - [ ] Base64 decoding  
  - [ ] Timestamp normalization  

## 2.4 Initial Transformation  
- [Multi-select]  
  - [ ] Flatten nested JSON  
  - [ ] Extract arrays into child tables  
  - [ ] Drop unused fields  
  - [ ] Add ingestion metadata  
  - [ ] Lookup enrichment  
  - [ ] Hash/tokenize sensitive data  

## 2.5 Data Quality & Integrity Checks (In-Flight)  
- [Multi-select]  
  - [ ] Schema enforcement (Confluent Schema Registry → https://www.confluent.io/product/schema-registry/)  
  - [ ] Type matching  
  - [ ] Range checks  
  - [ ] Pattern checks  
  - [ ] Freshness checks  
  - [ ] Duplicate detection  
  - [ ] Quarantine routing (DLQ)  

---

# PHASE 3: PROCESS (ETL / ELT)

## 3.1 Choose Processing Model  
- [Single-select]  
  - [ ] ELT (dbt → https://www.getdbt.com/)  
  - [ ] ETL
    - Spark → https://spark.apache.org/
    - Dataflow → https://cloud.google.com/dataflow 
  - [ ] Streaming transformations (Flink → https://flink.apache.org/)  

## 3.2 Select Transformation Engine  
- [Single-select]  
  - [ ] dbt  
  - [ ] Spark / Databricks → https://www.databricks.com/  
  - [ ] Dataflow (GCP)  
  - [ ] Snowflake Tasks/Streams → https://docs.snowflake.com/  
  - [ ] BigQuery SQL models → https://cloud.google.com/bigquery/docs  

## 3.3 Apply Transformations  
- [Multi-select]  
  - [ ] Casting & normalization  
  - [ ] Joins & enrichment  
  - [ ] Bronze → Silver → Gold modeling (Delta Lake → https://delta.io/)  
  - [ ] Window functions  
  - [ ] Deduplication  
  - [ ] SCD Type 1/2/3  
  - [ ] Business logic transformation  

---

# PHASE 4: STORE (Warehouse / Lake / DB)

## 4.1 Select Storage Target  
- [Single-select]  
  - [ ] Data Lake
    - S3 → https://aws.amazon.com/s3/
    - GCS → https://cloud.google.com/storage
  - [ ] Data Warehouse
    - (Snowflake → https://snowflake.com/
    - BigQuery → https://cloud.google.com/bigquery
    - Redshift → https://aws.amazon.com/redshift/
  - [ ] OLTP DB (Postgres/MySQL)  
  - [ ] NoSQL
    - (DynamoDB → https://aws.amazon.com/dynamodb/
    - Firestore → https://cloud.google.com/firestore/

## 4.2 Model Target Schema  
- [Multi-select]  
  - [ ] Relational tables  
  - [ ] Parquet/Delta/Iceberg tables → https://iceberg.apache.org/  
  - [ ] Partition strategy  
  - [ ] Clustering/sorting keys  
  - [ ] Retention policy  
  - [ ] Indexing strategy  

## 4.3 Storage-Level Constraints  
- [Multi-select]  
  - [ ] NOT NULL  
  - [ ] UNIQUE  
  - [ ] CHECK  
  - [ ] Foreign keys  
  - [ ] Row-level security  
  - [ ] Data masking/tokenization  

## 4.4 Post-Load Validation  
- [Multi-select]  
  - [ ] dbt tests → https://docs.getdbt.com/docs/building-a-dbt-project/tests  
  - [ ] Great Expectations → https://greatexpectations.io/  
  - [ ] Row count checks  
  - [ ] Null % checks  
  - [ ] Freshness monitoring  
  - [ ] Schema drift detection (concept → https://databricks.com/glossary/schema-drift)  

---

# PHASE 5: SERVE & CONSUME

## 5.1 Serving Layers  
- [Multi-select]  
  - [ ] BI dashboards
    - Looker → https://looker.com/
    - PowerBI → https://powerbi.microsoft.com/
    - Tableau → https://www.tableau.com/
  - [ ] Reverse ETL
    - Hightouch → https://www.hightouch.com/
    - Census → https://www.getcensus.com/)
  - [ ] ML feature store (Feast → https://feast.dev/)  
  - [ ] Datamarts  
  - [ ] Redis cache → https://redis.io/  
  - [ ] Elasticsearch → https://www.elastic.co/elasticsearch/  

## 5.2 Consumption Controls  
- [Multi-select]  
  - [ ] RBAC  
  - [ ] Data contracts for downstream → https://martinfowler.com/articles/data-monolith-to-mesh.html#DataContracts  
  - [ ] API endpoints for curated tables  
  - [ ] RLS + CLS  

---

# PHASE 6: GOVERNANCE & OPERATIONS

## 6.1 Metadata & Lineage  
- [Multi-select]  
  - [ ] Data catalogs (DataHub → https://datahubproject.io/ , Amundsen → https://www.amundsen.io/)  
  - [ ] Lineage tracking (OpenLineage → https://openlineage.io/ , dbt docs)  
  - [ ] PII tagging  

## 6.2 Monitoring Systems  
- [Multi-select]  
  - [ ] Pipeline alerts  
  - [ ] Latency dashboards  
  - [ ] Volume anomaly detection  
  - [ ] Schema drift monitoring  
  - [ ] Downstream consumer SLA checks  

## 6.3 CI/CD & Versioning  
- [Multi-select]  
  - [ ] Git  
  - [ ] dbt CI/CD  
  - [ ] Data test automation  
  - [ ] Blue/green deployment  
  - [ ] Data SLAs  

---

# PHASE 7: EVOLUTION & IMPROVEMENT

## 7.1 Continuous Architecture Review  
- [Multi-select]  
  - [ ] Scaling limits  
  - [ ] Cost optimization  
  - [ ] Lake organization  
  - [ ] Table redesign  
  - [ ] Deprecation plans  

## 7.2 Future-Proofing  
- [Multi-select]  
  - [ ] Versioned schemas  
  - [ ] Backward/forward-compatible changes  
  - [ ] Canary pipelines  
  - [ ] Replay from raw layer  
