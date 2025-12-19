# 🏎️ AutoSpec Pro: AI-Powered Automobile Assistant

**AutoSpec Pro** is a specialized Retrieval-Augmented Generation (RAG) assistant designed for the automotive domain. It allows users to upload multiple vehicle owner manuals and Diagnostic Trouble Code (DTC) references to extract detailed technical specifications and troubleshooting steps using AI.

### 🌐 Live Demo

**[Click here to access the live app](https://rag-powered-assistant.streamlit.app/)** *(Note: Please ensure you have your API keys ready to use the assistant if prompted.)*

## 🌟 Key Features

* **Multi-PDF Support:** Upload and index multiple service manuals simultaneously.
* **Detailed Technical Answers:** Custom-tuned prompts ensure the AI provides step-by-step instructions and specific torque/fluid values.
* **Conversational Memory:** Remembers the context of your previous questions for a natural troubleshooting flow.
* **Source Citation:** Highlights exactly which page and manual were used to generate the answer.
* **Workshop-Themed UI:** A high-contrast, professional interface built for workshop environments.

## 🛠️ Tech Stack

* **Frontend:** [Streamlit](https://streamlit.io/)
* **LLM:** [Google Gemini 2.5 Flash](https://aistudio.google.com/)
* **Embeddings:** [Hugging Face Sentence Transformers](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)
* **Vector Database:** [FAISS (Facebook AI Similarity Search)](https://github.com/facebookresearch/faiss)
* **Framework:** [LangChain](https://www.langchain.com/)

## 🚀 Deployment Instructions (Streamlit Cloud)

### 1. Prepare Your Repository

Ensure your GitHub repository has the following structure:

```text
├── app.py               # Main Streamlit frontend
├── backend.py           # RAG logic and processing
├── requirements.txt     # Python dependencies
└── README.md

```

### 2. Set Up Environment Variables

Since you are deploying to **Streamlit Community Cloud**, do not include your `.env` file. Instead:

1. Go to your app's **Settings** on the Streamlit Cloud Dashboard.
2. Navigate to **Secrets**.
3. Add the following:
```toml
GOOGLE_API_KEY = "your_gemini_api_key"
HUGGINGFACEHUB_API_TOKEN = "your_huggingface_token"

```



### 3. Local Installation

To run this project locally, follow these steps:

```bash
# Clone the repository
git clone https://github.com/yourusername/autospec-pro.git
cd autospec-pro

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py

```

## 📋 Example Queries

* "What is the engine oil capacity and grade for a 2014 F-150?"
* "Describe the step-by-step procedure for replacing front brake pads."
* "What does DTC P0300 mean and what are the possible causes?"
* "Give me the torque specifications for the cylinder head bolts."

##  Chalanges Faced 
* Cloud platform and payments constraints(Azure OpenAI)
  Used streamlit for UI instead of Azure.
* Large Pdf
  Churn chunking strategy.

## ⚖️ License

Distributed under the MIT License.

---
