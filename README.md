# 📚 RAG vs Non-RAG Question Answering System

This project demonstrates the difference between **Retrieval-Augmented Generation (RAG)** and **Non-RAG (pure LLM)** question answering using a machine learning book as the knowledge source.

It allows users to:

✅ Ask questions using **book context (RAG)**  
✅ Ask questions using **model knowledge only (Non-RAG)**  
✅ Compare accuracy and response quality  

---

## 🚀 Features

- 📄 Extracts text from PDF safely (handles corrupted pages)
- ✂️ Splits text into chunks for efficient retrieval
- 🔎 Creates semantic embeddings using Sentence Transformers
- ⚡ Stores embeddings using FAISS for fast similarity search
- 🤖 Uses FLAN-T5 for answer generation
- 🔁 Interactive CLI with RAG & Non-RAG modes

---

## 🧠 What is RAG?

**Retrieval-Augmented Generation (RAG)** improves answer accuracy by retrieving relevant context before generating an answer.

### ✔ RAG Workflow
1. User asks a question  
2. System retrieves relevant text from the PDF  
3. Context is provided to the model  
4. Model generates answer using that context  

### ✔ Non-RAG Workflow
- Model answers using **only pre-trained knowledge**

---

## 📂 Project Structure


.
├── RAG_AND_NON_RAG.ipynb
├── 2019BurkovTheHundred-pageMachineLearning.pdf
└── README.md


---

## ⚙️ Installation

Install required dependencies:

```bash
pip install pypdf sentence-transformers faiss-cpu transformers torch pymupdf
▶️ How to Run
1️⃣ Place the PDF in the project folder
2019BurkovTheHundred-pageMachineLearning.pdf
2️⃣ Run the notebook

Open and execute:

RAG_AND_NON_RAG.ipynb
3️⃣ Choose mode
1 → RAG (uses book context)
2 → Non-RAG (model knowledge)
4️⃣ Ask questions interactively
💡 Example Questions
📘 RAG Mode

What is supervised learning?

Explain overfitting.

What is gradient descent?

🤖 Non-RAG Mode

What is machine learning?

Explain neural networks.

What is bias vs variance?

🔍 How It Works
Step 1: Load PDF

Extracts text safely

Skips corrupted pages

Step 2: Chunk Text

Splits text into small segments for retrieval.

Step 3: Create Embeddings

Model used:

all-MiniLM-L6-v2
Step 4: FAISS Index

Stores vectors for fast semantic search.

Step 5: Generator Model

Model used:

google/flan-t5-base
📊 RAG vs Non-RAG Comparison
Feature	RAG	Non-RAG
Uses document context	✅	❌
More factual accuracy	✅	❌
Hallucination risk	Low	Higher
Domain-specific answers	Excellent	Limited
Requires embeddings	✅	❌
🎯 Use Cases

✅ Study assistant for textbooks
✅ Research document Q&A
✅ Enterprise knowledge retrieval
✅ Legal & policy document analysis
✅ Academic learning tools

⚠️ Common Issues & Fixes
❌ PDF loads but no text extracted

✔ Try another PDF
✔ Ensure it is not a scanned image

❌ FAISS installation errors
pip install faiss-cpu
❌ Slow first run

Models download during first execution.

🔮 Future Improvements

Add web UI (Streamlit / Gradio)

Support multiple documents

Add source citations in answers

Use larger LLMs for improved explanations

Add chat history & memory

👨‍💻 Author

Built to understand RAG vs LLM knowledge differences and modern AI retrieval systems.
