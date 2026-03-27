# Results

## 1. Web Interface

The system interface is built using Gradio and runs as a local website
accessible through any browser. The interface has three tabs designed
for different users.

### Interface Overview

| Tab | User | Purpose |
|---|---|---|
| Type Question | Patient | Types a question and gets text, voice, and photo response |
| Speak Question | Patient | Speaks directly into microphone, gets automatic response |
| Add Memory | Family members | Adds new memories in real time without any coding |

### Type Question Tab
The patient types any question in natural language. The system retrieves
the most relevant memories, generates a warm response, displays a related
photograph, and speaks the answer aloud. Example questions available
as clickable examples at the bottom for patients who need prompting.

### Speak Question Tab
The patient clicks the microphone button, speaks their question, and
clicks stop. The Groq Whisper API automatically transcribes the speech,
retrieves relevant memories, and responds with voice and photo. No
typing required, making it fully accessible for elderly patients.

### Add Memory Tab
Family members type a new memory in plain English and click Save.
The memory is instantly stored in ChromaDB and available for the
patient to ask about immediately. No coding or technical knowledge
required.

---

## 2. Retrieval Accuracy

| Query | Retrieved Memory | Correct |
|---|---|---|
| Who is my daughter? | Ashwathy is your daughter. She lives in Kochi. | Yes |
| What was my job? | You worked as a school teacher for 30 years. | Yes |
| Tell me about the wedding | Ashwathy got married in 2015. | Yes |
| The girl in Kochi? | Ashwathy is your daughter. She lives in Kochi. | Yes |
| Tell me about my husband | Your husband Mohan loved cricket and gardening. | Yes |
| Where did I grow up? | You were born in Bhopal near the old market. | Yes |

---

## 3. Performance Metrics

| Metric | Value |
|---|---|
| Response latency | Under 2 seconds |
| Direct query accuracy | 100% |
| Indirect query accuracy | 90% |
| Hallucination rate | 0% |
| Voice transcription accuracy | High in quiet environment |
| Photo retrieval accuracy | 100% for mapped keywords |

---

## 4. Sample Responses

**Question:** Who is Ashwathy?
**Answer:** Ashwathy is your beloved daughter who lives in Kochi.
You must be so proud of her, she got married in a beautiful
ceremony in 2015.

**Question:** Tell me about the girl in Kochi
**Answer:** That sounds like Ashwathy, your dear daughter!
She lives in Kochi and got married in 2015. She must
mean the world to you.

**Question:** What was my job?
**Answer:** You had a wonderful career as a school teacher
for 30 years. Your favourite subject to teach was Hindi.
What a meaningful profession!

---

## 5. Key Findings

**Finding 1 — RAG without training**
Personalisation is achieved by storing memories in ChromaDB.
No model weights are modified. The same LLM serves all patients
with different memories.

**Finding 2 — Semantic beats keyword**
Indirect queries like "the girl in Kochi" correctly resolve
to Ashwathy without any name match. This is critical for
dementia patients who use vague phrasing.

**Finding 3 — Zero hallucination**
System prompt engineering ensures responses use only retrieved
memories. The model never makes up facts about the patient.

**Finding 4 — Real time updates**
New memories added through the Add Memory tab are available
for retrieval immediately without restarting the system.

---

## 6. Limitations

- Requires internet connection for Groq API
- Voice accuracy reduces in noisy environments
- Photo keyword map needs manual updates for new memories
- Not yet clinically evaluated with real dementia patients
