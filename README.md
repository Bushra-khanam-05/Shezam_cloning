# 🎵 Shazam Clone: Audio Transcription & Subtitle Search

## Project Overview

This project is dedicated to creating an **AI-powered search system** that combines **audio-to-text conversion** with **interactive search functionalities**. By leveraging state-of-the-art technologies like search engines, vector embeddings, speech-to-text models, and subtitle processing, the project facilitates efficient retrieval of information and in-depth media analysis.

## Project Objective

The goal is to develop an advanced search engine algorithm that retrieves subtitles based on user queries with high precision. This is achieved by integrating natural language processing (NLP) and machine learning techniques, and by contrasting:

- **Keyword-based Search Engines:** Relying on exact keyword matches between user queries and indexed documents.
- **Semantic Search Engines:** Understanding the context and underlying meaning of both queries and documents, surpassing simple keyword matching.

## Core Implementation Steps

### 1. Data Preprocessing

- Extract and clean subtitle data by removing elements like timestamps and unnecessary punctuation.
- Optionally, reduce the dataset size (e.g., use only 30% of the data) when compute resources are limited.

### 2. Text Vectorization

- Transform subtitle text into vector embeddings using techniques such as:
  - **Bag of Words (BOW) / TF-IDF** for traditional keyword-based search.
  - **BERT-based SentenceTransformers** for capturing semantic nuances in text.

### 3. Document Chunking

- Divide long subtitle files into smaller, manageable chunks to retain context.
- Employ overlapping windows to minimize information loss during the segmentation process.

### 4. Storing Embeddings in ChromaDB

- Save the vector representations of the subtitle chunks in ChromaDB, enabling rapid and efficient similarity searches.

### 5. Retrieving Relevant Documents

- Convert the user’s audio query into text using an ASR model (e.g., AssemblyAI).
- Vectorize the resulting text and compute cosine similarity with the stored subtitle embeddings.
- Rank and return the most relevant subtitle segments to the user.

## Notebooks & Descriptions

### 1. Audio_2_Text.ipynb

- Converts audio files to text using speech recognition models like AssemblyAI.
- Useful for applications such as transcription services, podcast analysis, and enhancing accessibility.

### 2. Chroma_db_Embeddings_V2.ipynb

- Utilizes ChromaDB for creating and managing vector embeddings.
- Supports efficient similarity searches, semantic retrieval, and document indexing.
- Applicable in AI-powered search engines and question-answering systems.

### 3. Gradio_Search_Engine_Demo.ipynb

- Provides an interactive search engine demo built with Gradio.
- Allows users to test queries interactively using keyword-based, semantic, or hybrid search models.
- Integrates with ChromaDB embeddings to facilitate intelligent retrieval.

### 4. Search_Engine_Extracting_Data.ipynb

- Focuses on extracting, scraping, and indexing data for the search engine.
- Handles text preprocessing, tokenization, and structuring of documents.
- Ideal for applications like web crawling, automated indexing, and structured data retrieval.

### 5. Shazam_Clone_Search_Engine.ipynb

- Develops a music recognition system akin to Shazam.
- Capable of identifying audio clips, speeches, or sound patterns from sample audio inputs.

### 6. Subtitles_Chunking.ipynb

- Processes subtitle files by splitting them into smaller, context-preserving segments.
- Facilitates applications like automatic subtitle generation, video search indexing, and multilingual translation.
- Incorporates time-stamping, sentence segmentation, and embedding generation for efficient information retrieval.

### 7. Testing_Search_Mechanism.ipynb

- Evaluates and compares the performance of different search algorithms.
- Tests methods including BM25, TF-IDF, and vector-based retrieval to determine the best ranking models.

## Libraries Utilized

- **gradio**
- **assemblyai**
- **pydub**
- **python-dotenv**
- **chromadb**
- **sentence-transformers**

## Applications

- **Multimodal Search Engines:** Integrates text, audio, and vector embeddings to offer intelligent search capabilities.
- **Audio & Music Recognition:** Implements a Shazam-like system for identifying songs and various sound patterns.
- **Semantic Search & NLP:** Utilizes vector embeddings to drive advanced document retrieval and AI-driven search functionalities.
- **Interactive Demos & UI:** Leverages Gradio to provide a user-friendly interface for testing search queries.
- **Video & Subtitle Processing:** Extracts and structures subtitles to enhance accessibility and enable efficient video search indexing.

## Summary

This project unifies advanced AI search technologies with robust text/audio processing techniques to deliver a powerful media analysis tool. Utilizing vector databases, NLP models, and sophisticated ranking algorithms, it enables efficient transcription, subtitle retrieval, and interactive search experiences. 🚀

---

### Contribution

Contributions are welcome! Feel free to open issues, suggest improvements, or contribute directly to enhance this project. Let me know if any modifications are needed. 😊
