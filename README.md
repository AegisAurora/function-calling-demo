# Function Calling with Llama-Index Workflows

There are a couple of approaches to running function calling with open-source models. One of the approaches you can take is using Llama-Index together with Ollama. Particularly, you can use Llama-Index's `Workflow` or `AgentWorkflow` classes to construct the agent. I will be following: https://docs.llamaindex.ai/en/stable/examples/workflow/function_calling_agent/ and using workflows for this implementation. `Ollama` class inherits from `FunctionCallingLLM` (This is requred to get a `ChatMemoryBuffer`), therefore it is a good choice for running Llama3.1 model. The `agent` workflow is defined in `function_calling_demo` library and then constructed in the demo notebook. You can either use OpenAI API or local models that Ollama supports for function calling.

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
It allows choosing a model and defining new tools.

2. **Set Up Environment Variables (if using OpenAI)**

Create a `.env` file and parse it or set your enviroment variables directly in the notebook.

3. **Setting up Ollama**

In order to use open source models, have the Ollama installed and then run:

```bash
ollama serve
```

To start a local Ollama server, then run:

```bash
ollama pull llama3.1:latest
```

Once the model is downloaded (This downloads the smallest model), you can run the inference!

You can also consider incresing the context window size, this can be done with:

```bash
ollama run llama3.1:latest
/set parameter num_ctx 8192
/save llama3.1:latest-8k
ollama serve
```

You access the model with `llama3.1:latest-8k` afterwards.