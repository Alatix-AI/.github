<!-- .github/profile/README.md -->
<h1 align="center">
    <img src="./alaxitai.jpg" alt="AlatixAI Logo" width="120"/>
    <br>
    Alatix Agent Framework
</h1>

<p align="center"><em>"Empower AI Agents to plan, remember, and act autonomously."</em></p>

---

## 🚀 Overview

Alatix AI is a lightweight, open-source framework for building intelligent, autonomous AI agents. Designed for developers and researchers, it enables seamless integration of large language models (LLMs) with advanced planning, memory management, and tool execution capabilities. At its core, Alatix leverages a modular architecture to create agents that can reason, learn from experience, and interact with external tools in real time. It combines:

- **LLM Integration** – A unified adapter system supporting multiple providers like OpenAI, Anthropic, HuggingFace, Replicate, and Ollama. It handles generation, streaming, embedding, function-calling, caching, retries, and stats tracking for efficient and reliable LLM interactions.
- **Advanced Multi-step Planner** – it uses a Tree-of-Thought approach with multi-candidate generation, scoring, ranking, self-refinement, and dead-end detection. This enables robust multi-step planning, tool chaining, and adaptive decision-making.
- **Memory System** – Combines episodic memory (for recent events with chunk-based summarisation) and semantic memory (for long-term knowledge with importance decay, pruning, and clustering). Optional persistence via FAISS ensures data durability across sessions.
- **Tool Execution** – A registry for defining synchronous or asynchronous tools with automatic JSON schema generation from Python functions. Safe execution wrappers normalize outputs and handle errors.

---

## 🛠 Key Features

| Feature | Description |
|---------|-------------|
| **LLM Adapter** | Connects any LLM backend with adjustable temperature, max tokens, and function-calling support. |
| **Planner** | Multi-step, tree-of-thought planning with candidate scoring, pruning, and dead-end detection. |
| **Memory** | Semantic memory for knowledge storage and episodic memory for task history. |
| **Tools** | Define Python functions as agent-callable tools with automatic JSON schema generation. |
| **Streaming Execution** | Step-by-step output streaming and tool execution events. |
| **Persistence** | Store agent knowledge and history for long-term autonomous behavior. |

---

## Learn more

- [`Alatix`](https://github.com/Alatix-AI/Alatix Agent Framework) 
