# End-to-End Medical Chatbot Using Llama2

This project implements a chatbot designed to provide accurate and contextual responses based on medical knowledge extracted from a comprehensive medical book describing diseases. By leveraging Retrieval-Augmented Generation (RAG), the chatbot combines pre-trained language models with document retrieval for precise and reliable answers.

## How to Run?

### Steps

1. **Clone the repository**
   ```bash
   Project repo: https://github.com/m-lafont/Medical_ChatBot_Using_LLaMa2.git
   ```

2. **Create a conda environment after opening the repository**
   ```bash
   conda create -n mchatbot python=3.8 -y
   conda activate mchatbot
   ```

3. **Install the requirements**
   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` file in the root directory and add your Pinecone credentials as follows:**
   ```ini
   PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
   ```

5. **Download the quantized model and place it in the `model` directory**
   - **Model Name**: `llama-2-7b-chat.ggmlv3.q4_0.bin`
   - **Download Link**: [Llama 2 Model on HuggingFace](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main)

6. **Store the index**
   ```bash
   python store_index.py
   ```

7. **Run the application**
   ```bash
   python app.py
   ```

8. **Access the chatbot**
   ```bash
   Open up localhost:
   ```

## Features

### 1. Medical Document Processing
- **PDF Extraction**: Uses `PyPDFLoader` to extract data from a medical book.
- **Directory Support**: Load and process multiple PDFs efficiently.

### 2. Embedding Models
- **HuggingFace Models**: Employs advanced embedding models from HuggingFace for accurate document representation.
- **CTransformers Integration**: Provides an alternative embedding approach using community-driven tools.

### 3. Vector Database Integration
- **Pinecone Vector Store**: Implements vector storage using Pinecone for fast and scalable retrieval of disease-related information.
- **LangChain Integration**: Chains prompts and retrieval workflows with `LangChain` to enable intelligent QA systems.

### 4. Environment Management
- **API Key Setup**: Handles Pinecone API key configuration through environment variables.
- **Modular Functions**: Structured functions for loading, embedding, and retrieving medical knowledge.

## Applications
- Medical question answering for healthcare professionals.
- Disease information retrieval for researchers.
- Educational tool for students studying medicine.

## Tech Stack Used

- Python
- LangChain
- Flask
- Meta Llama2
- Pinecone

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.



