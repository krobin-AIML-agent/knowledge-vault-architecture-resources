# DEVOPS & APP DEPLOYMENT MASTER WORKFLOW  
_Complete DevOps → Infra → Build → Deploy → Observe → Scale → Govern Pipeline_  
_Linked + Explained + Unified Version_

---

# PHASE 0: SCOPING (App + DevOps Context)

## 0.1 Define App Type (Single-select)
- [ ] Lovable → https://lovable.dev  
  - AI-generated full-stack apps.
- [ ] React → https://react.dev  
  - Frontend UI library.
- [ ] Next.js → https://nextjs.org  
  - Full-stack React framework.
- [ ] Vue → https://vuejs.org  
  - Lightweight web framework.
- [ ] Node.js → https://nodejs.org  
  - Backend JS runtime.
- [ ] Python → https://www.python.org  
  - API + automation language.
- [ ] Go → https://go.dev  
  - Fast backend microservices.

## 0.2 Deployment Requirement (Single-select)
- [ ] Serverless → https://aws.amazon.com/lambda/  
  - Zero-maintenance compute.
- [ ] Docker → https://www.docker.com  
  - Container runtime.
- [ ] Kubernetes → https://kubernetes.io  
  - Container orchestration.
- [ ] Static Hosting → https://vercel.com  
  - CDN-based frontend hosting.
- [ ] Hybrid  
  - Combination architectures.

## 0.3 Infrastructure Provider (Single-select)
- [ ] AWS → https://aws.amazon.com  
  - Full cloud stack.
- [ ] GCP → https://cloud.google.com  
  - Developer-friendly cloud.
- [ ] Azure → https://azure.microsoft.com  
  - Enterprise cloud.
- [ ] Vercel → https://vercel.com  
  - Next.js-first deployments.
- [ ] Netlify → https://netlify.com  
  - Jamstack + serverless.
- [ ] Fly.io → https://fly.io  
  - Global low-latency apps.
- [ ] Railway → https://railway.app  
  - Instant apps + DBs.

---

# PHASE 1: PREPARATION (Before Deployment)

## 1.1 Code Management (Multi-select)
- [ ] Git → https://git-scm.com  
  - Version control.
- [ ] GitHub → https://github.com  
  - Repo hosting + workflows.
- [ ] GitLab → https://gitlab.com  
  - All-in-one DevOps.

## 1.2 Environment Setup

### Environment Selection (Single-select)
- [ ] Dev only  
  - Single environment.
- [ ] Dev + Staging  
  - Pre-production layer.
- [ ] Dev + Staging + Prod  
  - Full pipeline.

### Config & Secrets (Multi-select)
- [ ] dotenv → https://github.com/motdotla/dotenv  
  - Local env variables.
- [ ] AWS Secrets Manager → https://aws.amazon.com/secrets-manager  
  - Managed secret store.
- [ ] GCP Secret Manager → https://cloud.google.com/secret-manager  
  - GCP equivalent.

## 1.3 Architecture Definition (Multi-select)
- [ ] Express → https://expressjs.com  
  - Node.js API framework.
- [ ] FastAPI → https://fastapi.tiangolo.com  
  - Python high-speed API.
- [ ] Django → https://www.djangoproject.com  
  - Full Python framework.
- [ ] PostgreSQL → https://postgresql.org  
  - SQL relational database.
- [ ] MySQL → https://mysql.com  
  - Open-source SQL DB.
- [ ] MongoDB → https://mongodb.com  
  - NoSQL document DB.
- [ ] Redis → https://redis.io  
  - Cache + queues.
- [ ] S3 → https://aws.amazon.com/s3  
  - Object storage.
- [ ] Cloud Storage → https://cloud.google.com/storage  
  - Google object storage.
- [ ] CI/CD Pipelines (GitHub Actions) → https://github.com/features/actions  
  - Automation framework.
- [ ] Monitoring (Grafana/Datadog)  
  - Observability stack.

---

# PHASE 2: INFRASTRUCTURE PROVISIONING

## 2.1 IaC Selection (Single-select)
- [ ] Terraform → https://terraform.io  
  - Declarative infra.
- [ ] Pulumi → https://pulumi.com  
  - Infra using real code.
- [ ] AWS CDK → https://aws.amazon.com/cdk  
  - AWS-native IaC.
- [ ] Manual provisioning  
  - Click-ops.

## 2.2 Provision Core Resources (Multi-select)

### Compute
- [ ] AWS Lambda → https://aws.amazon.com/lambda  
  - Serverless compute.
- [ ] EC2 → https://aws.amazon.com/ec2  
  - Virtual servers.
