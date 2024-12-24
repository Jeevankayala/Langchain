# LangChain & Google Gemini API Exploration

This repository contains two Jupyter Notebooks demonstrating the use of LangChain with the Google Gemini API for various language model tasks, including:

- **Prompt Templates:** Creating reusable and dynamic prompts.
- **Chaining:** Combining multiple language model calls using `SimpleSequentialChain` and `SequentialChain`.
- **LangChain Agents:** Leveraging tools like SerpAPI and Wikipedia to augment the LLM's capabilities with real-time information.

## Project Structure

- **`Langchain_Introduction.ipynb`:**  Demonstrates basic LangChain concepts such as `Prompt Templates`, `SimpleSequentialChain`, and `SequentialChain`.
- **`agent_tools.ipynb`:** Explores LangChain agents, showcasing their ability to access external tools like SerpAPI and Wikipedia for enhanced context and updated information.

## Getting Started

### Prerequisites

1.  **Python 3.7+:** Make sure you have Python installed.
2.  **Pip:** Ensure you have pip, Python's package installer.
3. **Jupyter Notebook** : Make sure you have Jupyter notebook installed
4. **Google Gemini API Key:** You'll need a Gemini API key. Get one from [Google AI Studio](https://aistudio.google.com/apikey).
5.  **SerpAPI Key:**  You'll need a SerpAPI key. Get one from [SerpAPI Manage API Key](https://serpapi.com/manage-api-key).


## Key Concepts Explained

### 1. Prompt Templates

-   Prompt templates allow you to construct dynamic prompts that can take user input or other variables. They enable more structured interactions with language models.
-   In `Langchain_Introduction.ipynb`, you will see how to create prompt templates, inject variables, and pass them to a model.

### 2. Chaining (SimpleSequentialChain and SequentialChain)

-   **`SimpleSequentialChain`:** A straightforward way to chain multiple language model calls together. The output of one call becomes the input of the next.
-   **`SequentialChain`:**  Allows for more complex chaining, where you can define the outputs of specific steps and pass only relevant information to the next step.
-   You will find demonstrations of both types of chains in `langchain_introduction.ipynb`, showcasing how to build a workflow of language model interactions.

### 3. LangChain Agents and Tools

-   LangChain agents can be thought of as intelligent decision-making entities that can use "tools" to interact with the outside world.
-   **Why Agents are Needed**: Language models have a limited knowledge base which is usually upto a certain date they were trained on. To overcome the knowledge limitation, Agents use tools to interact with external data sources which are always updated.
-   **SerpAPI Tool:** Used for fetching search results from Google or other search engines, enabling the agent to gather up-to-date information on various topics.
-   **Wikipedia Tool:** Allows access to Wikipedia pages, giving the agent a vast repository of factual data.
-   In `langchain_agents_tools.ipynb`, you'll observe how agents can dynamically choose which tool to use based on a user query, greatly enhancing the LLM's capabilities and reliability. For example, if you ask an agent what is the current price of Bitcoin, it would fetch the latest information from SerpAPI (Google Search) rather than its outdated knowledge and respond to you.
