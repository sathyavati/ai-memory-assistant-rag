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
- No model training required — uses RAG

---

## Tech Stack

| Component | Technology |
|---|---|
| LLM | LLaMA 3.3 70B via Groq API |
| Embeddings | Sentence Transformers all-MiniLM-L6-v2 |
| Vector Database | ChromaDB (local) |
| Voice Input | Groq Whisper API |
| Voice Output | gTTS + pygame |
| Images | Google Gemini (pre-generated) |
| Interface | Gradio |
| Backend | Python + Jupyter Notebook |

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

- Lewis et al. RAG for Knowledge-Intensive NLP Tasks. NeurIPS 2020
- Reimers and Gurevych. Sentence-BERT. EMNLP 2019
- WHO. Dementia Fact Sheet. 2023









