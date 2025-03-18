# 🧠 AI-Powered Mental Health Chatbot (Flask + RAG)

This project is a **compassionate AI therapist chatbot** that provides **empathetic and structured mental health support** using **RAG (Retrieval-Augmented Generation)** and **Llama-2-7B/Mistral-7B**.

## 🚀 Features
👉 **Context-aware Responses** using RAG (FAISS + SentenceTransformers)  
👉 **LLM-powered Chatbot** (Llama-2-7B / Mistral-7B)  
👉 **Flask API for Easy Integration**  
👉 **Supports Frontend & Mobile Apps**  
👉 **Evaluates Response Quality** using BLEU, ROUGE, and Perplexity  

---

## 🛠️ Installation

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/yourusername/mental-health-chatbot.git
cd mental-health-chatbot
```

### **2️⃣ Install Dependencies**
```bash
pip install flask flask-cors torch transformers sentence-transformers faiss-cpu evaluate nltk
```

### **3️⃣ Download & Load the Model**
If you trained your model in **Google Colab**, download it and place it in the project folder:
```
mental-health-chatbot/
 ├── saved_model/
 │   ├── config.json
 │   ├── pytorch_model.bin
 │   ├── tokenizer.json
 │   ├── tokenizer_config.json
 │   └── special_tokens_map.json
 ├── app.py
 ├── README.md
```

---

## 🏃‍♂️ Running the Flask API
### **Start the API**
```bash
python app.py
```
Server will start at **`http://0.0.0.0:5000`**

---

## 🔗 API Usage
### **Endpoint: `POST /chat`**
**Request Example:**
```json
{
  "message": "I'm feeling very anxious lately. What should I do?"
}
```

**Response Example:**
```json
{
  "response": "I understand. Many people in similar situations have found deep breathing exercises and mindfulness helpful. Would you like to explore more techniques?"
}
```

---

## 📊 Evaluating Chatbot Responses (BLEU, ROUGE, Perplexity)

The chatbot's responses are evaluated using **BLEU, ROUGE, and Perplexity** to measure **accuracy, relevance, and confidence**.

### **🔹 BLEU Score (Bilingual Evaluation Understudy)**
- Measures how **similar the chatbot’s response is to a reference response**.
- **Higher BLEU = More accurate** chatbot responses.
- Used mainly for **word-for-word similarity**.

**Your BLEU Score:** `0.1281` (12.81% word similarity)

---

### **🔹 ROUGE Score (Recall-Oriented Understudy for Gisting Evaluation)**
- Measures **how much relevant information** from the reference response is included.
- **Higher ROUGE = Better coverage** of the original response.
- Used mainly for **content overlap**.

**Your ROUGE Score:** `0.3883` (38.83% content match)

---

### **🔹 Perplexity**
- Measures **how confident the chatbot is** in its response.
- **Lower Perplexity = More confident model** (Perplexity of `2-10` is considered good).
- **High perplexity** means the chatbot is **unsure about its response**.

**Your Perplexity Score:** `2.6409` (Confident and fluent response)

---

