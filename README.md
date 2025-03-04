Here’s a combined `README.md` for both **Version 1** and **Version 2** of your **Healthcare Chatbot** project. This document provides an overview of both versions, their features, setup instructions, and usage.

---

# Healthcare Chatbot

## Overview
This project consists of two versions of a **Healthcare Chatbot** designed to assist users with medical queries. Each version uses different approaches and technologies to provide accurate and context-aware medical answers.

---

## Versions

### **Version 1**
- **Approach**: Rule-based with Decision Tree Classifier and SVM.
- **Features**:
  - Symptom analysis and disease prediction.
  - Disease descriptions and precautionary measures.
  - Severity assessment of symptoms.
- **Tech Stack**:
  - Python, Pandas, Scikit-learn.
  - Decision Tree Classifier, Support Vector Machine (SVM).

---

### **Version 2**
- **Approach**: Retrieval-Augmented Generation (RAG) with OpenAI GPT and Pinecone.
- **Features**:
  - Medical and non-medical query handling.
  - Context-aware answers using OpenAI GPT.
  - Source attribution for medical answers.
  - Real-time communication via WebSocket.
- **Tech Stack**:
  - FastAPI (backend), Streamlit (frontend).
  - OpenAI GPT, LangChain, Pinecone.

---


## Setup Instructions

### **Version 1**
1. Clone the repository:
   ```bash
   git clone https://github.com/K-Tarunkumar/Healthcare-chatbot.git
   cd Healthcare-chatbot/chatbot\ version1
   ```

2. Install dependencies:
   ```bash
   pip install pandas scikit-learn
   ```

3. Run the chatbot:
   ```bash
   python chat_bot.py
   ```

---

### **Version 2**
1. Clone the repository:
   ```bash
   git clone https://github.com/K-Tarunkumar/Healthcare-chatbot.git
   cd Healthcare-chatbot
   ```

2. Set up a virtual environment:
   ```bash
   python -m venv venv
   ```

   - Activate the virtual environment:
     - On Windows:
       ```bash
       venv\Scripts\activate
       ```
     - On macOS/Linux:
       ```bash
       source venv/bin/activate
       ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:
   Create a `.env` file in the root directory with the following content:
   ```plaintext
   OPENAI_API_KEY=your_openai_api_key
   PINECONE_API_KEY=your_pinecone_api_key
   PINECONE_ENV=your_pinecone_environment
   ```

5. Run the backend:
   ```bash
   uvicorn medical_api:app --reload
   ```

6. Run the frontend:
   ```bash
   streamlit run app.py
   ```

---

## Usage

### **Version 1**
1. Run the `chat_bot.py` script.
2. Enter your symptoms when prompted.
3. The chatbot will:
   - Identify potential diseases.
   - Provide descriptions and precautions.
   - Assess symptom severity.

---

### **Version 2**
1. Open the Streamlit frontend in your browser (`http://localhost:8501`).
2. Enter your medical or general questions in the chat input box.
3. The chatbot will:
   - Answer medical queries using the RAG pipeline.
   - Answer general queries using OpenAI's GPT model.
4. Sources for medical answers (if available) will be displayed in the sidebar.

---

## Example Interaction (Version 1)
```
Enter the symptom you are experiencing: itching
Okay. From how many days?: 3
Are you experiencing skin_rash? (yes/no): yes
Are you experiencing nodal_skin_eruptions? (yes/no): no
You may have Fungal infection.
Description: Fungal infections are caused by fungi and can affect the skin, nails, and hair.
Take the following measures:
1) Keep the area clean
2) Apply antifungal cream
3) Consult a doctor
4) Avoid sharing personal items
```

---

## Example Interaction (Version 2)
```
User: What are the symptoms of diabetes?
Bot: Common symptoms of diabetes include frequent urination, excessive thirst, unexplained weight loss, fatigue, blurred vision, and slow-healing sores. You should consult a healthcare professional for a proper diagnosis.

Note: This information is for educational purposes only and does not constitute medical advice. Please consult with a healthcare professional for personalized medical guidance.
```

---

## Future Improvements
- **Expand Dataset**: Add more symptoms and diseases for better accuracy.
- **User Interface**: Build a GUI for Version 1 using Tkinter, Streamlit, or Flask.
- **Text-to-Speech**: Use `pyttsx3` to read out predictions and precautions.
- **Deploy**: Deploy Version 1 as a web application using FastAPI or Flask.

## GitHub Repository
GitHub Link: [https://github.com/K-Tarunkumar/Healthcare-chatbot.git](https://github.com/K-Tarunkumar/Healthcare-chatbot.git)
