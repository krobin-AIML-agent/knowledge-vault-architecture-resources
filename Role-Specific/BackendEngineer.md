**Role Context:** Back-End Engineer  
**Primary Focus:** APIs, databases, services, authentication, business logic  
**Daily Tasks:** Designing APIs, building services, managing data flows, optimizing performance  
**Output:** Scalable back-end systems (APIs, microservices, services, integrations)

---

# MUST-HAVE (Primary): 80/20 Core

## 1. Core Back-End Languages  
**System Alignment:** Execution Layer → Service Architecture  
**Task Frequency:** Daily  

### Your 20%  
- **Python** (FastAPI, Flask): https://www.python.org  
- **Node.js** (Express/Fastify): https://nodejs.org  
- **Go** (High-performance services): https://go.dev/doc/  

Pick 1 primary + 1 secondary.  

### What You *Don't* Need  
- Advanced language internals  
- Metaprogramming  

### Pattern Alignment  
- Request → Process → Respond  
- Stateless execution  

---

## 2. API Development  
**System Alignment:** API Layer → Service Delivery  
**Task Frequency:** Daily  

### Your 20%  
- **FastAPI**: https://fastapi.tiangolo.com  
- **Express (Node)**: https://expressjs.com  
- REST conventions  
- CRUD architecture  
- Pagination patterns  
- Error handling & middleware  

### What You *Don't* Need  
- GraphQL complexity (unless required)  
- Custom networking stacks  

### Pattern Alignment  
- Endpoint → Handler → Response  
- Validation → Error → Retry  

---

## 3. Databases (SQL & NoSQL)  
**System Alignment:** Storage Layer → Persistence  
**Task Frequency:** Daily  

### Your 20%  
- **PostgreSQL**: https://www.postgresql.org/docs  
- **MySQL**: https://dev.mysql.com/doc  
- **MongoDB**: https://www.mongodb.com/docs  
- ORMs (SQLAlchemy / Prisma / TypeORM)  
- Indexing basics  
- Transactions  

### What You *Don't* Need  
- Deep query planner internals  
- Full DBA skills  

### Pattern Alignment  
- Query → Transform → Persist  
- Index tuning → Performance → Scaling  

---

## 4. Authentication & Authorization  
**System Alignment:** Security Layer → Identity  
**Task Frequency:** Daily  

### Your 20%  
- **JWT** (JSON Web Tokens): https://jwt.io  
- OAuth2 (overview): https://oauth.net/2/  
- Role-based access control  
- Session management  
- Password hashing (bcrypt): https://github.com/pyca/bcrypt  

### What You *Don't* Need  
- Custom crypto algorithms  

### Pattern Alignment  
- Verify → Authorize → Allow/Deny  

---

## 5. Caching & Performance  
**System Alignment:** Optimization Layer → Low Latency  
**Task Frequency:** Daily  

### Your 20%  
- **Redis**: https://redis.io/docs  
- TTLs & invalidation  
- Query caching  
- Response caching  
- Async task queues (Redis Queue, BullMQ)  

### What You *Don't* Need  
- Distributed cache cluster tuning  

### Pattern Alignment  
- Cache → Serve → Refresh  

---

## 6. Testing & Reliability  
**System Alignment:** Quality Layer → Stability  
**Task Frequency:** Daily  

### Your 20%  
- Unit tests  
- Integration tests  
- **PyTest**: https://docs.pytest.org  
- **Jest** (Node): https://jestjs.io  
- Mocking dependencies  
- API contract testing  

### What You *Don't* Need  
- Full enterprise QA pipelines  

### Pattern Alignment  
- Arrange → Act → Assert  
- Mock → Test → Validate  

---

# SHOULD-HAVE (Secondary)

## 7. Containerization & Deployment  
### Your 20%  
- **Docker**: https://docs.docker.com  
- Docker Compose  
- Basic CI/CD familiarity  
- Environment variables + secrets  

---

## 8. Messaging & Asynchronous Architectures  
### Your 20%  
- **RabbitMQ**: https://www.rabbitmq.com/docs  
- **Kafka**: https://kafka.apache.org/documentation  
- Pub/Sub basics  
- Event-driven communication  

---

## 9. Cloud Providers  
### Your 20%  
- **AWS (Lambda, ECS, RDS)**: https://docs.aws.amazon.com  
- **GCP (Cloud Run, SQL)**: https://cloud.google.com/docs  
- **Azure App Services**: https://learn.microsoft.com/azure/  

---

# COULD-HAVE (Tertiary)

## 10. Microservices Architecture  
### Your 20%  
- Service boundaries  
- API gateways  
- Circuit breakers  
- Distributed tracing  

---

## 11. GraphQL  
### Your 20%  
- Queries, mutations, resolvers  
- Apollo Server  

---

# WOULD-LIKE (Optional)

## 12. Advanced Back-End Concepts  
### Your 20%  
- DDD (Domain-Driven Design)  
- CQRS  
- Event sourcing  
- High-performance Go service
