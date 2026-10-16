# Cynbit AI Lead Intelligence Assistant

## Project Overview

The Cynbit AI Lead Intelligence Assistant is a proof-of-concept application designed to analyze customer inquiries, calculate lead priority scores, retrieve relevant company service information, and generate AI-assisted recommendations and email drafts.

The project is implemented using Python in Google Colab.

## Objectives

- Analyze customer business inquiries.
- Assign transparent, rule-based lead priority scores.
- Retrieve relevant service descriptions using semantic search.
- Generate service recommendations and email drafts using an LLM.
- Evaluate service retrieval using sample customer inquiries.

## Key Features

### 1. Lead Scoring
Calculates a score out of 100 using business fit, urgency, budget clarity, and requirements clarity.

### 2. Semantic Service Retrieval
Uses Sentence Transformers to generate embeddings and FAISS to retrieve relevant service descriptions.

### 3. AI Recommendation Generation
Uses an LLM through the OpenRouter API to generate inquiry analysis, service recommendations, follow-up questions, and suggested email drafts.

### 4. Evaluation
Compares retrieved service categories with expected categories in a small synthetic test dataset.

## Technology Stack

- Python
- Google Colab
- Sentence Transformers
- FAISS
- NumPy
- Pandas
- OpenRouter API
- Retrieval-Augmented Generation (RAG)

## Project Files

- `project.ipynb` — Google Colab implementation.
- `cynbit_ai_lead_assistant.zip` — Supporting project data and evaluation files.
- `cynbit_services.json` — Service knowledge base.
- `cynbit_lead_evaluation.csv` — Evaluation results.

## How to Run

1. Open `project.ipynb` in Google Colab.
2. Run the notebook cells sequentially.
3. Install the required dependencies.
4. Load the service knowledge base and create the FAISS index.
5. Configure an available OpenRouter API key if LLM generation is required.
6. Run sample customer inquiries.
7. Review the lead scores, retrieved services, recommendations, and evaluation results.

## Data and Evaluation

The prototype uses sample service descriptions and synthetic customer inquiries. The evaluation is preliminary and should not be interpreted as proof of real-world business performance.

## Limitations

- Lead scoring uses manually defined rules and is not a trained sales-conversion prediction model.
- Retrieval quality depends on the service descriptions and test examples.
- LLM-generated recommendations require human review.
- Real business impact must be validated using appropriate data and testing.

## Security

API keys and confidential customer information must not be committed to the repository. Use private environment variables or approved secret-management mechanisms.

## Conclusion

This proof of concept demonstrates how semantic retrieval, rule-based scoring, and LLM-assisted generation can be combined to support business inquiry analysis and service recommendations.