- [ ] Cloud Run → https://cloud.google.com/run  
  - Serverless containers.
- [ ] Kubernetes → https://kubernetes.io  
  - Container orchestration.

### Networking
- [ ] VPC → https://aws.amazon.com/vpc  
  - Network isolation.
- [ ] Load Balancer → https://aws.amazon.com/elasticloadbalancing  
  - Traffic distribution.
- [ ] API Gateway → https://aws.amazon.com/api-gateway  
  - Public API router.
- [ ] Cloudflare → https://cloudflare.com  
  - Security + proxy + CDN.

### Storage
- [ ] S3 → https://aws.amazon.com/s3  
  - Blob storage.
- [ ] Google Cloud Storage → https://cloud.google.com/storage  
  - GCP equivalent.

### Databases
- [ ] RDS → https://aws.amazon.com/rds  
  - Managed SQL.
- [ ] Cloud SQL → https://cloud.google.com/sql  
  - GCP managed SQL.
- [ ] DynamoDB → https://aws.amazon.com/dynamodb  
  - NoSQL KV store.
- [ ] Firestore → https://cloud.google.com/firestore  
  - NoSQL document DB.

### Secrets
- [ ] AWS Secrets Manager → https://aws.amazon.com/secrets-manager  
  - Secure secret store.
- [ ] GCP Secret Manager → https://cloud.google.com/secret-manager  
  - GCP equivalent.

---

# PHASE 3: BUILD & PACKAGE

## 3.1 Build System (Multi-select)
- [ ] npm → https://npmjs.com  
  - JS build runner.
- [ ] pnpm → https://pnpm.io  
  - Fast JS package manager.
- [ ] yarn → https://yarnpkg.com  
  - JS dependency tool.
- [ ] pip (Python) → https://pip.pypa.io  
  - Python dependency manager.
- [ ] Maven → https://maven.apache.org  
  - Java build tool.
- [ ] Gradle → https://gradle.org  
  - JVM build automation.

## 3.2 Containerization (Single-select)
- [ ] Dockerfile → https://docs.docker.com/engine/reference/builder  
  - Container build recipe.
- [ ] Buildpacks → https://buildpacks.io  
  - Automated container builder.
- [ ] No containers  
  - Skip.

## 3.3 Artifact Storage (Multi-select)
- [ ] GitHub Packages → https://github.com/features/packages  
  - Container + artifact registry.
- [ ] Docker Hub → https://hub.docker.com  
  - Public container registry.
- [ ] AWS ECR → https://aws.amazon.com/ecr  
  - AWS container registry.
- [ ] Artifact Registry → https://cloud.google.com/artifact-registry  
  - GCP container registry.

---

# PHASE 4: CI/CD PIPELINE

## 4.1 CI/CD Platform (Single-select)
- [ ] GitHub Actions → https://github.com/features/actions  
  - CI/CD automation.
- [ ] GitLab CI → https://docs.gitlab.com/ee/ci  
  - GitLab DevOps.
- [ ] CircleCI → https://circleci.com  
  - Hosted CI.
- [ ] Jenkins → https://jenkins.io  
  - Self-hosted CI.
- [ ] ArgoCD → https://argo-cd.readthedocs.io  
  - GitOps for Kubernetes.

## 4.2 CI Checks (Multi-select)
- [ ] Jest → https://jestjs.io  
  - JS testing.
- [ ] PyTest → https://pytest.org  
  - Python testing.
- [ ] Snyk → https://snyk.io  
  - Security scanning.

## 4.3 Deployment Strategies (Multi-select)
- [ ] Blue/Green → https://martinfowler.com/bliki/BlueGreenDeployment.html  
  - Zero-downtime swap.
- [ ] Canary → https://martinfowler.com/bliki/CanaryRelease.html  
  - Slow rollout.
- [ ] Manual approvals  
  - Human gating.

---

# PHASE 5: DEPLOYMENT EXECUTION

## 5.1 Deployment Targets (Single-select)
- [ ] Vercel → https://vercel.com  
  - Frontend hosting.
- [ ] Netlify → https://netlify.com  
  - Static + serverless.
- [ ] AWS ECS → https://aws.amazon.com/ecs  
  - Managed containers.
- [ ] AWS Lambda → https://aws.amazon.com/lambda  
  - Serverless.
- [ ] Cloud Run → https://cloud.google.com/run  
  - Serverless containers.

## 5.2 Routing & Load Balancing (Multi-select)
- [ ] Nginx → https://nginx.org  
  - Reverse proxy.
- [ ] Traefik → https://traefik.io  
  - Dynamic router.
- [ ] Cloudflare → https://cloudflare.com  
  - CDN + DNS + WAF.

