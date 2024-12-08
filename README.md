### Pre-requisites
1. Install [Ollama](https://ollama.com/download)
2. In the command prompt: run `ollama pull llama3.2` and optionally `ollama serve`
3. git clone the project
4. Create a conda virtual environment and `pip install -r requirements.txt`
5. Place [qdrant](https://drive.google.com/drive/folders/13o45mPZiRF6e55_D2TWLyXQL-sZuf3GF?usp=drive_link) folder in the project folder
7. Place [peft-sent-model](https://drive.google.com/drive/folders/1Qy5y_JOmklT39fF4U67Q15Nc37vf-2hP?usp=drive_link) folder in `src/backend` folder
8. Place [peft-sent-model](https://drive.google.com/drive/folders/1Qy5y_JOmklT39fF4U67Q15Nc37vf-2hP?usp=drive_link) folder in the Project folder (This is for the jupyter notebook)

### Install Qdrant
1. Install [Docker](https://docs.docker.com/desktop/setup/install/windows-install/)
2. In the project folder, run : `docker pull qdrant/qdrant`
3. The run `docker run -p 6333:6333 -p 6334:6334 -v ./qdrant_storage:/qdrant/storage:z qdrant/qdrant`

### For the UI / backend code (Not Jupyter)
1. Do the steps above (from 1 to 6) and Qdrant installation
2. Execute `uvicorn financeengine:app --host 0.0.0.0 --port 8025` in `src/backend` folder (in another terminal)
3. Execute `streamlit run financechatclient.py` in `src/frontend` folder (in another terminal)
4. Open `http://localhost:8501/`
