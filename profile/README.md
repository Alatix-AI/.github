<!-- .github/profile/README.md -->
<h1 align="center">
    <img src="alaxitai.jpg" alt="AlatixAI Logo" width="120"/>
    <br>
    Alatix Agent Framework
</h1>

<p align="center"><em>"Empower AI Agents to plan, remember, and act autonomously."</em></p>

---

## 🚀 Overview

Alatix is an open-source **agent framework** designed for developers and researchers who want to build autonomous AI agents. It combines:

- **LLM Integration** – Support for OpenAI, HuggingFace, and other LLM backends.
- **Advanced Multi-step Planner** – planning with candidate generation, scoring, and self-refinement.
- **Memory System** – Semantic and episodic memory for context-aware decision making.
- **Tool Execution** – Easily integrate synchronous and asynchronous tools with unified JSON input/output.

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

## ⚡ Usage Example

```python
from alatix.agent import Agent
from alatix.tools import tool

# Define a simple tool
@tool
def save_file(name: str, content: str):
    with open(name, "w", encoding="utf-8") as f:
        f.write(content)
    return {"status": "saved", "filename": name}

# Initialize the agent
Codeagent = Agent(
    model="huggingface:Qwen/Qwen3-Coder-30B-A3B-Instruct:nebius",
    api_key="hf_xxx",
    max_tokens=4048,
    tools=[save_file],
    max_steps=5,
    temperature=0.6,
    persistent=True
)

# Run agent asynchronously
import asyncio

async def main():
    query = "Search the internet for latest AI agent advancements and save the code."
    result = await Codeagent.run(query)
    print("Final Result:\n", result)

asyncio.run(main())

