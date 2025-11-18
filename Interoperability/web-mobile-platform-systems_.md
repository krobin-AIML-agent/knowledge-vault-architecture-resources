# web/mobile/platform systems Components

## 1. Authentication / Authorization (AuthN / AuthZ)
Ensures identity (AuthN) and permissions (AuthZ).

**Official References**
- OAuth2: https://oauth.net/2/
- OpenID Connect: https://openid.net/connect/
- JWT (JSON Web Tokens): https://jwt.io/introduction
- API Keys (RFC 6750): https://datatracker.ietf.org/doc/html/rfc6750

---

## 2. Rate Limits
Protects systems from abuse, spikes, and overload.

**Official References**
- Cloudflare rate limiting: https://developers.cloudflare.com/rate-limits/
- AWS API Gateway throttling: https://docs.aws.amazon.com/apigateway/latest/developerguide/api-gateway-request-throttling.html
- Netflix Hystrix / fault tolerance: https://github.com/Netflix/Hystrix
- Circuit Breaker pattern: https://martinfowler.com/bliki/CircuitBreaker.html

---

## 3. Gateway / Proxy
Handles routing, security, logging, normalization.

**Official References**
- NGINX reverse proxy: https://nginx.org/en/docs/
- Envoy Proxy (Service mesh standard): https://www.envoyproxy.io/docs
- AWS API Gateway: https://aws.amazon.com/api-gateway/
- Cloudflare reverse proxy: https://www.cloudflare.com/learning/cdn/glossary/reverse-proxy/

---

## 4. ORM / Mapping Layer
Maps objects → database rows/documents.

**Official References**
- Prisma: https://www.prisma.io/docs
- SQLAlchemy (Python): https://docs.sqlalchemy.org
- Hibernate (Java): https://hibernate.org/orm/
- ActiveRecord (Rails): https://guides.rubyonrails.org/active_record_basics.html

---

## 5. Transaction Boundary
Defines atomic units of work: begin, commit, rollback.

**Official References**
- Database transactions (Wikipedia summary): https://en.wikipedia.org/wiki/Database_transaction
- Postgres transaction docs: https://www.postgresql.org/docs/current/tutorial-transactions.html
- ACID overview: https://en.wikipedia.org/wiki/ACID
- Isolation levels: https://www.postgresql.org/docs/current/transaction-iso.html

---

## 6. Indexing / Constraints
Ensures performance + data integrity.

**Official References**
- Postgres indexing: https://www.postgresql.org/docs/current/indexes.html
- MySQL indexing: https://dev.mysql.com/doc/refman/8.0/en/mysql-indexes.html
- Constraints (PK, FK, unique): https://www.postgresql.org/docs/current/ddl-constraints.html
- Partitioning: https://www.postgresql.org/docs/current/ddl-partitioning.html

---

## 7. Caching Layer
Improves read speed and reduces DB load.

**Official References**
- Redis documentation: https://redis.io/docs
- Memcached: https://memcached.org/
- Application caching patterns: https://martinfowler.com/bliki/Cache.html
- CDNs as cache layers (Cloudflare): https://www.cloudflare.com/learning/cdn/what-is-a-cdn/