## 5.3 Database Migrations (Multi-select)
- [ ] Prisma → https://prisma.io  
  - DB schema migrations.
- [ ] Flyway → https://flywaydb.org  
  - Versioned SQL.
- [ ] Liquibase → https://liquibase.org  
  - DB change automation.

---

# PHASE 6: OBSERVABILITY & MONITORING

## 6.1 Logging (Multi-select)
- [ ] CloudWatch → https://aws.amazon.com/cloudwatch  
  - AWS logs.
- [ ] GCP Logging → https://cloud.google.com/logging  
  - GCP logs.
- [ ] Loki → https://grafana.com/oss/loki  
  - Log aggregation.

## 6.2 Monitoring (Multi-select)
- [ ] Prometheus → https://prometheus.io  
  - Metrics collection.
- [ ] Grafana → https://grafana.com  
  - Metrics visualization.
- [ ] Datadog → https://datadoghq.com  
  - Full observability suite.

## 6.3 Alerts (Multi-select)
- [ ] PagerDuty → https://pagerduty.com  
  - Incident alerts.
- [ ] Opsgenie → https://www.atlassian.com/software/opsgenie  
  - On-call rotations.

---

# PHASE 7: SECURITY & COMPLIANCE

## 7.1 Infrastructure Security (Multi-select)
- [ ] AWS WAF → https://aws.amazon.com/waf  
  - Traffic filtering.
- [ ] Cloud Armor → https://cloud.google.com/armor  
  - GCP WAF.
- [ ] IAM → https://aws.amazon.com/iam  
  - Identity access mgmt.
- [ ] Azure AD → https://azure.microsoft.com/services/active-directory  
  - Azure identity.
- [ ] GCP IAM → https://cloud.google.com/iam  
  - GCP roles & access.

## 7.2 Application Security (Multi-select)
- [ ] JWT → https://jwt.io  
  - Token auth.
- [ ] OAuth2 → https://oauth.net/2  
  - Authorization flow.
- [ ] Auth0 → https://auth0.com  
  - Managed identity.
- [ ] OWASP Top 10 → https://owasp.org/www-project-top-ten  
  - Security risks list.
- [ ] Rate limiting (Cloudflare) → https://developers.cloudflare.com/waf/rate-limiting/  
  - Prevent abuse.
- [ ] Validator.js → https://github.com/validatorjs/validator.js  
  - Input sanitization.

---

# PHASE 8: SCALING & PERFORMANCE

## 8.1 Scaling Strategies (Multi-select)
- [ ] AWS Auto Scaling → https://aws.amazon.com/autoscaling  
  - Automatic capacity.
- [ ] Kubernetes HPA → https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale  
  - Pod scaling.
- [ ] CloudFront CDN → https://aws.amazon.com/cloudfront  
  - AWS edge caching.
- [ ] Cloudflare CDN → https://cloudflare.com/cdn  
  - Global caching.

## 8.2 Performance Tools (Multi-select)
- [ ] Redis → https://redis.io  
  - Cache + session store.
- [ ] RabbitMQ → https://rabbitmq.com  
  - Async queues.
- [ ] Kafka → https://kafka.apache.org  
  - Event streaming.
- [ ] Nginx → https://nginx.org  
  - High-perf proxy.
- [ ] HAProxy → https://haproxy.org  
  - Enterprise load balancer.

---

# PHASE 9: GOVERNANCE & CONTINUOUS IMPROVEMENT

## 9.1 Governance Tools (Multi-select)
- [ ] Backstage → https://backstage.io  
  - Developer portal.
- [ ] Atlantis → https://runatlantis.io  
  - Terraform automation.
- [ ] OPA → https://openpolicyagent.org  
  - Policy-as-code.
- [ ] ArgoCD → https://argo-cd.readthedocs.io  
  - GitOps management.

## 9.2 Processes & Ops (Multi-select)
- [ ] Postmortems → https://sre.google/sre-book/postmortem  
  - RCA after incidents.
- [ ] Retrospectives → https://retrospectivewiki.org  
  - Process feedback.
- [ ] Cost reviews → https://aws.amazon.com/aws-cost-management  
  - Budget + savings.
- [ ] SLO/SLA Tracking → https://sre.google/sre-book/service-level-objectives  
  - Reliability goals.
- [ ] PagerDuty IR → https://pagerduty.com  
  - Incident response.

---

# FINAL SUMMARY
This is the **complete unified DevOps master workflow**, including:

- Scoping  
- Infra provisioning  
- Build pipelines  
- Deployment  
- Routing  
- Observability  
- Security  
- Scaling  
- Governance 
- Security  
- Scaling  
- Governance 
