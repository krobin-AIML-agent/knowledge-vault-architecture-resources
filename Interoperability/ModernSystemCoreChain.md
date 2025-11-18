# Modern System Core Chain

This guide explains the 12 core layers found in all modern backend systems,
what each layer is applicable to, who uses it, and when.

---

# Table of Contents
1. [API Interface](#1-api-interface)
2. [Data Format](#2-data-format)
3. [Serialization](#3-serialization)
4. [Transport](#4-transport)
5. [Request Parsing](#5-request-parsing)
6. [Request Validation](#6-request-validation)
7. [Type Normalization](#7-type-normalization)
8. [Schema Compliance](#8-schema-compliance)
9. [Semantic Validation](#9-semantic-validation)
10. [Business Logic](#10-business-logic)
11. [Persistence](#11-persistence)
12. [Database Storage Model](#12-database-storage-model)
13. [Modern Examples](#modern-system-core-chain-with-real-modern-examples)

---

# 1. API Interface
**Official References**
- REST: https://restfulapi.net  
- GraphQL: https://graphql.org/learn  
- OpenAPI/Swagger: https://swagger.io/specification  

---

# 2. Data Format
**Official References**
- JSON: https://www.json.org  
- XML: https://www.w3.org/XML  
- Protobuf: https://protobuf.dev  
- Avro: https://avro.apache.org/docs/current  
- CSV spec: https://tools.ietf.org/html/rfc4180  
- Multipart: https://www.rfc-editor.org/rfc/rfc2388  

---

# 3. Serialization
**Official References**
- UTF-8: https://www.ietf.org/rfc/rfc3629.txt  
- Base64: https://www.rfc-editor.org/rfc/rfc4648  
- MessagePack: https://msgpack.org  
- CBOR: https://cbor.io  

---

# 4. Transport
**Official References**
- HTTP/1.1: https://www.rfc-editor.org/rfc/rfc2616  
- HTTP/2: https://http2.github.io  
- HTTP/3 (QUIC): https://www.rfc-editor.org/rfc/rfc9000  
- WebSockets: https://www.rfc-editor.org/rfc/rfc6455  
- gRPC: https://grpc.io/docs/what-is-grpc/core-concepts  
- MQTT: https://mqtt.org  

---

# 5. Request Parsing
**Official References**
- JSON parsing: https://www.json.org/json-en.html  
- Protobuf decoding: https://protobuf.dev/programming-guides/  
- Multipart forms: https://www.rfc-editor.org/rfc/rfc7578  

---

# 6. Request Validation
**Official References**
- OWASP Input Validation: https://owasp.org/www-community/controls/Input_Validation_Cheat_Sheet  
- JSON Schema validation: https://json-schema.org/learn  

---

# 7. Type Normalization
**Official References**
- ECMAScript Type Conversion: https://262.ecma-international.org/#sec-ecmascript-language-types  
- RFC3339 datetime: https://www.rfc-editor.org/rfc/rfc3339  

---

# 8. Schema Compliance
**Official References**
- JSON Schema: https://json-schema.org  
- Protobuf Schema: https://protobuf.dev/programming-guides/proto3  
- XML Schema (XSD): https://www.w3.org/XML/Schema  

---

# 9. Semantic Validation
**Official References**
- ISO 8601 date semantics: https://www.iso.org/standard/70907.html  
- OWASP Data Validation: https://owasp.org/www-project-cheat-sheets/  

---

# 10. Business Logic
**Official References**
- Domain Driven Design: https://www.domainlanguage.com/ddd  
- Business Rules Patterns: https://martinfowler.com/bliki/BusinessRules.html  

---

# 11. Persistence
**Official References**
- SQL Standard (ISO 9075): https://www.iso.org/standard/73065.html  
- MongoDB CRUD: https://www.mongodb.com/docs/manual/crud  
- DynamoDB CRUD: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/WorkingWithItems.html  
- ACID: https://en.wikipedia.org/wiki/ACID  

---

# 12. Database Storage Model
**Official References**
- PostgreSQL Storage: https://www.postgresql.org/docs/current/storage.html  
- MongoDB Document Model: https://www.mongodb.com/docs/manual/core/document  
- DynamoDB Key-Value Design: https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.CoreComponents.html  
- ClickHouse Storage: https://clickhouse.com/docs/en/architecture/storage  
- BigQuery Storage: https://cloud.google.com/bigquery/docs/storage-overview  

---

# Modern System Core Chain: With Real Modern Examples

## 1. API Interface: Modern Examples
- Stripe REST API  
- Shopify REST & GraphQL APIs  
- Google Cloud gRPC APIs  
- AWS API Gateway → Lambda  

---

## 2. Data Format: Modern Examples
- JSON (all mobile & web backends)  
- Protobuf (Uber, Google, Lyft microservices)  
- Avro (Kafka & Confluent Platform)  
- Multipart uploads (YouTube, Instagram)  
- CSV ingestion (Snowflake, BigQuery)

---

## 3. Serialization: Modern Examples
- UTF-8 JSON (Slack, Twitter/X)  
- Protobuf binary (gRPC systems)  
- Base64 (S3 uploads)  
- MessagePack (Redis Streams)  
- CBOR (IoT devices, embedded systems)

---

## 4. Transport: Modern Examples
- HTTP/1.1 (Most REST APIs)  
- HTTP/2 (gRPC microservices)  
- HTTP/3 (Cloudflare, Google)  
- WebSockets (Discord, Slack RTM)  
- MQTT (AWS IoT, Azure IoT Hub)  
- gRPC streaming (Netflix, DoorDash)  

---

## 5. Request Parsing: Modern Examples
- Express.js body parser  
- FastAPI Pydantic parsing  
- Spring Boot Jackson JSON parser  
- Protobuf unmarshal in gRPC  
- AWS Lambda multipart decoding  

---

## 6. Request Validation: Modern Examples
- Pydantic models in FastAPI  
- Django model validation  
- Spring Boot Bean Validation  
- JSON Schema in Cloudflare Workers  
- API Gateway request validation  

---

## 7. Type Normalization: Modern Examples
- `"42"` → int in Node/Express  
- `"true"` → boolean in React Native backends  
- `"2025-01-01T00:00Z"` → timestamp in Airbnb/Uber services  
- Float conversion in Stripe/Shopify billing  

---

## 8. Schema Compliance: Modern Examples
- Protobuf enforcement (Google, Uber)  
- JSON Schema in Kafka Connect  
- SQL schema checks (Postgres/MySQL)  
- DTO validation in NestJS/Spring  

---

## 9. Semantic Validation: Modern Examples
- Date logic in Google Calendar API  
- Inventory logic in Shopify Stores  
- Financial constraints in Stripe/Plaid  
- Capacity validation in Airbnb  

---

## 10. Business Logic: Modern Examples
- Uber surge pricing  
- Amazon Prime shipping rules  
- Netflix recommendations engine  
- Stripe fraud detection (Radar)  

---

## 11. Persistence: Modern Examples
- Postgres writes (Instagram, Airbnb)  
- MySQL writes (Facebook, Uber)  
- DynamoDB writes (serverless apps)  
- MongoDB (e-commerce catalogs)  
- ORM commits (Prisma, Hibernate, SQLAlchemy)

---

## 12. Database Storage Model: Modern Examples
- Relational (Airbnb: Postgres; Facebook: MySQL)  
- Document (Mongo for product catalogs)  
- Key-value (Redis at Twitter/X; DynamoDB at Amazon)  
- Columnar (BigQuery at Google; Snowflake in enterprises)  
- Time-series (InfluxDB, TimescaleDB for IoT)
