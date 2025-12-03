# .github
Alatix AI is a lightweight, modular, and asynchronous AI agent framework designed for building autonomous agents. It provides advanced planning, memory management, tool integration, and multi-LLM support, making it ideal for creating efficient AI systems. Built with simplicity and scalability in mind, Alatix AI enables developers to prototype and deploy agents quickly without heavy dependencies.
Key Features

Advanced Planner: Tree-of-Thought style multi-step planning with candidate generation, scoring, refinement, and dead-end detection. Supports function-calling and tool chaining.
Memory System: Hybrid episodic and semantic memory with automatic summarization, importance decay, pruning, and clustering. Optional persistent storage via FAISS for long-term data retention.
Multi-LLM Support: Seamless integration with providers like OpenAI, Anthropic, Hugging Face, Ollama, and Replicate. Includes caching, retries, stats tracking, and ensemble/failover modes.
Tool Registry: Easy registration of synchronous/asynchronous tools with automatic JSON schema generation for LLM compatibility.
Asynchronous Execution: Full async support for streaming responses, tool runs, and memory operations, ensuring high performance in real-time applications.
Persistent Mode: Enable persistent memory for semantic data using FAISS, with automatic snapshots to disk for durability across sessions.
Configurable Parameters: Customizable max steps, temperature, retrieval limits, and more for fine-tuned agent behavior.
