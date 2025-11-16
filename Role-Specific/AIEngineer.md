**Role Context:** AI Enginner
**Primary Focus:** LLM-powered applications, RAG systems, agents, prompt engineering  
**Daily Tasks:** Fine-tuning, retrieval systems, orchestrating LLM chains  
**Output:** Production AI apps (chatbots, copilots, semantic search)

---

# MUST-HAVE (Primary): 80/20 Core

## 1. Python for AI Engineering  
**System Alignment:** Programming Languages → AI/ML Ecosystem  
**Task Frequency:** Daily  

### Your 20%  
- **LangChain**: https://python.langchain.com  
- **LlamaIndex**: https://docs.llamaindex.ai  
- **async/await (Python)**: https://docs.python.org/3/library/asyncio.html  
- **Pydantic**: https://docs.pydantic.dev  
- **JSON parsing**: https://docs.python.org/3/library/json.html  
- **Error handling (Python)**: https://docs.python.org/3/tutorial/errors.html  

### What You *Don't* Need  
- NumPy internals: https://numpy.org/doc  
- Matplotlib: https://matplotlib.org  
- Statistical libraries: https://scipy.org  

### Pattern Alignment  
- Conditional logic  
- Iteration / batching  
- Retry + fallback handling

---

## 2. LLM APIs & Fine-tuning  
**System Alignment:** AI/ML Ecosystem → LLM Platforms  
**Task Frequency:** Daily  

### Your 20%  
- **OpenAI API**: https://platform.openai.com/docs  
- **Anthropic API**: https://docs.anthropic.com  
- **Prompt engineering guide**: https://www.promptingguide.ai  
- **LoRA/QLoRA**: https://arxiv.org/abs/2106.09685  
- **Token management**: https://platform.openai.com/docs/guides/tokens  
- **JSON mode / structured outputs**: https://platform.openai.com/docs/guides/structured-outputs  

### What You *Don't* Need  
- Transformer internals: https://huggingface.co/docs/transformers/index  
- Training from scratch  
- Custom tokenizers

### Pattern Alignment  
- Filter → Transform → Aggregate  
- State management  

---

## 3. Vector Databases (Deep)  
**System Alignment:** Vector Databases → Retrieval  
**Task Frequency:** Daily  

### Your 20%  
- **Pinecone**: https://docs.pinecone.io  
- **Weaviate**: https://weaviate.io/developers  
- **Milvus**: https://milvus.io/docs  
- **HNSW**: https://arxiv.org/abs/1603.09320  
- **Hybrid Search (BM25)**: https://arxiv.org/abs/1904.08375  
- **Embedding Models (OpenAI)**: https://platform.openai.com/docs/guides/embeddings  
- **Product Quantization (PQ)**: https://ieeexplore.ieee.org/document/5459272  

### What You *Don't* Need  
- Custom index building  
- Deep HNSW internals  

### Pattern Alignment  
- Filter → Transform → Aggregate  

---

## 4. RAG System Architecture  
**System Alignment:** AI/ML Ecosystem → RAG Patterns  
**Task Frequency:** Daily  

### Your 20%  
- **PDF parsing (pypdf)**: https://pypdf.readthedocs.io  
- **Semantic chunking (recursive)**: https://python.langchain.com/docs/modules/data_connection/document_transformers  
- **Retrieval (dense)**: https://huggingface.co/docs/sentence-transformers  
- **Reranking (Cohere ReRank)**: https://docs.cohere.com/reference/rerank  
- **Evaluation metrics**: https://arxiv.org/abs/2309.01431  

### What You *Don't* Need  
- Classical NLP  
- ETL pipelines  

---

## 5. API Development for AI  
**System Alignment:** Back-end Ecosystem → API Layer  
**Task Frequency:** Daily  

### Your 20%  
- **FastAPI**: https://fastapi.tiangolo.com  
- **Streaming responses (SSE)**: https://fastapi.tiangolo.com/advanced/custom-response/#streamingresponse  
- **Rate limiting**: https://github.com/long2ice/fastapi-limiter  
- **Pydantic models**: https://docs.pydantic.dev  
- **CORS**: https://fastapi.tiangolo.com/tutorial/cors  

### What You *Don't* Need  
- Full DB design  
- Custom auth stacks  

---

## 6. LLM Observability  
**System Alignment:** LLM Observability → Monitoring  
**Task Frequency:** Daily  

### Your 20%  
- **LangSmith**: https://docs.langchain.com/docs/langsmith  
- **LangFuse**: https://langfuse.com/docs  
- **Token/cost tracking**: included in both  
- **Prompt versioning**: best practices documented above  

### What You *Don't* Need  
- Traditional ML metrics  

---

# SHOULD-HAVE (Secondary)

## 7. Agent Frameworks  
### Your 20%  
- **ReAct pattern**: https://arxiv.org/abs/2210.03629  
- **Tool calling / schemas**: https://platform.openai.com/docs/guides/function-calling  
- **Memory (LangChain)**: https://python.langchain.com/docs/modules/memory  
- **Planning approaches**: https://arxiv.org/abs/2307.02446  

---

## 8. Embedding Optimization  
### Your 20%  
- PCA: https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html  
- Batch embedding: via OpenAI API  
- Caching: https://python.langchain.com/docs/modules/data_connection/text_embedding/caching  

---

## 9. Docker for AI  
### Your 20%  
- **NVIDIA CUDA images**: https://hub.docker.com/r/nvidia/cuda  
- **TorchServe**: https://pytorch.org/serve  
- **vLLM**: https://docs.vllm.ai  
- **Volume mounting**: https://docs.docker.com/storage/volumes  

---

# COULD-HAVE (Tertiary)

## 10. Model Quantization  
### Your 20%  
- **GPTQ**: https://arxiv.org/abs/2210.17323  
- **AWQ**: https://arxiv.org/abs/2306.00978  
- **GGUF (llama.cpp)**: https://github.com/ggerganov/llama.cpp  

---

## 11. Local LLM Serving  
### Your 20%  
- **Ollama**: https://ollama.ai  
- **vLLM**: https://docs.vllm.ai  
- **llama.cpp**: https://github.com/ggerganov/llama.cpp  

---

# WOULD-LIKE (Optional)

## 12. Custom Model Training  
### Your 20%  
- **MMLU**: https://arxiv.org/abs/2009.03300  
- **HumanEval**: https://arxiv.org/abs/2107.03374  
- Dataset curation references: https://huggingface.co/docs/datasets/index  
