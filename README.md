# Function Calling with Llama-Index Workflows

A demonstration of function calling using LlamaIndex workflows, works with proprietary OpenAI and open-source models hosted through Ollama.

## Installation

1. **Clone the repository**
```bash
git clone https://github.com/AegisAurora/function-calling-demo.git
cd function-calling-demo
```
2. **Install dependencies with Poetry**
```bash
poetry install
```

3. **(Optional) Install Ollama to use function calling with open-source models**

https://ollama.com/download

## Usage

1. **You can run examples in demo.ipynb notebook**
2. **You can define extra tools in the notebook**
3. **Set Up Environment Variables (if using OpenAI)**

Create a .env file and parse it or set your enviroment variables directly in the notebook.

4. **Setting up Ollama**

In order to use open source models, have the Ollama installed and then run:

```bash
ollama serve
```

To start a local Ollama server, then run:

```bash
ollama pull llama3.1:latest
```

Once the model is downloaded, you can run the inference!