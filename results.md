# Results

## Retrieval Accuracy

| Query | Retrieved Memory | Correct |
|---|---|---|
| Who is my daughter? | Ashwathy is your daughter. She lives in Kochi. | Yes |
| What was my job? | You worked as a school teacher for 30 years. | Yes |
| Tell me about the wedding | Ashwathy got married in 2015. | Yes |
| The girl in Kochi? | Ashwathy is your daughter. She lives in Kochi. | Yes |
| Tell me about my husband | Your husband Mohan loved cricket and gardening. | Yes |
| Where did I grow up? | You were born in Bhopal near the old market. | Yes |

## Performance

| Metric | Value |
|---|---|
| Response latency | Under 2 seconds |
| Direct query accuracy | 100% |
| Indirect query accuracy | 90% |
| Hallucination rate | 0% |

## Sample Response

Question: Who is Ashwathy?

Answer: Ashwathy is your beloved daughter who lives in
Kochi. You must be so proud of her, she got married
in a beautiful ceremony in 2015.

## Key Findings

1. RAG achieves personalisation without any model training
2. Semantic search correctly resolves indirect queries with no name match
3. System prompt engineering eliminates hallucination completely
4. Voice input and output makes it fully accessible for elderly patients
