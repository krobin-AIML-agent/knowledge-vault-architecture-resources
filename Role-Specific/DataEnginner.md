**Role Context:** Data Engineer  
**Primary Focus:** Data pipelines, ETL/ELT systems, orchestration, storage, modeling  
**Daily Tasks:** Building pipelines, managing data flows, ensuring data quality & reliability  
**Output:** Production-grade data infrastructure (pipelines, warehouses, ingestion layers)

---

# MUST-HAVE (Primary): 80/20 Core

## 1. Python for Data Engineering  
**System Alignment:** Programming Languages → Data Ecosystem  
**Task Frequency:** Daily  

### Your 20%  
- **Pandas**: https://pandas.pydata.org/docs  
- **PySpark**: https://spark.apache.org/docs/latest/api/python  
- **SQLAlchemy**: https://docs.sqlalchemy.org  
- **Requests (APIs)**: https://docs.python-requests.org  
- **Typing / Pydantic**: https://docs.pydantic.dev  
- **Concurrency basics (multiprocessing/async)**: https://docs.python.org/3/library/asyncio.html  

### What You *Don't* Need  
- ML frameworks  
- Transformer architectures  
- Deep learning libraries  

### Pattern Alignment  
- Extract → Transform → Load  
- Batch vs streaming logic  
- Idempotent pipeline execution  

---

## 2. SQL Mastery  
**System Alignment:** Data Warehouses → Query Layer  
**Task Frequency:** Daily  

### Your 20%  
- **SELECT / JOIN / WHERE** basics  
- **Window functions**  
- **CTEs**  
- **Aggregation patterns**  
- **Partitions / clustering**  
- **Indexes**: https://www.postgresql.org/docs/current/indexes.html  

### Tools  
- **PostgreSQL**: https://www.postgresql.org/docs  
- **MySQL**: https://dev.mysql.com/doc  
- **Snowflake SQL**: https://docs.snowflake.com/en/sql-reference  
- **BigQuery SQL**: https://cloud.google.com/bigquery/docs/reference/standard-sql  

### What You *Don't* Need  
- Pure database administration  
- Advanced DB internals  

### Pattern Alignment  
- Filter → Aggregate → Merge  
- Windowed analytics  

---

## 3. ETL/ELT Pipelines  
**System Alignment:** Data Flow Layer → Ingestion & Processing  
**Task Frequency:** Daily  

### Your 20%  
- **Batch ingestion**  
- **CDC (Change Data Capture)** concepts  
- **Data validation**  
- **Schema mapping / normalization**  
- **File formats (Parquet, ORC, Avro)**  
  - Parquet: https://parquet.apache.org  
  - Avro: https://avro.apache.org  

### What You *Don't* Need  
- Proprietary ETL tool stacks  
- Heavy low-level C++ for compression  

### Pattern Alignment  
- Ingest → Validate → Transform → Persist  

---

## 4. Orchestration Systems  
**System Alignment:** Scheduling → Workflow Management  
**Task Frequency:** Daily  

### Your 20%  
- **Apache Airflow**: https://airflow.apache.org/docs  
- **Prefect**: https://docs.prefect.io  
- **Dagster**: https://docs.dagster.io  

Key concepts:  
- DAGs  
- Operators / tasks  
- Retries / backoff  
- Sensors  
- Task dependencies  

### What You *Don't* Need  
- Full Kubernetes cluster administration  

### Pattern Alignment  
- Directed Acyclic Graphs  
- Retry + recovery patterns  

---

## 5. Data Warehouses  
**System Alignment:** Storage → Analytical Layer  
**Task Frequency:** Daily  

### Your 20%  
- **Snowflake**: https://docs.snowflake.com  
- **BigQuery**: https://cloud.google.com/bigquery/docs  
- **Redshift**: https://docs.aws.amazon.com/redshift  
- **Delta Lake / Lakehouse**: https://docs.delta.io  

Skills:  
- Warehouse schemas (star, snowflake)  
- Partitioning / clustering  
- Cost optimization  

### What You *Don't* Need  
- Deep OLAP cube design history  

### Pattern Alignment  
- Query → Optimize → Persist  

---

## 6. Data Modeling  
**System Alignment:** Data Architecture → Schema Layer  
**Task Frequency:** Daily  

### Your 20%  
- **Kimball Dimensional Modeling**: https://www.kimballgroup.com  
- **Normalization (1NF → 3NF)**  
- **Slowly Changing Dimensions (SCD)**  
- **Entity-relationship modeling**  

### What You *Don't* Need  
- Extremely high-normalized academic schemas  

### Pattern Alignment  
- OLTP → OLAP transformation  
- Dimension + fact modeling  

---

# SHOULD-HAVE (Secondary)

## 7. Cloud Platforms  
### Your 20%  
- **AWS S3**: https://docs.aws.amazon.com/AmazonS3  
- **AWS Lambda**: https://docs.aws.amazon.com/lambda  
- **GCP Storage**: https://cloud.google.com/storage  
- **Azure Data Lake**: https://learn.microsoft.com/azure/storage  

Useful for:  
- event-driven ingestion  
- object storage  
- lightweight transformations  

---

## 8. Streaming Systems  
### Your 20%  
- **Kafka**: https://kafka.apache.org/documentation  
- **Kinesis**: https://docs.aws.amazon.com/kinesis  
- **Pub/Sub**: https://cloud.google.com/pubsub/docs  

Patterns:  
- producers / consumers  
- topics / partitions  
- message retention  
- low-latency processing  

---

## 9. Data Quality & Governance  
### Your 20%  
- **Great Expectations**: https://greatexpectations.io  
- **dbt tests**: https://docs.getdbt.com/docs/build/tests  
- Data contracts  
- Validation rules  
- Lineage tracking  

---

# COULD-HAVE (Tertiary)

## 10. Distributed Compute  
### Your 20%  
- **Apache Spark**: https://spark.apache.org/docs/latest  
- **Databricks**: https://docs.databricks.com  
- **Dask**: https://docs.dask.org  

Used for:  
- large-scale transformations  
- distributed dataframes  
- ML preprocessing at scale  

---

## 11. Containerization  
### Your 20%  
- **Docker**: https://docs.docker.com  
- **docker-compose**  

---

# WOULD-LIKE (Optional)

## 12. Advanced Data Architecture  
### Your 20%  
- Data mesh concepts  
- Event-driven architectures  
- Lakehouse optimization 
