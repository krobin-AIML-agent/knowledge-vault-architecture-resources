# Artificial Intelligence and Machine Learning

Modern AI systems overview: core research, engineering practices, and architectures that define production AI today.

---

## Table of Contents

- [Reasoning and Prompting](#reasoning-and-prompting)
- [Reinforcement Learning Foundations](#reinforcement-learning-foundations)
- [Neural Network Architecture](#neural-network-architecture)
- [Reliability and Safety](#reliability-and-safety)
- [AI Engineering](#ai-engineering)
- [Agentic Systems](#agentic-systems)

---

## Reasoning and Prompting

### Chain of Thought (CoT) Prompting

Improves reasoning by having models generate intermediate logical steps before producing answers. Essential for math, planning, and multi-step logic tasks.

**Key Papers:**
- **[Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903)** (Wei et al., 2022)
- **[Large Language Models are Zero-Shot Reasoners](https://arxiv.org/abs/2205.11916)** (Kojima et al., 2022)

**Resources:**
- **[Prompt Engineering Guide](https://www.promptingguide.ai/)**: Comprehensive techniques
- **[OpenAI Cookbook](https://cookbook.openai.com/)**: Practical examples

---

## Reinforcement Learning Foundations

### RLHF (Reinforcement Learning from Human Feedback)

The training methodology behind ChatGPT, Claude, and modern LLMs. Models learn from human preference rankings to produce safer, more natural responses.

**Key Papers:**
- **[InstructGPT: Training language models to follow instructions with human feedback](https://arxiv.org/abs/2203.02155)** (Ouyang et al., 2022)
- **[Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073)** (Anthropic, 2022)

**Resources:**
- **[Hugging Face RLHF Blog](https://huggingface.co/blog/rlhf)**: Comprehensive overview
- **[Anthropic's RLHF Research](https://www.anthropic.com/research)**: Safety-focused approach

### Deep Q Networks (DQN)

Landmark 2015 work that established deep RL as practical. Learned to play Atari games from raw pixels.

**Key Paper:**
- **[Human-level control through deep reinforcement learning](https://www.nature.com/articles/nature14236)** (Mnih et al., 2015)

**Modern Implementations:**
- **[Stable Baselines3](https://stable-baselines3.readthedocs.io/)**: Production-ready PyTorch RL

---

## Neural Network Architecture

### Transformers (The Current Standard)

The architecture powering all modern LLMs (GPT, BERT, Claude, Llama). Replaced RNNs/LSTMs for sequence modeling.

**Key Paper:**
- **[Attention Is All You Need](https://arxiv.org/abs/1706.03762)** (Vaswani et al., 2017)

**Modern Variants:**
- **[LLaMA: Open and Efficient Foundation Language Models](https://arxiv.org/abs/2302.13971)** (Meta, 2023)
- **[GPT-4 Technical Report](https://arxiv.org/abs/2303.08774)** (OpenAI, 2023)

### Dropout & Regularization

Classic technique (2014) still used in every modern neural network. Prevents overfitting.

**Key Paper:**
- **[Dropout: A Simple Way to Prevent Neural Networks from Overfitting](https://jmlr.org/papers/v15/srivastava14a.html)** (Srivastava et al., 2014)

### Retentive Networks

Recent alternative to transformers with better efficiency for long contexts. Worth watching.

**Key Paper:**
- **[Retentive Network: A Successor to Transformer for Large Language Models](https://arxiv.org/abs/2307.08621)** (Sun et al., 2023)

---

## Reliability and Safety

### Hallucination Mitigation

Core challenge in production LLM systems. RAG (Retrieval-Augmented Generation) is the current best practice.

**Key Papers:**
- **[Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)** (Lewis et al., 2020)
- **[Survey of Hallucination in Natural Language Generation](https://arxiv.org/abs/2202.03629)** (Ji et al., 2022)

**Production Tools:**
- **[LangChain RAG](https://python.langchain.com/docs/use_cases/question_answering/)**: RAG implementation
- **[LlamaIndex](https://www.llamaindex.ai/)**: Data framework for LLM apps
- **[Chroma](https://www.trychroma.com/)**: Vector database
- **[Pinecone](https://www.pinecone.io/)**: Vector database (managed)

---

## AI Engineering

### ML Systems Design

Real-world production systems: deployment, monitoring, drift detection, pipelines, and lifecycle management.

**Essential Reading:**
- **[Designing Machine Learning Systems](https://www.oreilly.com/library/view/designing-machine-learning/9781098107956/)** by Chip Huyen
- **[Chip Huyen's Blog](https://huyenchip.com/blog/)**: ML engineering insights

**Production Stack:**
- **[FastAPI](https://fastapi.tiangolo.com/)**: API framework for ML
- **[Ray](https://www.ray.io/)**: Distributed ML training/serving
- **[MLflow](https://mlflow.org/)**: ML experiment tracking
- **[Weights & Biases](https://wandb.ai/)**: Experiment tracking & visualization

### Data Engineering

Infrastructure that supports AI systems: ingestion, storage, transformation, orchestration.

**Essential Reading:**
- **[Fundamentals of Data Engineering](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/)** by Reis & Housley

**Modern Stack:**
- **[dbt](https://www.getdbt.com/)**: Data transformation
- **[Dagster](https://dagster.io/)**: Data orchestration (modern Airflow alternative)
- **[DuckDB](https://duckdb.org/)**: Embedded analytics database
- **[Apache Kafka](https://kafka.apache.org/)**: Event streaming

---

## Agentic Systems

### AI Agents (Planning + Tool Use)

Systems that can plan, reason, and execute multi-step actions using tools. The current frontier of AI applications.

**Key Papers:**
- **[ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)** (Yao et al., 2022)
- **[Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761)** (Schick et al., 2023)
- **[Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442)** (Park et al., 2023)

**Production Frameworks:**
- **[LangGraph](https://langchain-ai.github.io/langgraph/)**: Graph-based agent orchestration (recommended)
- **[AutoGen](https://microsoft.github.io/autogen/)**: Microsoft's multi-agent framework
- **[CrewAI](https://www.crewai.com/)**: Role-based multi-agent system
- **[Semantic Kernel](https://learn.microsoft.com/en-us/semantic-kernel/)**: Microsoft's agent SDK

### Agent Protocols & Standards

**Current Standards:**
- **[Model Context Protocol (MCP)](https://www.anthropic.com/news/model-context-protocol)**: Anthropic's agent communication standard
- **[OpenAI Function Calling](https://platform.openai.com/docs/guides/function-calling)**: Tool use standard

### Multi-Agent Systems

**Key Papers:**
- **[MetaGPT: Meta Programming for Multi-Agent Collaborative Framework](https://arxiv.org/abs/2308.00352)** (2023)
- **[ChatDev: Communicative Agents for Software Development](https://arxiv.org/abs/2307.07924)** (2023)

---

## Essential Learning Path

### For Practitioners (Start Here)

**Month 1: Foundations**
1. Read Chain-of-Thought paper
2. Understand transformer architecture
3. Learn prompt engineering basics

**Month 2: Production Systems**
4. Study Chip Huyen's ML systems book
5. Build a simple RAG system with LangChain
6. Implement basic monitoring

**Month 3: Advanced Applications**
7. Read ReAct paper
8. Build an AI agent with LangGraph
9. Study RLHF methodology

### Core Papers (Read These)

**Must Read (Top 5):**
1. **[Attention Is All You Need](https://arxiv.org/abs/1706.03762)**: Transformers
2. **[InstructGPT](https://arxiv.org/abs/2203.02155)**: RLHF
3. **[Chain-of-Thought](https://arxiv.org/abs/2201.11903)**: Prompting
4. **[RAG](https://arxiv.org/abs/2005.11401)**: Retrieval-augmented generation
5. **[ReAct](https://arxiv.org/abs/2210.03629)**: AI agents

**Next 5 (Depth):**
6. Constitutional AI: Safety
7. LLaMA: Open models
8. Toolformer: Tool use
9. Survey of Hallucination: Reliability
10. MetaGPT: Multi-agent systems

---

## Modern Tech Stack

### LLM Providers
- **[OpenAI](https://platform.openai.com/)**: GPT-4, ChatGPT
- **[Anthropic](https://www.anthropic.com/)**: Claude
- **[Together AI](https://www.together.ai/)**: Open models (Llama, Mixtral)
- **[Groq](https://groq.com/)**: Fast inference

### Vector Databases
- **[Chroma](https://www.trychroma.com/)**: Open source, local
- **[Pinecone](https://www.pinecone.io/)**: Managed, production
- **[Weaviate](https://weaviate.io/)**: Open source, scalable
- **[Qdrant](https://qdrant.tech/)**: High performance

### ML Frameworks
- **[PyTorch](https://pytorch.org/)**: Deep learning (industry standard)
- **[Hugging Face Transformers](https://huggingface.co/docs/transformers/)**: Pre-trained models
- **[LangChain](https://www.langchain.com/)**: LLM applications
- **[LlamaIndex](https://www.llamaindex.ai/)**: Data framework for LLMs

### Deployment
- **[Modal](https://modal.com/)**: Serverless GPU
- **[Replicate](https://replicate.com/)**: Model API hosting
- **[AWS SageMaker](https://aws.amazon.com/sagemaker/)**: Full ML platform
- **[Google Vertex AI](https://cloud.google.com/vertex-ai)**: Full ML platform

---

## Learning Resources

### Online Courses
- **[Fast.ai Practical Deep Learning](https://course.fast.ai/)**: Free, practical
- **[DeepLearning.AI](https://www.deeplearning.ai/)**: Specializations
- **[Hugging Face Course](https://huggingface.co/learn)**: Transformers, free

### Communities
- **[r/LocalLLaMA](https://www.reddit.com/r/LocalLLaMA/)**: Open source LLMs
- **[r/MachineLearning](https://www.reddit.com/r/MachineLearning/)**: Research
- **[Hugging Face Discord](https://discord.gg/hugging-face)**: NLP community
- **[LangChain Discord](https://discord.gg/langchain)**: Agent development

### Stay Current
- **[Papers with Code](https://paperswithcode.com/)**: Latest research + code
- **[Hugging Face Daily Papers](https://huggingface.co/papers)**: Curated papers
- **[AI News by ThursdAI](https://www.thursdai.news/)**: Weekly AI updates
- **[Import AI Newsletter](https://jack-clark.net/)**: Weekly research roundup

---

## Summary

Modern AI is built on:
- **Transformers** (architecture)
- **RLHF** (alignment)
- **RAG** (grounding)
- **Agents** (autonomy)

Production stack:
- **PyTorch** + **Transformers** for models
- **LangGraph** for agents
- **Vector DB** for knowledge
- **FastAPI** for serving

Focus on **practical implementation** over theory. Build, deploy, iterate.

---

**Last Updated**: November 2025  
**License**: MIT

**Last Updated**: November 2025  
**License**: MIT: Use freely with attribution

