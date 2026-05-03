# 🧠 Agentic AI Portfolio — LangGraph + RAG + Guardrails

![Python](https://img.shields.io/badge/Python-3.11%2B-blue.svg)
![LangGraph](https://img.shields.io/badge/LangGraph-Stateful%20Workflows-green.svg)
![RAG](https://img.shields.io/badge/RAG-FAISS%20Vector%20Search-orange.svg)
![Guardrails](https://img.shields.io/badge/Guardrails-Validation%20%2B%20Retry-purple.svg)
![LLM](https://img.shields.io/badge/LLM-Groq-black.svg)

A portfolio of **production-style Agentic AI systems** built using **LangGraph**, focused on:

✅ Deterministic workflows (explicit control flow)  
✅ Validation-first design (guardrails)  
✅ Tool-based execution (LLM orchestrates, tools act)  
✅ RAG grounding (FAISS retrieval + citations)  
✅ Retry logic & failure handling  

> **Core philosophy:** **Plan → Act → Verify → Recover**

---

## 📌 Quick Links (Repositories)

- **Project 1 — Task Automation Agent:** https://github.com/Sameerrepos/langgraph-task-automation-agent  
- **Project 2 — Decision‑Making Agent:** https://github.com/Sameerrepos/langgraph-decision-making-agent  
- **Project 3 — Reliable AI Assistant (Guardrails):** https://github.com/Sameerrepos/langgraph-reliable-ai-assistant  
- **Project 4 — RAG Assistant (FAISS + Guardrails):** https://github.com/Sameerrepos/RAG  

---

## 🧩 Architecture Patterns Used

### 1) Planner → Executor → Validator (Agentic Workflow)
```text
Planner → Executor → Validator → [VALID → END | INVALID → Retry]
```

### 2) RAG Workflow (Retriever → Responder → Validator)
```text
Retriever(FAISS) → Responder(LLM) → Validator → [VALID → END | INVALID → Re-retrieve]
```

### Mermaid Diagram (GitHub renders this)
```mermaid
flowchart TD
  A[START] --> B[Retriever (FAISS)]
  B --> C[Responder (LLM)]
  C --> D[Validator (VALID/INVALID)]
  D -->|VALID| E[END]
  D -->|INVALID & retries left| B
```

---

## 📂 Projects Overview (What each one proves)

### ✅ Project 1 — LangGraph Task Automation Agent  
**Focus:** Tool execution + workflow reliability  
**Repo:** https://github.com/Sameerrepos/langgraph-task-automation-agent

**Highlights**
- Planner → Executor → Validator workflow
- Tool-driven actions (deterministic results)
- Reliability-first patterns (clear responsibilities + controlled flow)

---

### ✅ Project 2 — LangGraph Decision‑Making Agent  
**Focus:** Explainable approval/rejection decisions  
**Repo:** https://github.com/Sameerrepos/langgraph-decision-making-agent

**Highlights**
- Deterministic decision pipeline (APPROVED/REJECTED)
- Rule + LLM hybrid design
- Explanation + validation (auditable decisions)

---

### ✅ Project 3 — Reliable AI Assistant (Guardrails)  
**Focus:** Response quality + validation + retries  
**Repo:** https://github.com/Sameerrepos/langgraph-reliable-ai-assistant

**Highlights**
- Intent → Responder → Validator loop
- Self-verification (VALID/INVALID)
- Retry on low-quality output (bounded retries)

---

### ✅ Project 4 — RAG Assistant (LangGraph + FAISS + Guardrails)  
**Focus:** Retrieval-grounded answers with citations + validation + retry  
**Repo:** https://github.com/Sameerrepos/RAG

**Highlights**
- Real vector retrieval using FAISS
- Chunking + overlap for better retrieval precision
- Grounded generation using retrieved context
- Citations/sources for traceability
- Validator checks relevance + grounding
- Retry goes back to retriever (stronger than retrying responder only)

---

## ⚙️ How to Run (Quickstart)

> Each project is independent. Use **one virtual environment per repo**.

### Windows PowerShell
```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

### Environment variables
Create `.env` from `.env.example` (do NOT commit `.env`):
```env
GROQ_API_KEY=your_groq_key_here
HF_TOKEN=optional_hf_token_here
```

---

## ▶️ Run Commands (per project)

### Project 1 — Task Automation Agent
```bash
python main.py
```

### Project 2 — Decision‑Making Agent
```bash
python main.py
```

### Project 3 — Reliable AI Assistant
```bash
python main.py
```

### Project 4 — RAG Assistant
```bash
python RAG_final.py
```

---

## 🧪 Suggested Test Queries (RAG project)
- What is an AI agent?
- How do agentic systems prevent hallucinations?
- What is the capital of France?  
  ✅ Expected: “I don’t know based on the provided documents.”

---

## 🔍 What This Portfolio Demonstrates (Skills)

### Agentic AI & LLM Systems
- LangGraph state-driven workflows
- Planner–Executor–Validator architecture
- Validation guardrails + retry logic
- Tool orchestration patterns

### RAG (Retrieval‑Augmented Generation)
- Chunking + overlap
- Embeddings (HuggingFace)
- FAISS vector search
- Grounded generation with citations
- Retrieval failure handling + retries

### Engineering Mindset
- Deterministic flow control
- Debuggable state transitions
- Reliability-first system design

---

## 📌 Recommended Pin Order (GitHub Profile)
1) RAG Assistant (FAISS + Guardrails)  
2) Task Automation Agent  
3) Decision‑Making Agent  
4) Reliable AI Assistant (Guardrails)  

---

## 🗺️ Roadmap (Optional Enhancements)
- Add reranking (improve retrieval quality)
- Add structured evaluation (simple test suite)
- Persist FAISS index + caching improvements
- Add a small UI demo (Streamlit) after core stability

---

## 📫 Connect
- GitHub: https://github.com/Sameerrepos  
- LinkedIn: (add your LinkedIn link here)

✅ Thanks for checking out my work!
