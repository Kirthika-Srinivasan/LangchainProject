# 🦜🔗 LangChain & LangGraph Tutorial Repo

Welcome to the **LangChain & LangGraph Tutorial** repository! This project serves as a comprehensive, step-by-step guide to building agentic AI workflows, integrating multiple LLM providers, defining custom tools, managing conversational state/memory, and generating structured outputs using the latest LangChain (v1/v2) and LangGraph ecosystem.

---

## 🚀 Key Features & Topics Covered

The repository is structured into sequential Jupyter Notebooks, each focusing on a core concept of the modern LangChain/LangGraph stack:

| Notebook | Topic | Key Concepts Covered |
| :--- | :--- | :--- |
| 📓 [01-langchainintro.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/01-langchainintro.ipynb) | **LangChain V1 Agents** | Building complete conversational agents using `create_agent` with custom tool definitions. |
| 📓 [02-modelintegration.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/02-modelintegration.ipynb) | **Multi-Model Integration** | Integrating **OpenAI (GPT-4)**, **Google Gemini**, **Groq (Qwen)**, and **Ollama (Local Models)**. Demonstrates invocation, streaming (`.stream()`), batching (`.batch()`), and concurrency limits. |
| 📓 [03-tools.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/03-tools.ipynb) | **Tool Creation & Binding** | Declaring custom tools with the `@tool` decorator, binding them to chat models via `.bind_tools()`, and inspecting tool calls in model outputs. |
| 📓 [04-messages.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/04-messages.ipynb) | **Message Protocols** | Managing conversation history using `SystemMessage`, `HumanMessage`, `AIMessage`, and `ToolMessage`. Accessing token usage metrics via `usage_metadata`. |
| 📓 [05-structuredoutput.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/05-structuredoutput.ipynb) | **Structured Outputs** | Formatting LLM responses using `with_structured_output()`. Supports Pydantic `BaseModel`, `TypedDict`, Python `dataclasses`, and returning raw model messages alongside parsed JSON. |
| 📓 [06-middleware.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/06-middleware.ipynb) | **State & Memory Middleware** | Utilizing `InMemorySaver` from LangGraph for session-level persistence, thread-based conversation memory, and checkpoint management. |

---

## 🛠️ Getting Started

### Prerequisites

This project is configured using Python and managed via **uv** (a fast Python package installer and resolver).

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Kirthika-Srinivasan/LangchainProject.git
   cd LangchainProject
   ```

2. **Set Up the Virtual Environment**:
   Using `uv` (recommended):
   ```bash
   uv venv
   .venv\Scripts\activate  # On Windows
   uv sync
   ```
   Or using standard `pip`:
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables**:
   Create a `.env` file in the root directory and add your API keys:
   ```env
   OPENAI_API_KEY=your_openai_api_key_here
   GROQ_API_KEY=your_groq_api_key_here
   GOOGLE_API_KEY=your_google_api_key_here
   ```

---

> [!NOTE]
> All credentials and configurations in `.env` are automatically ignored from git tracking to prevent accidental exposure of sensitive keys.

> [!TIP]
> Use the [02-modelintegration.ipynb](file:///c:/Users/kirth/OneDrive/Desktop/AI_Software_Engineer_Kirthika/Github_Projects_for_AI/Agentic_AI_Overall/LangchainProject/updatedlangchain/02-modelintegration.ipynb) notebook to quickly test if your API keys are configured correctly by executing the model diagnostics cells.
