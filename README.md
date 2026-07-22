# AI Memory Assistant for Dementia Care

### A Personalised Voice-Activated AI Assistant for Dementia Care Using Retrieval Augmented Generation

> Built using RAG, LLaMA 3.3 70B, ChromaDB, Sentence Transformers and Gradio

---

## Problem

Dementia and Alzheimer's patients progressively lose the ability to recall
names, faces and life events. Caregivers cannot be available 24 hours a day
to answer the same questions repeatedly. This assistant provides an AI that
remembers the patient's life for them and responds warmly on demand.

---

## How It Works


https://github.com/user-attachments/assets/78490266-c734-44a4-bf13-127d9fb25689



```
Family uploads memories -> Stored as vector embeddings in ChromaDB
Patient asks question   -> Semantic search retrieves relevant memories
LLaMA 3.3 70B           -> Generates warm personalised response
Output                  -> Text + Voice + Photo shown simultaneously
```
---

## Features

- Related photo displayed alongside answer
- Family members can add new memories in real time
- Voice input using Groq Whisper API
- Text input through Gradio interface
- Warm personalised responses using LLaMA 3.3 70B
- Voice output using Google Text to Speech
- No model training required - uses RAG

---

## Tech Stack

| Component | Technology |
|---|---|
| RAG Pipeline | Built from scratch (no LangChain/LlamaIndex) |
| LLM | ![LLaMA 3.3 70B](https://img.shields.io/badge/LLaMA%203.3%2070B-6E40C9?style=flat&logo=meta&logoColor=white) via ![Groq API](https://img.shields.io/badge/Groq%20API-F55036?style=flat&logo=groq&logoColor=white) |
| Embeddings | ![Sentence Transformers](https://img.shields.io/badge/Sentence%20Transformers-FF6F00?style=flat&logo=huggingface&logoColor=white) |
| Vector Database | ![ChromaDB](https://img.shields.io/badge/ChromaDB-5A45FF?style=flat&logo=databricks&logoColor=white) (local) |
| Voice Input | ![Groq Whisper API](https://img.shields.io/badge/Groq%20Whisper%20API-F55036?style=flat&logo=groq&logoColor=white) |
| Voice Output | ![gTTS](https://img.shields.io/badge/gTTS-4285F4?style=flat&logo=google&logoColor=white) + ![Pygame](https://img.shields.io/badge/Pygame-00AA00?style=flat&logo=pygame&logoColor=white) |
| Images | ![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75FF?style=flat&logo=google-gemini&logoColor=white) (pre-generated) |
| Interface | ![Gradio](https://img.shields.io/badge/Gradio-FF6F00?style=flat&logo=gradio&logoColor=white) |
| Backend | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) + ![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?style=flat&logo=jupyter&logoColor=white) |

---
## Setup

1. Clone this repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Get a free API key from console.groq.com
4. Create a `.env` file in the project folder:
```
GROQ_API_KEY=your_key_here
```
5. Open `Al Dementia project.ipynb` in Jupyter
6. Run all cells top to bottom

---

## References

-Chen et al. (2025). The Role of AI-Driven Personal Assistants in Geriatric Care. Annals of Gerontology and Geriatric Research.  

-Li et al. (2020). A Personalised Voice-Based Diet Assistant for Caregivers of Alzheimer Disease. Journal of Medical Internet Research, 22(9).

-Lewis et al. (2020). Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks. NeurIPS 2020.
  









