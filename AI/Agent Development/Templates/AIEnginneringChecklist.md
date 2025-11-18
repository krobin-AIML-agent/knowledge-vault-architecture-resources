# AI ENGINEERING MASTER WORKFLOW CHECKLIST  
_LLM Development → Retrieval → Agents → Deployment → Monitoring → Governance_  

---

# PHASE 0: SCOPING (AI Engineering Context)

## 0.1 Define AI Use Case (Single-select)
- [ ] Classification  
- [ ] Regression  
- [ ] NLP / LLMs  
- [ ] Vision  
- [ ] Forecasting  
- [ ] Recommendations  
- [ ] RAG (Retrieval-Augmented Generation)  
- [ ] Agents / Tool-using AI  

## 0.2 Define AI Objective (Single-select)
- [ ] Predictive model  
- [ ] Generative model  
- [ ] Embedding model  
- [ ] Agentic workflow  
- [ ] Retrieval system  
- [ ] Reinforcement learning  

## 0.3 Define Latency Requirements (Single-select)
- [ ] Real-time (< 100ms)  
- [ ] Near real-time (100–1000ms)  
- [ ] Batch/offline  

---

# PHASE 1: DATA PREPARATION

## 1.1 Data Source Acquisition (Multi-select)
- [ ] SQL Databases (Postgres → https://postgresql.org / MySQL → https://mysql.com)  
- [ ] Data Warehouses (Snowflake → https://snowflake.com , BigQuery → https://cloud.google.com/bigquery)  
- [ ] Data Lakes (S3 → https://aws.amazon.com/s3 , GCS → https://cloud.google.com/storage)  
- [ ] APIs  
- [ ] PDF/Doc ingestion  
- [ ] Web scraping  
- [ ] Synthetic data generation  

## 1.2 Data Versioning & Lineage (Multi-select)
- [ ] DVC → https://dvc.org/  
- [ ] LakeFS → https://lakefs.io/  
- [ ] Pachyderm → https://www.pachyderm.com/  
- [ ] DataHub → https://datahubproject.io/  

## 1.3 Data Preprocessing (Multi-select)
- [ ] Cleaning + normalization  
- [ ] Tokenization  
- [ ] Embedding generation  
- [ ] Chunking (for RAG)  
- [ ] OCR (Tesseract → https://github.com/tesseract-ocr/tesseract)  
- [ ] Image augmentation  

## 1.4 Dataset Splits (Single-select)
- [ ] Train/Validation/Test  
- [ ] K-fold  
- [ ] Time-series split  

---

# PHASE 2: VECTOR & RETRIEVAL SYSTEMS

## 2.1 Choose Embedding Model (Single-select)
- [ ] OpenAI Embeddings → https://platform.openai.com/docs/guides/embeddings  
- [ ] HuggingFace Embeddings → https://huggingface.co/models  
- [ ] Sentence Transformers → https://www.sbert.net/  
- [ ] Cohere → https://docs.cohere.com/  

## 2.2 Choose Vector Database (Single-select)
- [ ] Pinecone → https://www.pinecone.io/  
- [ ] Weaviate → https://weaviate.io/  
- [ ] Qdrant → https://qdrant.tech/  
- [ ] Chroma → https://www.trychroma.com/  
- [ ] Faiss → https://github.com/facebookresearch/faiss  

## 2.3 Retrieval System (RAG) (Multi-select)
- [ ] LangChain → https://python.langchain.com/  
- [ ] LlamaIndex → https://www.llamaindex.ai/  
- [ ] Haystack → https://haystack.deepset.ai/  
- [ ] Hybrid (keyword + vector) search  
- [ ] Metadata filtering  
- [ ] Query transformation  

---

# PHASE 3: MODEL DEVELOPMENT

## 3.1 Choose Model Type (Single-select)
- [ ] LLM (OpenAI → https://platform.openai.com , Anthropic → https://anthropic.com , GPT-NeoX, Llama3)  
- [ ] Fine-tuned transformer  
- [ ] Encoder-only (BERT-style)  
- [ ] Diffusion model (images)  
- [ ] Speech model (Whisper → https://github.com/openai/whisper)  

## 3.2 Model Frameworks (Multi-select)
- [ ] PyTorch → https://pytorch.org/  
- [ ] TensorFlow → https://tensorflow.org/  
- [ ] JAX → https://jax.readthedocs.io/en/latest/  
- [ ] HuggingFace Transformers → https://huggingface.co/transformers  
- [ ] OpenAI Assistants API → https://platform.openai.com/docs/assistants  

## 3.3 Agent Frameworks (Multi-select)
- [ ] LangChain Agents → https://python.langchain.com/docs/agents/  
- [ ] LlamaIndex Agents → https://docs.llamaindex.ai/agents  
- [ ] CrewAI → https://crewai.com/  
- [ ] OpenAI Assistants Agents  

## 3.4 Experiment Tracking (Multi-select)
- [ ] MLflow → https://mlflow.org/  
- [ ] Weights & Biases → https://wandb.ai/  
- [ ] TensorBoard  
- [ ] Neptune.ai → https://neptune.ai/  

## 3.5 Hyperparameter Optimization (Multi-select)
- [ ] Optuna → https://optuna.org/  
- [ ] Ray Tune → https://docs.ray.io/en/latest/tune  
- [ ] Hyperopt  
- [ ] Grid / Random search  

---

# PHASE 4: EVALUATION

## 4.1 Metrics (Multi-select)
- [ ] Accuracy / Precision / Recall  
- [ ] F1 Score  
- [ ] AUROC  
- [ ] RMSE / MAE  
- [ ] BLEU / ROUGE  
- [ ] Cosine similarity  
- [ ] LLM-as-a-judge → https://platform.openai.com/docs/guides/evaluation  

## 4.2 Evaluation Tools (Multi-select)
- [ ] OpenAI Eval → https://platform.openai.com/docs/guides/evaluation  
- [ ] Ragas → https://docs.ragas.io/  
- [ ] DeepEval → https://github.com/confident-ai/deepeval  
- [ ] TruLens → https://www.trulens.org/  

## 4.3 Validations (Multi-select)
- [ ] Bias & fairness  
- [ ] Drift analysis  
- [ ] Hallucination testing  
- [ ] Safety & prompt injection tests  
- [ ] Explainability (SHAP → https://shap.readthedocs.io/)  

---

# PHASE 5: DEPLOYMENT (MLOps / LLMOps)

## 5.1 Packaging Model (Multi-select)
- [ ] Docker container → https://docker.com  
- [ ] ONNX → https://onnx.ai/  
- [ ] TorchScript  
- [ ] Model artifact registry  

## 5.2 Deployment Strategy (Single-select)
- [ ] Serverless (Lambda → https://aws.amazon.com/lambda , Cloud Run → https://cloud.google.com/run)  
- [ ] GPU-backed containers (NVIDIA Triton → https://developer.nvidia.com/nvidia-triton-inference-server)  
- [ ] ML platforms (SageMaker → https://aws.amazon.com/sagemaker , Vertex AI → https://cloud.google.com/vertex-ai)  
- [ ] Edge deployment  

## 5.3 Serving APIs (Multi-select)
- [ ] FastAPI → https://fastapi.tiangolo.com/  
- [ ] Flask → https://flask.palletsprojects.com/  
- [ ] gRPC → https://grpc.io/  
- [ ] WebSockets  
- [ ] Batch inference  

## 5.4 Model Registry (Multi-select)
- [ ] MLflow Registry  
- [ ] SageMaker Registry  
- [ ] Vertex AI Model Registry  
- [ ] WandB Artifacts  

---

# PHASE 6: AGENTS, TOOLS & AUTOMATION

## 6.1 Tools for Agents (Multi-select)
- [ ] LangChain Tools → https://python.langchain.com/docs/integrations/tools  
- [ ] Browser tools  
- [ ] Code execution sandboxes  
- [ ] SQL database agents → https://python.langchain.com/docs/integrations/tools/sql  
- [ ] File search / RAG tools  
- [ ] Custom business logic tools  

## 6.2 Memory Systems (Multi-select)
- [ ] LangChain Memory → https://python.langchain.com/docs/modules/memory/  
- [ ] LlamaIndex Memory → https://docs.llamaindex.ai  
- [ ] Redis memory → https://redis.io  
- [ ] Vector memory stores  

## 6.3 Orchestration (Multi-select)
- [ ] LangGraph → https://langchain-ai.github.io/langgraph/  
- [ ] Airflow → https://airflow.apache.org/  
- [ ] Prefect → https://www.prefect.io/  
- [ ] Dagster → https://dagster.io/  

---

# PHASE 7: PRODUCTION MONITORING (LLMOps)

## 7.1 Model Monitoring (Multi-select)
- [ ] Latency  
- [ ] Token usage  
- [ ] Cost monitoring  
- [ ] Throughput  
- [ ] Error rates  

## 7.2 Drift Monitoring Tools  
- [ ] Evidently AI → https://evidentlyai.com/  
- [ ] WhyLabs → https://whylabs.ai/  

## 7.3 RAG Monitoring (Multi-select)
- [ ] Retrieval accuracy  
- [ ] Context relevance  
- [ ] Hallucination rates  
- [ ] Embedding drift  

## 7.4 Logging (Multi-select)
- [ ] OpenAI Logs  
- [ ] Prometheus → https://prometheus.io  
- [ ] Grafana → https://grafana.com  
- [ ] Datadog → https://datadoghq.com  

---

# PHASE 8: GOVERNANCE & SECURITY

## 8.1 Model Governance (Multi-select)
- [ ] Audit logs  
- [ ] Model versioning  
- [ ] Dataset lineage  
- [ ] Approval workflows  

## 8.2 Responsible AI (Multi-select)
- [ ] Bias monitoring  
- [ ] Safety testing  
- [ ] Red-teaming  
- [ ] Hallucination mitigation strategies  

## 8.3 Access Control (Multi-select)
- [ ] IAM policies  
- [ ] API authentication  
- [ ] RBAC (role-based access)  

---

# PHASE 9: CONTINUOUS IMPROVEMENT

## 9.1 Optimization Techniques (Multi-select)
- [ ] Quantization  
- [ ] Distillation  
- [ ] Pruning  
- [ ] LoRA tuning → https://huggingface.co/blog/lora  
- [ ] Batch optimizations  

## 9.2 CI/CD for AI (Multi-select)
- [ ] GitHub Actions → https://github.com/features/actions  
- [ ] GitLab CI  
- [ ] Argo Workflows → https://argo-workflows.readthedocs.io  
- [ ] Jenkins  

## 9.3 Future-Proofing (Multi-select)
- [ ] Dataset versioning  
- [ ] Automatic re-training pipelines  
- [ ] Model lifecycle automation  
- [ ] Agent-based system orchestration  
