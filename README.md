# LLM-Powered Chatbot and Web Scraper with LangChain

This project demonstrates a LangChain-powered application that uses the Llama2 LLM model for generating responses to user queries. The application is implemented in two parts:

- **Chatbot**: An interactive chatbot for general-purpose Q&A.
- **Web Scraper**: A tool to scrape and retrieve relevant content from web sources, then answer questions based on that content.

## Features

- **LLM-Powered Chatbot**: Uses the Llama2 language model to generate responses for user queries.
- **Web Scraping with LangChain**: Scrapes content from a specified URL, processes it, and enables question-answering based on the scraped content.
- **Streamlit Interface**: Simple, user-friendly interface built with Streamlit for easy interaction with the chatbot.

## Project Structure

- **chatbot.py**: A simple chatbot interface using Llama2 to answer user queries.
- **webScrapper.py**: Scrapes a webpage, splits the content for embedding, and retrieves relevant information based on user queries.
- **requirements.txt**: List of all required packages and dependencies.

## Setup and Installation

### Prerequisites

- Python 3.10
- Conda (optional but recommended for environment management)
- Ollama for running the Llama2 model locally (currently macOS only)

### Installation Steps

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/yourusername/yourprojectname.git
    cd yourprojectname
    ```

2. **Install and Set Up Ollama**:

    - Download and install Ollama from [https://ollama.com/](https://ollama.com/).
    - Open a command prompt or terminal and run:

    ```bash
    ollama run llama2
    ```

3. **Create and Activate the Virtual Environment**:

    ```bash
    conda create -p venv python==3.10 -y
    conda activate ./venv  # Adjust the path as needed
    ```

4. **Install Dependencies**:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

### Running the Chatbot

To start the chatbot with Streamlit:

```bash
streamlit run chatbot.py
```
# Running the Web Scraper

To run the web scraper and get information from the specified URL:

```bash
python webScrapper.py
# Web Scraper and Chatbot Setup
```
This will scrape content from the URL provided in `webScrapper.py`, split the text for embedding, and return answers to questions based on the scraped content.

## Files Explained

### `chatbot.py`
Uses a `ChatPromptTemplate` and the Llama2 model to answer user questions. It runs a Streamlit-based interface.

### `webScrapper.py`
Uses `WebBaseLoader` to scrape content from a specified URL, then splits the content into chunks and embeds it using `HuggingFaceEmbeddings`. It retrieves relevant content to answer questions about the topic.

### `requirements.txt`
Specifies dependencies such as LangChain, OpenAI, and Streamlit for running the chatbot and web scraper.

## Additional Notes

- Ensure that the virtual environment (venv) path is correct when activating the virtual environment.
- Modify the URL in `webScrapper.py` to scrape different web pages if desired.
- Ollama is required to run the Llama2 model and must be running in the background (`ollama run llama2`) for the chatbot to function.

## License

This project is licensed under the MIT License.
=======

