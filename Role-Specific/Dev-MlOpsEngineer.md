**Role Context:** DevOps / MLOps Engineer  
**Primary Focus:** CI/CD, deployment pipelines, infrastructure automation, ML model serving  
**Daily Tasks:** Managing cloud infra, containerization, orchestrating training/serving pipelines, monitoring  
**Output:** Reliable, scalable, automated systems for code + data + model deployment

---

# MUST-HAVE (Primary): 80/20 Core

## 1. Linux & Command Line  
**System Alignment:** Execution Environment → OS Layer  
**Task Frequency:** Daily  

### Your 20%  
- Basic shell commands  
- File permissions  
- Process management  
- System logs  
- Package management (apt/yum)  

### Docs  
- **Linux Basics**: https://ubuntu.com/tutorials/command-line-for-beginners  

### What You *Don't* Need  
- Kernel engineering  

### Pattern Alignment  
- Inspect → Modify → Execute  

---

## 2. GitOps & CI/CD  
**System Alignment:** Delivery Pipeline → Automation  
**Task Frequency:** Daily  

### Your 20%  
- **GitHub Actions**: https://docs.github.com/actions  
- **GitLab CI**: https://docs.gitlab.com/ee/ci  
- **Jenkins**: https://www.jenkins.io/doc  
- Build → Test → Deploy workflows  
- Secrets management  
- Deployment triggers  

### What You *Don't* Need  
- Writing custom CI runners  

### Pattern Alignment  
- Commit → Build → Test → Deploy  

---

## 3. Docker & Containers  
**System Alignment:** Packaging Layer → Environment Reproducibility  
**Task Frequency:** Daily  

### Your 20%  
- **Docker**: https://docs.docker.com  
- Writing Dockerfiles  
- Multi-stage builds  
- docker-compose  
- Image optimization basics  
- Volume & network basics  

### What You *Don't* Need  
- Deep container runtime internals  

### Pattern Alignment  
- Build → Run → Ship  

---

## 4. Cloud Platforms  
**System Alignment:** Infrastructure Layer → Compute + Storage  
**Task Frequency:** Daily  

### Your 20%  
- **AWS** (EC2, ECR, S3, Lambda, CloudWatch): https://docs.aws.amazon.com  
- **GCP** (Compute Engine, Cloud Run, Cloud Storage): https://cloud.google.com/docs  
- **Azure** equivalents  

Concepts:  
- IAM roles  
- Network basics (VPCs, subnets)  
- Scaling groups  
- Logging + monitoring  

### What You *Don't* Need  
- Full multi-cloud architecture certification  

### Pattern Alignment  
- Provision → Deploy → Monitor  

---

## 5. Infrastructure as Code (IaC)  
**System Alignment:** Automation Layer → Infra Templates  
**Task Frequency:** Daily  

### Your 20%  
- **Terraform**: https://developer.hashicorp.com/terraform/docs  
- Providers (AWS/GCP)  
- Variables + modules  
- State files basics  
- Declarative infra patterns  

### What You *Don't* Need  
- Writing custom Terraform providers  

### Pattern Alignment  
- Declare → Plan → Apply  

---

## 6. Kubernetes (Foundational)  
**System Alignment:** Orchestration Layer → Workload Management  
**Task Frequency:** Daily/Weekly  

### Your 20%  
- Pods, deployments, services  
- ConfigMaps + Secrets  
- Horizontal pod autoscaling  
- Basic YAML configs  
- **kubectl** commands  

### Docs  
- https://kubernetes.io/docs/home/  

### What You *Don't* Need  
- Custom operators  
- Etcd administration  

### Pattern Alignment  
- Deploy → Scale → Heal  

---

# SHOULD-HAVE (Secondary)

## 7. Observability & Monitoring  
### Your 20%  
- **Prometheus**: https://prometheus.io/docs  
- **Grafana**: https://grafana.com/docs  
- Logging pipelines  
- Alerting rules  
- Dashboards for latency + resource usage  

---

## 8. Model Serving (MLOps)  
### Your 20%  
- **MLflow Serving**: https://mlflow.org/docs/latest  
- **TorchServe**: https://pytorch.org/serve  
- **TF Serving**: https://www.tensorflow.org/tfx/guide/serving  
- Containerized model endpoints  

---

## 9. Feature Storage & ML Pipelines  
### Your 20%  
- **Feast (Feature Store)**: https://docs.feast.dev  
- Scheduled batch pipelines  
- Real-time feature retrieval  
- Training → serving consistency  

---

# COULD-HAVE (Tertiary)

## 10. Workflow Orchestration  
### Your 20%  
- **Airflow**: https://airflow.apache.org/docs  
- **Kubeflow Pipelines**: https://www.kubeflow.org/docs/components/pipelines  
- DAGs for ML jobs  
- Data → train → evaluate → deploy workflow  

---

## 11. Serverless Architectures  
### Your 20%  
- AWS Lambda  
- GCP Cloud Functions  
- Lightweight ML inference  

---

# WOULD-LIKE (Optional)

## 12. Advanced Scalability & Architecture  
### Your 20%  
- Service meshes (Istio)  
- Canary deployments  
- Blue/green rollouts  
- Distributed tracing
