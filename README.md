# Hello, I'm Hyun Woo Jeong 👋

M.S. student in Artificial Intelligence at **Ajou University** (Advisor: Prof. Kyung-Ah Sohn).

My research focus is to make large language models **smaller, cheaper to adapt, and safer to deploy**.

- 🔬 **Research interests:** Large Language Models · Model Compression · Parameter-Efficient Fine-Tuning · AI Safety
- 🎓 M.S. in AI, Ajou University (Mar. 2025 – Feb. 2027, expected) · B.S. in Software and Computer Engineering, Ajou University (2019 – 2025)
- 📫 jhw0714@ajou.ac.kr

---

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| **Languages** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) · ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black) · ![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white) |
| **ML / DL** | ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) · ![Hugging Face](https://img.shields.io/badge/Hugging%20Face-FFD21E?style=flat-square&logo=huggingface&logoColor=black) · PEFT · verl |
| **LLM Apps** | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) · LangGraph · FAISS · RAG · REST APIs |
| **Data** | ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) · ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) · Matplotlib · Seaborn |
| **Dev Tools** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) · ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) · Shell Scripting |

---

## 📄 Publications

- **Hyun Woo Jeong**, Ju-Heon Ha, Taegyu Yang, Dongjun Kim, Kyung-Ah Sohn.
  *Nudge and Merge: Simple Post-Hoc Sparsification of Dense Adapters for Parameter-Efficient Fine-Tuning on Sparse LLMs.*
  Under review (AAAI 2027), 2026.
  
- Yunseo Choi, **Hyun Woo Jeong**, Ho Jin Lee, Ju-Heon Ha, Kyung-Ah Sohn.
  *SchemaTopic: Neural Topic Modeling with LLM-Generated Schemas.*
  ACL ARR May 2026 Submission, 2026.
  
- **Hyun Woo Jeong**, Yunseo Choi, Dong-Hun Choi, Kyung-Ah Sohn.
  *LangGraph-based LLM Agent Design for Addressing Copyright Infringement by Generative AI.* 
  Korea Artificial Intelligence Conference, Sep. 2025. [[paper]](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12416361)
  
- **Hyun Woo Jeong**, Byounghan Lee, Kyung-Ah Sohn.
  *Using Knowledge Injection in Prompt Learning for Counter Speech Generation.* 
  Korea Software Congress (KSC), Dec. 2024. 🏆 Top Excellence Award (Undergraduate) [[paper]](https://www.dbpia.co.kr/journal/articleDetail?nodeId=NODE12042307)

---

## 🚀 Projects

### (Ongoing) LLM Safeguard — Safety Evaluation & Training Design
*Mar. 2026 – Present*

- Designed a hierarchical safety-benchmark taxonomy (**General / Adversarial / Contextual**) for building specialized safeguard models.
- Building a reinforcement-learning pipeline for LLM-based safeguard models, exploring **GRPO** and **MOPD**.

### AI Copyright Dispute Agent — LangGraph + RAG | [[Repo]](https://github.com/dhcryan/ai-copyright-dispute-agent)
*Jul. 2025 – Sep. 2025*

- Orchestrated image-based copyright risk analysis, legal-document retrieval, and LLM response generation with a **LangGraph StateGraph** workflow.
- Built a **FAISS** legal-case retriever with OpenAI embeddings and integrated retrieval-augmented QA into the agent.

---

## 🔬 Research

### Nudge and Merge (NNM): Plug-and-Play Adapter Sparsification for Sparse LLMs
*May 2026 – Present · Master's thesis*

Pruned LLMs save memory, but merging a dense LoRA-style adapter into them breaks the sparsity mask, and re-masking it throws away part of what the adapter learned. **NNM** fixes this **after training, with no retraining**: it nudges the adapter update within the orthogonal complement of the calibration-activation subspace (PCA-based) so that the masked update better reproduces the original adapter's outputs.

- Proposed and implemented post-hoc adapter consolidation that **preserves fixed sparsity masks** (unstructured 50%/75%, semi-structured 2:4/2:8).
- Evaluated on **LLaMA-7B, LLaMA-13B, and Qwen2.5-7B** with Wanda and SparseGPT, across seven zero-shot benchmarks and WikiText-2 perplexity.
  - Qwen2.5-7B: average zero-shot accuracy **62.76% → 63.57%** over direct masked merging.
  - LLaMA-13B (SparseGPT, 75% sparsity): WikiText-2 perplexity **2563.41 → 24.26**.
- Plug-and-play across **LoRA, AdaLoRA, DoRA, and LoRA+**, with no adapter-specific changes.
- Analyzed multi-seed variability, layer-wise output preservation, and GPU cost on a single NVIDIA H200.

### Counter Speech Generation with Knowledge-Injected Prompt Learning
*2024 · Undergraduate research*

- Studied knowledge-injected prompt learning for generating counter speech against hateful expressions while keeping general conversational ability.
- 🏆 **Top Excellence Award (Undergraduate), KSC 2024 Undergraduate/Junior Paper Competition**




