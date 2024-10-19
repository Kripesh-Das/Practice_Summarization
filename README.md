# Text Summarization Project

This project demonstrates various text summarization techniques using the LangChain library. The techniques include Stuff Document Chain, MapReduce Summarization, and Refine Chain Summarization.

## Project Structure

- **`.env`**: Contains environment variables for API keys.
- **`requirements.txt`**: Lists the dependencies required for the project.
- **`text_summarization.ipynb`**: Jupyter notebook demonstrating the text summarization techniques.

## Setup
1. **Install dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

2. **Set up environment variables**:
    - Create a `.env` file in the root directory.
    - Add the following environment variables:
      ```env
      LANGCHAIN_API_KEY = "your_langchain_api_key"
      LANGCHAIN_PROJECT = "Text_Summarization"
      HF_TOKEN = "your_hf_token"
      GROQ_API_KEY = "your_groq_api_key"
      ```
## Techniques Demonstrated

### 1. Stuff Document Chain Summarization

Combines the entire document content and sends it as a single prompt to the LLM model. Best for smaller documents that fit within the LLM's context window.

### 2. MapReduce Summarization Technique

Breaks the document into smaller chunks, summarizes each chunk, and then combines the summaries into a final output. Ideal for larger documents or files that exceed the LLM's context size.

### 3. Refine Chain Summarization

Sequentially processes document chunks, updating a rolling summary. Different from "stuff document chain" and "map reduce chain."

## Dependencies

- `python-dotenv`
- `langchain_groq`
- `langchain_community`
- `langchain`
