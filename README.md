# Chat with Audio
A simple Voice RAG (Retrieval-Augmented Generation) system using Deepseek, LangChain, and Streamlit to chat with audio files and answer complex questions about them.


## 🚀 Features

- **Voice/Audio Interface**: Upload or stream audio (e.g., podcasts, interviews, lectures).  
- **RAG Pipeline**: Retrieve relevant content from audio transcripts or embeddings to augment responses.  
- **Embeddings & Vector Search**: Audio is transcribed/embedded, and content is stored in a vector database for fast similarity-based retrieval.  
- **LLM Response Generation**: Combine retrieved context + user query to generate coherent answers or summaries.  
- **Interactive UI**: (Optional) Web interface (e.g., Streamlit) for uploading audio, asking questions, and viewing results.  
- **Multimodal Ready**: Leverages state-of-the-art transcription, embedding, and vector-search tools (see tutorials). :contentReference[oaicite:1]{index=1}

## 🧠 System Overview
Pipeline:
- Audio ingestion – User uploads audio file or records via microphone.
- Transcription/chunking – Convert audio to text (via API or model), then chunk into manageable segments.
- Embedding & storage – Generate embeddings for chunks and store in a vector database (e.g., Chroma, Qdrant).
- User query – User types (or speaks) a question about the audio content.
- Retrieval – Convert query to embedding; retrieve top relevant chunks via vector search.
- Generation – Feed retrieved context + query into an LLM (e.g., OpenAI GPT‑3.5 or GPT-4) to generate answer, summary or follow-up.
- Response/Output – Return answer in text (and optionally speak the answer via TTS).

# Pre-requisites
Install Ollama on your local machine from the [official website](https://ollama.com/). And then pull the Deepseek model:

```bash
ollama pull deepseek-r1:8b
```

Install the dependencies using pip:

```bash
uv add -r requirements.txt
```

# Run
Run the Streamlit app:

```bash
streamlit run voice_rag.py
```


Audio can be generated from https://www.openai.fm/.


## 🧑‍🎓 Author

**👨‍💻 Jay Rathod**  
*Software Engineer | AI & ML Trainer*  
📍 Ahmedabad, India  

🔗 [LinkedIn](https://www.linkedin.com/in/rathodjay3497/) | [GitHub](https://github.com/JayRathod341997)
