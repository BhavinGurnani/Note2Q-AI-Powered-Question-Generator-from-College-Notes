# Note2Q-AI-Powered-Question-Generator-from-College-Notes
AI-powered question generation system using Retrieval-Augmented Generation (RAG) to create chapter-wise academic questions from notes and lecture materials.
The project is built using a Retrieval-Augmented Generation (RAG) architecture, ensuring that generated questions are context-aware, document-grounded, and accurate.

This system enhances personalized learning, exam preparation, and self-assessment by transforming static notes into interactive study material.

# 🎯 Problem Statement

Traditional Large Language Models (LLMs):

Are general-purpose and not domain-specific.

Can hallucinate content not present in source material.

Cannot dynamically process newly uploaded academic documents.

Note2Q solves these limitations by:

Processing user-uploaded documents. (PPT, PDF, DOCX)

Performing semantic retrieval over document chunks.

Generating questions strictly grounded in retrieved content.

Reducing hallucination through retrieval conditioning.

# 🧠 System Architecture

The system follows a structured Retrieval-Augmented Generation pipeline:

# 1️⃣ Resource Collection

Supports multiple academic formats:

PPTX (Lecture Slides)

PDF (Notes)

DOCX (Study Material)

# 2️⃣ Text Extraction

PPTX → python-pptx

PDF → PyPDF2

DOCX → python-docx

Extracted text is aggregated into a unified corpus.

# 3️⃣ Text Preprocessing

Lowercasing text

Removing special characters and punctuation

Stopword removal

Whitespace normalization

This ensures clean and consistent input for embedding generation.

# 4️⃣ Chapter-wise Chunking

Documents are divided into logical chapter-based sections to:

Preserve contextual relationships

Improve semantic retrieval accuracy

Enable topic-focused question generation

# 5️⃣ Embedding & Indexing

Embedding Model: all-MiniLM-L6-v2 (SentenceTransformers)

Lightweight and efficient

Converts document chunks into dense vector embeddings

Enables semantic similarity search

# 6️⃣ Retrieval Mechanism

User query is embedded

Cosine similarity is computed against indexed document chunks

Most relevant content is retrieved

This ensures document-grounded generation.

# 7️⃣ Question Generation

Generative Model: microsoft/DialoGPT-medium

Transformer-based conversational model

Generates natural, human-like academic questions

Conditioned on retrieved context

# 🔥 Key Features

Chapter-wise question generation.

Context-aware semantic retrieval.

Reduced hallucination via grounding.

Flashcard generation for quick revision.

Exam simulation & mock test support.

Personalized learning assistance.

# 🛠 Tech Stack

Python

Hugging Face Transformers

SentenceTransformers

PyPDF2

python-pptx

python-docx

NumPy

Scikit-learn

# 📚 Use Cases

Self-assessment & practice

Exam preparation

Personalized learning

Teacher assistance

Academic revision

# 🔮 Future Improvements

Fine-tuning domain-specific transformer models.

Integration with vector databases. (FAISS / Pinecone)

Web deployment using Streamlit or Flask.

Difficulty-level adaptive question generation.

Multi-language academic support.

# 🏆 Project Significance

Note2Q demonstrates:

Practical implementation of Retrieval-Augmented Generation.

Real-world NLP pipeline design.

Document-grounded LLM architecture.

Application of semantic embeddings in educational technology.


This project bridges the gap between static academic notes and intelligent AI-driven learning systems.
