# RAG_CHATBOT
📚 RAG Chatbot using LangChain, FAISS, Gradio & OpenRouter

This project builds a Retrieval-Augmented Generation (RAG) chatbot that answers user queries using data scraped from a website and a local text file. It uses LangChain, FAISS vector database, and LLMs via OpenRouter & Google Gemini, with a simple Gradio UI.

🚀 Features
🔍 Web scraping using BeautifulSoup
📄 Custom document ingestion (TXT file)
✂️ Smart text chunking using LangChain
🧠 Embeddings with OpenAI / HuggingFace
📦 Vector storage using FAISS
🤖 LLM support via OpenRouter & Gemini
💬 Question answering using RetrievalQA
🌐 Interactive UI using Gradio
🛠️ Tech Stack
Python
LangChain
FAISS
OpenRouter API
Google Generative AI (Gemini)
Gradio
BeautifulSoup
Pandas
📂 Project Structure
├── RAG_Chatbot_Project.ipynb
├── course.txt
├── README.md
⚙️ Installation

Install all required dependencies:

pip install langchain-openai
pip install langchain faiss-cpu pandas requests beautifulsoup4 openai gradio tiktoken
pip install langchain-text-splitters
pip install langchain-google-genai
pip install langchain-community langchain-huggingface
pip install langchain-classic
🔑 API Keys Setup

Set your API keys:

OPENROUTER_API_KEY = "your_openrouter_api_key"
os.environ["OPENAI_API_KEY"] = OPENROUTER_API_KEY
os.environ["OPENAI_API_BASE"] = "https://openrouter.ai/api/v1"

For Gemini:

google_api_key = "your_google_api_key"

⚠️ Important: Never expose your API keys publicly. Use environment variables or .env files.

📥 Data Sources
🌐 Website: https://fullstackacademy.in/
📄 Local file: course.txt

The project combines both sources into a unified knowledge base.

🧠 How It Works
Scrapes website content using BeautifulSoup
Loads local text data
Combines both into one dataset
Splits text into chunks
Converts chunks into embeddings
Stores embeddings in FAISS vector database
Retrieves relevant chunks based on query
Sends context + query to LLM
Returns generated answer
💡 Example Queries
"Who is the trainer for data science?"
"What courses are offered?"
"What is this document about?"
🧪 Running the Project

Run the notebook step by step:

jupyter notebook RAG_Chatbot_Project.ipynb

Or open in Google Colab and execute all cells.

💬 Gradio Interface (Optional)

You can extend this project with a simple Gradio UI:

import gradio as gr

def chat(query):
    response = qa_chain.invoke({"query": query})
    return response['result']

gr.Interface(fn=chat, inputs="text", outputs="text").launch()
📌 Future Improvements
Add chat history (memory)
Improve UI with chat-style interface
Use streaming responses
Add multiple document sources (PDF, CSV, etc.)
Deploy using Hugging Face Spaces or Streamlit Cloud
⚠️ Limitations
Depends on quality of scraped data
No long-term memory
API cost may apply for LLM usage
🤝 Contributing

Feel free to fork this repository and improve it. Contributions are welcome!

📜 License

This project is open-source and available under the MIT License.
