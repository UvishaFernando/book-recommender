# Semantic Book Recommender 📚

An intelligent, interactive book recommendation engine that goes beyond simple keyword matching. This project uses semantic vector search, zero-shot text classification, and sentiment analysis to help you find the perfect book based on the meaning of your query and the emotional tone you're looking for.

## ✨ Features

- **Semantic Vector Search:** Powered by HuggingFace embeddings (`all-MiniLM-L6-v2`) and ChromaDB. Describe what you want to read, and it finds books with matching plots!
- **Emotional Tone Filtering:** Uses a DistilRoBERTa model (`j-hartmann/emotion-english-distilroberta-base`) to score book descriptions across 7 emotions. Filter your recommendations by tones like *Happy, Sad, Surprising, Angry,* or *Suspenseful*.
- **Category Classification:** Groups books into simplified, distinct categories for easy browsing.
- **Interactive Dashboard:** A sleek, glass-themed web interface built entirely in Python using Gradio.

## 🛠️ Tech Stack

- **Frontend Interface:** [Gradio](https://gradio.app/)
- **Vector Database:** [Chroma](https://www.trychroma.com/)
- **Embeddings & Orchestration:** [LangChain](https://python.langchain.com/), `sentence-transformers`
- **NLP & Sentiment Analysis:** HuggingFace `transformers` pipeline
- **Data Processing:** Pandas, Jupyter Notebooks

## 📂 Project Structure

- `gradio-dashboard.py` - The main application script that launches the web interface.
- `vector-search.ipynb` - Explores LangChain and ChromaDB setup using HuggingFace embeddings.
- `text-classification.ipynb` - Cleans the dataset and categorizes the books.
- `sentiment-analysis.ipynb` - Generates emotional tone scores for every book description.
- `data-exploration.ipynb` - Initial Kaggle dataset download and missing-values analysis.

## 🚀 How to Run Locally

1. **Clone the repository.**
2. **Install dependencies:**
   Ensure you have PyTorch, LangChain, Transformers, Gradio, and Pandas installed.
   ```bash
   pip install langchain langchain-chroma langchain-openai sentence-transformers transformers gradio pandas python-dotenv
   ```
3. **Run the Dashboard:**
   Execute the main script in your terminal:
   ```bash
   python gradio-dashboard.py
   ```
4. **Open in Browser:**
   Click the local URL (usually `http://127.0.0.1:7860`) provided in your terminal to start exploring!