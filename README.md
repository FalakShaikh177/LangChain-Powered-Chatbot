
# LangChain-Powered Chatbot

![Python](https://img.shields.io/badge/python-3.10-blue) ![Streamlit](https://img.shields.io/badge/Streamlit-%E2%9C%93-orange) ![LangChain](https://img.shields.io/badge/LangChain-Enabled-green) ![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5--Turbo-pink)

A conversational AI chatbot built using **LangChain**, **OpenAI GPT-3.5-Turbo**, **Pinecone** vector database, and **Streamlit**. It handles chat memory, refines user queries, and retrieves contextually relevant answers.

---

## 🚀 Features

- 💬 Context-aware chatbot with memory using LangChain
- 🧠 Integrates vector search with **Pinecone** for relevant context retrieval
- 🔁 Refines user queries based on chat history
- 🖼️ Clean, interactive UI using **Streamlit** and `streamlit_chat`
- 🛡️ Modular structure via utility functions

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **Streamlit**
- **LangChain**
- **OpenAI GPT-3.5-Turbo**
- **Pinecone (for vector database search)**
- **streamlit_chat** (for conversation UI)

---

## 📦 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR-USERNAME/langchain-chatbot.git
   cd langchain-chatbot
   ```

2. **Create a virtual environment (optional)**
   ```bash
   python -m venv venv
   source venv/bin/activate      # macOS/Linux
   venv\Scripts\activate       # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Add your API keys**
   - Edit your code or create a `.env` file and load:
     ```env
     OPENAI_API_KEY=your_openai_api_key
     PINECONE_API_KEY=your_pinecone_api_key
     ```

---

## 🚀 Run the App

```bash
streamlit run app.py
```

---

## 📁 Project Structure

```
langchain-chatbot/
├── app.py                 # Main Streamlit application
├── utils.py               # Helper functions: query_refiner, find_match, etc.
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
└── .env                   # (Optional) API key storage
```

---

## 🤖 How It Works

1. User enters a query.
2. LangChain uses `ConversationBufferWindowMemory` to track the last 3 exchanges.
3. The user query is refined based on conversation context.
4. Pinecone fetches similar documents/contexts.
5. GPT-3.5-Turbo generates an answer using both context and query.

---

## 📌 Example

**User:**  
```
What's the eligibility criteria for the ML internship?
```

**Chatbot:**  
```
Based on the context, applicants must have completed at least 2 machine learning projects and be proficient in Python.
```

---

## 📜 License

This project is open-sourced under the **MIT License**.

---

## 🙌 Acknowledgments

- [LangChain](https://www.langchain.com/)
- [OpenAI](https://openai.com/)
- [Streamlit](https://streamlit.io/)
- [Pinecone](https://www.pinecone.io/)
