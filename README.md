# Medical Chatbot

This project is an AI-powered medical chatbot designed to answer health-related questions accurately and concisely. Built using **LangChain**, **FAISS**, and **Hugging Face embeddings**, the chatbot retrieves relevant information from a curated database of trusted medical documents and delivers responses in real-time. It’s optimized for CPU usage, making it deployable on local machines and adaptable to various environments.

## Table of Contents

1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Project Structure](#project-structure)
6. [Configuration](#configuration)
7. [License](#license)

---

## Features

- **Accurate Health Information**: Provides concise, reliable answers to health-related questions based on curated sources.
- **Customizable Prompt Template**: Configured to deliver fact-based responses and avoid speculation.
- **Efficient Retrieval**: Uses FAISS for fast search capabilities across large medical document datasets.
- **User-Friendly Deployment**: Runs on VS Code and compatible with CPU, making it accessible for various devices.

## Tech Stack

- **Python**: Core language for development.
- **LangChain**: Framework to build custom question-answering (QA) models.
- **FAISS**: Efficient similarity search and clustering for vectorized document storage.
- **Hugging Face**: Embeddings for effective query interpretation and response generation.
- **Chainlit**: Framework for conversational AI applications.
- **Transformers**: Tokenizer to optimize language model usage.

## Installation

### Prerequisites
- Python 3.8 or higher
- Pip (Python package installer)

### Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/medical-chatbot.git
   cd medical-chatbot
   ```

2. **Set up a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download the medical data files** and save them in the `/data` folder.

## Usage

1. **Ingest Medical Documents:**
   Run `ingest.py` to preprocess and vectorize your medical documents into a FAISS database:
   ```bash
   python ingest.py
   ```

2. **Start the Chatbot:**
   Run `app.py` to launch the chatbot:
   ```bash
   python app.py
   ```

3. **Interact with the Chatbot:**
   Open the Chainlit interface as instructed in the console, then enter health-related queries to receive concise responses.

## Project Structure

```plaintext
├── app.py                 # Main chatbot script
├── ingest.py              # Script to preprocess and vectorize medical documents
├── data/                  # Directory for storing source medical documents
├── faiss_db/              # Directory for storing the FAISS database
├── requirements.txt       # List of required Python packages
└── README.md              # Project documentation
```

## Configuration

- **Data Path**: Specify the path to your data in the `DATA_PATH` variable in both `app.py` and `ingest.py`.
- **FAISS Database Path**: Specify the path for your FAISS database in the `DB_FAISS_PATH` variable in both `app.py` and `ingest.py`.
- **Prompt Template**: Customize the prompt in `app.py` under `custom_prompt_template` to tailor response behavior.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
