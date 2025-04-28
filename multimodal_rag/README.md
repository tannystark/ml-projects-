# Multimodal Retrieval Augmented Generation (RAG) System

## Overview
This project implements a Multimodal Retrieval Augmented Generation (RAG) system that enhances query answering by retrieving both **text** and **image** information from a knowledge base (Wikipedia) and feeding them into a Large Language Model (LLM) to generate enriched responses.

## System Architecture
User Query ➔ Embedding Creation ➔ Vector Search in Qdrant (Text + Image) ➔ Retrieved Context ➔ Prompt Construction via LlamaIndex ➔ LLM ➔ Final Answer

## Approach
- **Data Preparation**: Indexed Wikipedia text passages and image captions separately.
- **Embeddings**:
  - Text: Sentence Transformers (`all-MiniLM-L6-v2`)
  - Image: OpenAI CLIP model
- **Vector Database**: Used Qdrant for efficient similarity search.
- **Retrieval Pipeline**:
  - Encoded user query into text and image embeddings.
  - Retrieved top-k matches separately for text and images.
- **Answer Generation**:
  - Compiled retrieved content.
  - Used LlamaIndex to construct a prompt for the LLM.
  - Generated a final enriched answer.

## Sample Query Example
- **Query**: "Who was the first person on the moon?"
- **Retrieved Text**: "Neil Armstrong was the commander of Apollo 11 and the first man to walk on the Moon."
- **Retrieved Image Caption**: "Neil Armstrong stepping onto the lunar surface."
- **Generated Answer**: "Neil Armstrong was the first human to set foot on the Moon during NASA's Apollo 11 mission in 1969."

## Technologies Used
- Python
- SentenceTransformers
- OpenAI CLIP
- Qdrant Vector Database
- LlamaIndex
- HuggingFace Transformers
- Matplotlib (optional visualization)

## Results
- Text Retrieval Top-5 Recall: ~85%
- Image Retrieval Top-5 Recall: ~80%
- Final answers enriched by both textual and visual context.

## Key Learnings
- How to unify structured (text) and unstructured (image) data retrieval pipelines.
- Efficient vector search operations using Qdrant.
- Prompt design for retrieval-augmented LLM response generation.

## Future Improvements
- Combine text and image retrieval scores for weighted ranking.
- Build a simple front-end UI for real-time multimodal QA.
- Fine-tune retrieval models for domain-specific applications.
