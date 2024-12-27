# PIAIC - Projects

## Project 1: Hello World with LangChain

This project demonstrates the initialization and use of a Google Gemini model via LangChain to generate a "Hello, World!" response.

### 🚀 Code Example

```python
# Install required packages
!pip install -Uq langchain langchain-google-genai

# Importing necessary modules
from langchain_google_genai import ChatGoogleGenerativeAI
from google.colab import userdata

# Retrieving API Key securely
GOOGLE_API_KEY = userdata.get('GOOGLE_API_KEY')

# Initializing the Gemini 2.0 model
llm: ChatGoogleGenerativeAI = ChatGoogleGenerativeAI(
    model="gemini-2.0-flash-exp",
    api_key=GOOGLE_API_KEY,
)

# Simple Hello World Prompt
response = llm("Hello, world!")
print(response)
```

## 📖 Explanation

### Installation
The command `!pip install -Uq langchain langchain-google-genai` installs the required packages:
- **langchain**: A framework for building applications with language models.
- **langchain-google-genai**: A module for integrating Google Gemini models with LangChain.

### Imports
- **ChatGoogleGenerativeAI** from `langchain_google_genai`: This class provides an interface to use Google’s Gemini models.
- **userdata** from `google.colab`: This allows us to securely access user-specific environment variables, such as the API key needed to authenticate with the Google Gemini model.

### Retrieving the API Key
- **GOOGLE_API_KEY**: Retrieved securely using `userdata.get('GOOGLE_API_KEY')` to ensure safe access and prevent hardcoding sensitive credentials in the code.

### Model Initialization
The `ChatGoogleGenerativeAI` class is instantiated with the following parameters:
- **`model="gemini-2.0-flash-exp"`**: Specifies the Gemini model version used in this project.
- **`api_key=GOOGLE_API_KEY`**: Authenticates the request using the provided API key.

### Sending a Prompt
- The prompt `"Hello, world!"` is sent to the Gemini model using the instantiated `llm` object.
- The model processes the prompt and returns a response, which is printed to the console using `print(response)`.

### 🤖 Why Gemini?
Google’s **Gemini** models represent the next generation of large language models (LLMs). They are designed to provide:
- High-quality, contextually accurate responses.
- Superior performance for a variety of tasks, from natural language understanding to problem-solving.
- Efficiency and scalability for modern AI applications.

In this project, the `"gemini-2.0-flash-exp"` model showcases the latest advancements in Google’s LLM capabilities.
