# Dataset

## Important Note

All data used in this project including memory statements and photographs
are artificially created for demonstration purposes only. No real patient
data, real personal photographs or real medical information has been used
anywhere in this project. This was a deliberate decision to protect privacy
during academic demonstration.

---

## 1. Memory Dataset

### Overview
The memory dataset consists of manually written autobiographical statements
simulating the personal life history of a fictional dementia patient. These
statements were written by the project team to represent the kind of
information a real family would provide for their patient.

### Memory Statements

| # | Category | Memory |
|---|---|---|
| 1 | Child | Ashwathy is your daughter. She lives in Kochi. She got married in 2015. |
| 2 | Spouse | Your husband Mohan loved cricket and watched every India match. He loved gardening. |
| 3 | Occupation | You worked as a school teacher for 30 years. Your favourite subject was Math. |
| 4 | Grandchildren | Your grandson Arjun is 8 years old. He loves football. |
| 5 | Birthplace | You were born in Kozhikode and grew up near the old market. You loved eating biriyani. |
| 6 | Friendship | Your best friend is Sunita. You have known her since college. She visits every Diwali. |
| 7 | Pets | You have a dog named Titu. He is a golden retriever and loves to play fetch. |
| 8 | Preferences | Your favourite movie is Nadodikkatu and you used to watch it. |

### Properties

| Property | Value |
|---|---|
| Total memories | 8 |
| Format | Plain English text |
| Language | English |
| Written in | Second person (you, your) |
| Created by | Project team (simulated) |
| Real patient data | No |
| Embedding model | all-MiniLM-L6-v2 |
| Embedding dimensions | 384 |
| Storage | ChromaDB vector database (local) |

---

## 2. Photo Dataset

### Overview
All photographs used in this project were artificially generated using
Google Gemini's image generation feature. No real personal photographs
of any real person were used. Each image was generated using a descriptive
text prompt.

### Generated Photos

| Filename | Prompt Used | Represents |
|---|---|---|
| ashwathy.jpg | A young Malayali woman smiling in Kochi | Patient's daughter |
| mohan.jpg | An elderly Malayali man outside his house in Kerala | Patient's husband |
| arjun.jpg | A young boy riding cycle outside his home in Kochi | Patient's grandson |
| wedding.jpg | A traditional Keralite wedding ceremony | Daughter's wedding |
| working.jpg | An elderly female school teacher | Patient's teaching career |

### Properties

| Property | Value |
|---|---|
| Total photos | 5 |
| Format | JPG |
| Generated using | Google Gemini |
| Real photographs | No |
| Storage | Local device only |
| Uploaded to GitHub | No (excluded via .gitignore) |

### Why AI Generated Photos

Real personal photographs were intentionally avoided for two reasons:

1. Privacy - using real faces of real people without consent is unethical
2. Academic demonstration - AI generated images are sufficient to demonstrate
   the photo retrieval feature without any privacy risk

In a real clinical deployment, actual family photographs would be uploaded
by caregivers through the Add Memory interface.

---

## 3. Voice Dataset

### Overview
No pre-recorded voice dataset was used. All voice input in this project
is live i.e the patient speaks directly into the microphone during real time
use. The Groq Whisper API transcribes the spoken question into text
on the fly.

| Property | Value |
|---|---|
| Type | Live real time input |
| Pre-recorded data | None |
| Transcription | Groq Whisper API |
| Language supported | English |

---

## 4. Why No Standard Dataset

There is no publicly available standard dataset for personal autobiographical
memory because every patient's life is completely unique. A dementia
assistant by definition requires personalised data specific to one individual.

The innovation in this project is not the dataset itself but the RAG
architecture that allows any family to create and personalise their own
dataset for their patient through a simple text interface with no technical
knowledge required.

---

## 5. Scalability

The system is designed to scale with more data over time:

| Scale | How |
|---|---|
| Add new memories | Through Add Memory tab in the app |
| Add new photos | Drop photo in data/photos folder and update keyword map |
| Multiple patients | Create a separate ChromaDB collection per patient |
| Large datasets | Same code works for 8 or 8000 memories without changes |

---

## 6. Privacy and Ethics

| Data Type | Where Stored | Uploaded to Cloud | Real Data |
|---|---|---|---|
| Memory statements | ChromaDB (local) | No | No (simulated) |
| Photographs | Local folder | No | No (AI generated) |
| Voice input | Not stored | Groq API only | Yes (live input) |
| API responses | Not stored | Groq API only | Yes (live) |

In a real clinical deployment all data would remain on the local device
using a fully offline model like Ollama, ensuring complete patient
data privacy under HIPAA and India's Digital Personal Data Protection
Act 2023.
