# Alasight
This project is created with intention to get a quick start guide on how to train a model on local using llama-2 and create a custom chat bot built on PDF documents you provide.
Prerequisites: langchain, FAISS(vectorstore), LLMs, chainlit.
This takes away the complexity of setting up OpenAI API keys and black box LLM that OpenAI keeps with itself.
Is also enables you to debug embeddings and visualise intermediate stages of LLM training.
This project uses FAISS as vector DB.
This project uses chainlit to help create chatgpt like UI to add fun to experimentation.

# Setup:
- Create python virtual environment in project directory. Example: python -m venv <project_parent_dir>/Alasight/env/.
- Activate virtual env. `source <project_parent_dir>/Alasight/env/bin/activate`
- Change directory to Alasight root directory.
- Run: `pip install -r requirements.txt`
- Download `llama-2-7b-chat.ggmlv3.q8_0.bin` from [huggingface](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main).

# Run from Alasight root directory:
- env/bin/python ingest.py (Takes a few minutes). The result of this command would be two files in vectorstores/db_faiss/index.faiss and vectorstores/db_faiss/index.pkl in Alasight root directory.
- chainlit run model.py -w
- You now should have a local instance of chatbot running on your system which is trained on Alation documents residing in data/ directory.
