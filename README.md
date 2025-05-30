# Tool Calling / Function Calling in Agentic AI

## 📌 What is Tool Calling / Function Calling?

In Agentic AI systems (like OpenAI's Assistants or custom agents built with frameworks like LangChain, AutoGen, or CrewAI), Tool Calling or Function Calling** is a feature that allows an AI agent to:
- **Call external functions, APIs, or tools** to perform real-world tasks.
- Extend its capabilities beyond language generation.
- Interact with the environment through code, APIs, or utilities.

---

## 🧠 Why is it Important?

Language models (LLMs) are good at reasoning and understanding context, but they:
- **Cannot access real-time data** (like current weather, stock prices, databases).
- **Can't execute code directly** (like running a Python script or accessing files).

Tool calling enables LLMs to **delegate specific tasks** to external tools.

---

## ⚙️ How Does It Work?

1. **You define a tool/function** (with name, parameters, and description).
2. **LLM decides** (based on prompt) if a tool is needed.
3. If needed, it automatically calls the tool with the correct inputs.
4. **Tool executes**, returns the result.
5. LLM **uses the result** to continue the conversation or reasoning.

---

## 🔧 Example (Python Function Tool)

```python
def get_weather(city: str, unit: str = "metric") -> str:
    """
    Fetches weather data from OpenWeatherMap API.
    """
    # pseudo-code
    return f"The weather in {city} is 28°C with clear sky."
