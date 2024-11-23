# Clearfeed Internship Task - Knowledge Retrieval System

A machine learning-based retrieval system for searching and ranking Clearfeed documentation URLs in response to user queries, with the option for answer generation using LLMs. Below, you'll find all the necessary information to get started. 🚀

---

## 📂 Project Structure

- **`assignment.ipynb`**: The main Jupyter Notebook for this assignment, which includes:
  - 📄 **Markdown Cells**: Descriptions, explanations, and context for the problem.
  - 🖥️ **Code Cells**: Functional blocks implementing the solution or performing analysis.
  - 📊 **Outputs**: Results of executed code for visualization or validation.

---

## 🛠️ Setup Instructions

Follow these steps to set up and run the project locally:

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>

2. Install Dependencies: Make sure you have Python and Jupyter Notebook installed. Create a virtual environment and install the required packages:
   ```bash
   pip install -r requirements.txt



## ✨ What I Used
  - 📝 TF-IDF (Term Frequency-Inverse Document Frequency) and Cosine Similarity 
  - ⚡  Latent Semantic Analysis(LSA)
  - 📈 Best Matching 25(BM25)
  - 🤖 T5-Bse LLM model was used to explore

## 📂 Comparison of all the NON - ML Approaches

| **Method**       | **TF-IDF + Cosine Similarity**                                                                                      | **LSA (Latent Semantic Analysis)**                                                                                               | **BM25**                                                                                                  | **T5 Base Model**                                                                                                                                     |
|-------------------|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Purpose**       | Ranks documents based on the importance of words in a query and document.                                         | Captures latent topics in the data to improve semantic understanding of queries and documents.                                | Focuses on exact term matches and relevance, prioritizing documents with frequent query terms.         | Generates natural language answers based on context, understanding both the query and the retrieved documents.                                      |
| **Best For**      | Simple queries, where exact word match and importance are key.                                                    | Understanding the meaning of queries in a broader context, even with different phrasing.                                      | Cases with a need for exact matches and fine-tuned relevance ranking for short or long documents.      | Complex queries requiring generated responses or summaries, especially when context is needed to answer questions.                                  |
| **Strengths**     | Easy to implement, quick, and interpretable.                                                                      | Captures semantic relationships, reducing reliance on exact word matches.                                                    | Handles relevance well, works effectively for keyword-heavy queries.                                   | Can generate coherent, context-aware answers; handles paraphrasing and nuances in language well; produces human-like responses.                    |
| **Weaknesses**    | Fails to capture semantic meaning and struggles with synonyms or paraphrased queries.                             | Requires computational resources and doesn’t work well with sparse or small datasets.                                         | Relies heavily on word overlap, which might ignore deeper context.                                     | Requires more computational resources; slower inference times; relies on large model weights and is harder to fine-tune for specific domain data.  |
| **Results (ClearFeed Example)** | Found relevant documents but couldn’t rank nuanced matches well.                                             | Produced more meaningful rankings, with better semantic understanding of the query.                                           | Retrieved highly relevant documents and assigned clear relevance scores based on common terms.         | Generated answers with context-specific relevance, but too short and too precise                   |
| **Overall Preference** | Preferred for straightforward retrieval tasks when minimal preprocessing is needed.                              | Ideal when semantic understanding and broader topic matching are necessary.                                                  | Best when term frequency and ranking precision are critical.                                           | Best for complex question answering tasks where the generated answer must fit the context, making it ideal for interactive applications.           |


