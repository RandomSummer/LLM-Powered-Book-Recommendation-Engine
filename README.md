# 📚 LLM-Powered-Semantic-Book-Recommendation-Engine
 

### LLM-Powered Vector Search || Text-Embeddings || Sentimental-Analysis || Real-Time Gradio UI

This project implements a **semantic recommendation engine** that suggests books based on meaning, not just keywords.  
Using **Large Language Models (LLMs)**, vector embeddings, similarity search, and an interactive Gradio dashboard, the system provides intelligent, context-aware book recommendations.

---

## 🚀 Features

- **Semantic Embeddings**: Converts book descriptions into dense LLM-based embeddings.
- **Vector Similarity Search** using Chroma/FAISS.
- **Data Cleaning & Preprocessing Pipeline**.
- **Text Classification Module**   (genre prediction).
- **Interactive Gradio Dashboard** for real-time recommendations.
- **Modular, production-ready Python application**.

---

## 🏗️ Project Architectured

```
User Query ─► LLM Embedding ─► Vector Search ─► Ranked Books ─► Gradio UI
                         │
                         └──► Text Classification (optional)
```

---

## 📁 Project Folder Structure

```
llm-Book-Recommender/
│
│--  raw_books.csv
│--  cleaned_books.csv
│
│── src/
│   ├── preprocessing.py
│   ├── embeddings.py
│   ├── vector_store.py
│   ├── recommender.py
│   ├── classifier.py
│   └── utils.py
│
│── models/
│   └── classifier_model.pkl
│
│── notebooks/
│   └── analysis.ipynb
│
│── gradio-dashboard.py
│── requirements.txt
│── README.md
│── .gitignore
│── .venv/
```

---

## 🛠️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/RandomSummer/LLM-Powered-Book-Recommendation-Engine.git
cd LLM-Powered-Book-Recommendation-Engine
```

### 2. Create a virtual environment
```bash
python -m venv .venv
```

### 3. Activate environment  
**Windows:**
```bash
.\.venv\Scripts\activate
```

**Mac/Linux:**
```bash
source .venv/bin/activate
```

### 4. Install dependencies
```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### **Run the Gradio Dashboard**
```bash
python gradio-dashboard.py
```

The interface will start on:
```
http://127.0.0.1:7860
```

There you can:
- Enter book title / topic / description  
- View top semantic matches  
- See similarity score and metadata  
- Explore through a responsive UI  

---

## 🧠 How it Works (Detailed Architecture)

```
                   ┌────────────────────────────┐
                   │        Raw Dataset         |
                   └───────────────┬────────────┘
                                   │
                          Data Cleaning
                                   │
                                   ▼
                         Cleaned Book Data
                                   │
                                   ▼
               ┌──────────────── Embedding Model ────────────────┐
               │                (Sentence Transformer / LLM)     |
               └──────────────────────┬──────────────────────────|
                                      │
                                      ▼
                           Vector Database (Chroma)
                                      │
                                      ▼
                               Similarity Search
                                      │
                         ┌────────────┴─────────────┐
                         │   Optional Classifier    |
                         └────────────┬─────────────┘
                                      │
                                      ▼
                                   Output
                                      │
                                      ▼
                          Gradio Interactive Dashboard
```

---

## 🖼️ Screenshots

### 📌 Dashboard Home  
*(Replace with your own screenshot)*  
![Dashboard Screenshot](./assets/dashboard.png)

### 📌 Recommendation Results  
*(Replace with your screenshot)*  
![Results Screenshot](./assets/results.png)

---

## 📦 Requirements

See `requirements.txt` or the list below:

```
gradio
pandas
numpy
scikit-learn
sentence-transformers
chromadb
faiss-cpu
tqdm
python-dotenv
```

---

## 🤝 Contributing

Pull requests are welcome!  
For major changes, please open an issue first to discuss what you'd like to improve.

---

## ⭐ Support

If you like this project, consider giving the repository a **star ⭐ on GitHub**.
