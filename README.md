# 📚 Semantic Book Recommender with LLMs

This project uses Large Language Models (LLMs) and Vector Databases to build a recommendation engine.

---

## 🌟 Key Features
* **Semantic Search:** Find books by describing a plot, a feeling, or a specific topic in natural language.
* **Vectorized Knowledge:** Uses OpenAI Embeddings to transform text into 1536-dimensional vectors for precise mathematical comparison.
* **Metadata Enrichment:** Search results include rich data such as ISBN, publication year, authors, and thumbnails.

---

## 🏗️ Technical Architecture



### 1. Data Processing Pipeline
* **Dataset:** 7k books with metadata sourced from [Kaggle](https://www.kaggle.com/datasets/dylanjcastillo/7k-books-with-metadata).
* **Document Loading:** Used `DataFrameLoader` to maintain a 1:1 relationship between book records and searchable documents.
* **Strategic Splitting:** Analyzed the dataset to find the maximum description length (**5,800 characters**) to ensure the `CharacterTextSplitter` keeps each book's context intact.

### 2. Vector Database & Retrieval
* **Vector Store:** Built with **ChromaDB** to index and persist embeddings locally.
* **Embeddings:** Powered by OpenAI's `text-embedding-3-small` model.

---

## 🚀 Usage

### Installation & Setup
1. Clone the repository and install dependencies:
   ```bash
   pip install langchain langchain-openai langchain-community chromadb pandas python-dotenv
2. Create a .env file and add your key:

OPENAI_API_KEY=your_api_key_here
