<h1 align="center">
Langchain Basic RAG Implementation
</h1>

This implementation conducts RAG on whatever knowledge base is stored inside the _docs_source_ folder. For demonstration purposes, the knowledge base currently being used is the full AWS Documentation in the form of Markdown files.

<h3 align="center">
Setup
</h3>

Create an OpenAI account (if you don't already have one) along with an OpenAI key, and set the secret OpenAI key in the _environment.yml_ file under the **variables** section:

```yml
variables:
    OPENAI_API_KEY: ENTER_API_KEY_HERE
```

Create a Conda virtual environment from the _environment.yml_ file:

```shell
conda env create -f environment.yml
```

Activate the Conda environment:

```shell
conda activate llm-rag
```

<h3 align="center">
Run
</h3>

Create the Chroma DB by executing the _create_database.py_ file. This will populate the _chroma_ folder with the database representing the embeddings (this only needs to be done once):

```shell
python create_database.py
```

Query the database and generate a response from the LLM. Example:

```shell
python query_data.py "How can I set up an Amazon RDS Proxy database proxy?"
```
