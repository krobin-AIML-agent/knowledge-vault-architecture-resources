# Full DBA Scope (SQL + Database Administration)

The following is the complete domain of a professional SQL DBA.  
Each item from the original list is retained exactly, with clear explanations added.

---

# 1. Database Architecture & Design

## 1.1 Data Modeling  
Designing how data is structured before it enters the database.  
Includes creating conceptual, logical, and physical models to ensure data is stored efficiently, relationships are clear, and queries remain fast.

## 1.2 ER Diagrams  
Entity-Relationship diagrams visually represent tables, relationships, and constraints.  
This ensures teams understand how data interacts across the system.

## 1.3 Normalization (1NF → 5NF)  
The process of organizing data to reduce redundancy and improve integrity.  
Higher forms of normalization solve specific issues like duplicate data, update anomalies, and relationship complexity.

## 1.4 Denormalization (OLAP vs OLTP)  
In analytics systems (OLAP), denormalization speeds up reads.  
In transactional systems (OLTP), normalized design supports fast writes and integrity.

## 1.5 Star / Snowflake Schemas  
Used in data warehouses:  
- **Star schema** → fewer joins, simpler  
- **Snowflake schema** → normalized dimensions to reduce storage

## 1.6 Storage Architecture  
Understanding how the DB engine stores data:  
Pages → Extents → Segments → Tablespaces  
DBAs must tune storage for performance and reliability.

## 1.7 WAL / Redo / Undo Logs  
WAL = Write-Ahead Log.  
All changes are written to log first, which ensures crash recovery and durability.

## 1.8 Indexes (B-tree, Hash, Bitmap)  
Indexes speed up reads but add overhead to writes.  
DBAs choose proper index types based on query patterns.

## 1.9 Clustered vs Non-Clustered Indexes  
- **Clustered:** table is physically ordered by the index  
- **Non-clustered:** independent index structure  

---

# 2. Database Operations & Administration

## 2.1 Installation & Configuration  
Installing PostgreSQL, SQL Server, MySQL, Oracle, etc.  
Includes configuring memory, CPU settings, autovacuum, caching, file locations.

## 2.2 Parameter Tuning  
Adjusting DB-level parameters to optimize performance and reliability.  
Example: `shared_buffers`, `work_mem`, `max_connections`.

## 2.3 User & Role Management  
DBA manages permissions:  
- logins  
- roles  
- least-privilege access  
- auditing of who can read/write sensitive data

## 2.4 Privilege Hierarchies  
Structured permission levels ensure strong security.  
E.g., superuser → admin → writer → reader.

## 2.5 Environment Management  
Keeping DEV / QA / STAGE / PROD databases synchronized.  
Includes managing schema differences and promoting changes properly.

## 2.6 Data Masking in Non-Prod  
Production data must be masked when copied into dev systems for privacy and compliance.

## 2.7 Job Scheduling & Automation  
DBA uses tools like SQL Agent or cron to run daily tasks:  
- cleanup jobs  
- index maintenance  
- automated backups  
- ETL kickoff scripts

---

# 3. Backup, Recovery, High Availability (HA/DR)

## 3.1 Backup Strategies  
Different backup methods used for balancing performance, cost, and recovery speed.  
Full, differential, incremental, binary log backups.

## 3.2 PITR (Point-in-Time Recovery)  
Restoring the database to a specific timestamp by replaying WAL/redo logs.  
Critical for disaster recovery.

## 3.3 Restore Procedures  
DBAs must test and document restore procedures regularly.  
A backup that can't be restored is a failed backup.

## 3.4 High Availability  
Ensuring databases stay running even if servers fail:  
- streaming replication  
- clustering  
- synchronous vs asynchronous replication

## 3.5 Replication (Logical / Physical)  
Physical = block-level replication.  
Logical = table-level replication, flexible for migrations.

## 3.6 AlwaysOn Availability Groups (SQL Server)  
Microsoft’s enterprise HA solution enabling multiple secondary replicas.

