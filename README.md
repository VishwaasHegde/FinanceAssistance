Pre-requisites
1. Install [Ollama](https://ollama.com/download)
2. In the command prompt: run `ollama pull llama3.2` and optionally `ollama serve`
3. git clone the project
4. Create a conda virtual environment and `pip install -r requirements.txt`
4. Place [qdrant]() folder in the project folder
5. Place [peft-sent-model]() folder in `src/backend` folder
6. Execute `uvicorn financeengine:app --host 0.0.0.0 --port 8025` in `src/backend` folder (in another terminal)
7. Execute `streamlit run financechatclient.py` in `src/frontend` folder (in another terminal)
8. Open `http://localhost:8501/`