## 3.7 Disaster Recovery  
Designing failover plans, multi-region replication, and DR runbooks covering what to do if the entire environment fails.

---

# 4. Performance Tuning & Query Optimization

## 4.1 Query Performance  
Using EXPLAIN plans to diagnose slow queries, identify bad joins, inefficient filters, and missing indexes.

## 4.2 Join Strategies  
Understanding nested loops, hash joins, merge joins, and when each is chosen by the optimizer.

## 4.3 Avoid Full Table Scans  
Whenever possible, DBAs ensure queries use indexes instead of scanning the entire table.

## 4.4 Index Optimization  
Regularly removing unused indexes, rebuilding fragmented indexes, and identifying missing indexes.

## 4.5 Server Performance Monitoring  
Watching CPU, memory, disk I/O, and network to catch bottlenecks.

## 4.6 Locking / Blocking  
Detecting sessions that block others and cause deadlocks.  
DBAs investigate lock types and transaction isolation levels.

## 4.7 Partitioning  
Splitting tables into smaller physical chunks for performance and maintenance efficiency.

## 4.8 Storage Optimization  
Designing retention policies, archive tables, hot/cold segmentation.

---

# 5. Security, Compliance, Governance

## 5.1 Encryption  
Encrypting data at rest and in transit to protect sensitive data.

## 5.2 TDE (Transparent Data Encryption)  
Automatically encrypts database files and logs.

## 5.3 SSL/TLS  
Ensures encrypted connections between apps and database servers.

## 5.4 SOC2, HIPAA, PCI, GDPR  
DBAs execute controls for industries requiring strict compliance.

## 5.5 Auditing  
Tracking data access, failed logins, user activity.

## 5.6 Row-Level Security (RLS)  
Restricting rows returned to certain users.

## 5.7 Column-Level Security  
Masking or restricting sensitive columns (SSN, DOB, etc.)

## 5.8 Data Classification  
Labeling sensitive fields correctly for governance and compliance.

---

# 6. SQL Mastery (Core Querying)

## 6.1 SQL Fundamentals  
SELECT, JOIN, GROUP BY, window functions.

## 6.2 CTEs & Recursive Queries  
Used for hierarchical data and complex transformations.

## 6.3 Transactions & ACID  
Guaranteeing atomic commits and consistent data.

## 6.4 Isolation Levels  
Understanding read phenomena:  
dirty reads, phantom reads, non-repeatable reads.

## 6.5 Stored Procedures & Triggers  
Encapsulated logic within the database engine.

---

# 7. Infrastructure & Cloud DB Management

## 7.1 AWS  
Using RDS, Aurora, Redshift for managed DB environments.

## 7.2 GCP  
Cloud SQL, Spanner (globally consistent DB).

## 7.3 Azure  
Azure SQL + CosmosDB.

## 7.4 Kubernetes for Databases  
Using StatefulSets and Operators to manage DBs in distributed clusters.

---

# 8. Tools, Monitoring & Observability

## 8.1 Monitoring Tools  
pgAdmin, Datadog, Prometheus, Grafana.

## 8.2 DB Tools  
pgBouncer (connection pooling), SQL Workbench, SSMS.

## 8.3 Alerts  
Replication lag, long-running queries, storage full, high latency.

---

# 9. Advanced Concepts (Senior DBA)

## 9.1 Scaling Strategies  
Vertical (bigger server) vs horizontal (more nodes).

## 9.2 Distributed Databases  
CockroachDB, YugabyteDB, Vitess.

## 9.3 Multi-Tenancy  
Shared vs isolated architectures for SaaS products.

## 9.4 CDC (Change Data Capture)  
Real-time propagation of DB changes to other systems.

---

# 10. DBA On-Call Responsibilities

## 10.1 Typical Alerts  
Deadlocks, blocking sessions, replication failures, backup failures, storage emergencies.

DBA acts as the **SRE of the data layer**.
