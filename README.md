# Smart Article Summarizer

A web application that summarizes news articles, extracts key points, and performs sentiment analysis using Natural Language Processing (NLP).

## Features
- **Article Summarization**: Get concise summaries of any news article.
- **Key Points Extraction**: Automatically identify and highlight important points.
- **Sentiment Analysis**: Determine if the article has a positive, negative, or neutral tone.
- **User-Friendly Interface**: Simple and intuitive design.
- **Paywall Handling**: Fallback mechanisms to handle articles behind paywalls.

## Technologies Used
- **Flask**: A lightweight web framework for building the application.
- **NLTK**: A powerful library for natural language processing.
- **BeautifulSoup4**: For web scraping and parsing HTML content.
- **Requests**: For making HTTP requests to fetch article content.
- **Transformers (Hugging Face)**: For advanced AI-based summarization (optional).
- **PyTorch**: A framework for deep learning, used if you want to run AI-based summarization (optional).

## Requirements
- Python 3.7+
- Basic dependencies:
  - Flask
  - NLTK
  - BeautifulSoup4
  - Requests
- Advanced features (optional):
  - Transformers (Hugging Face)
  - PyTorch

## Installation

### 1. Clone the repository:
```bash
git clone <repository-url>
cd News_Article_Summarizer
````

### 2. Install dependencies:

Run the `run.py` script, which will guide you through dependency installation.

```bash
python run.py
```

If you're missing basic dependencies, the script will prompt you to install them.

### 3. Alternative Installation (if you face issues with dependencies):

You can manually install the required dependencies:

```bash
pip install Flask==1.1.2
pip install NLTK
pip install BeautifulSoup4
pip install Requests
```

To install optional advanced features:

```bash
pip install transformers
pip install torch
```

## Usage

You have multiple ways to run the application based on your system configuration:

### 1. Full Version (with AI summarization):

If your system supports PyTorch and Transformers, this will use the Hugging Face pipeline for advanced summarization:

```bash
python run.py
```

### 2. Basic Version (without AI summarization):

If you face issues installing PyTorch or Transformers, you can run the app with basic extractive summarization:

```bash
python fallback.py
```

### 3. Interactive Setup:

The `run.py` script will automatically detect available dependencies and offer you the appropriate options based on your system's capabilities:

```bash
python run.py
```

## How It Works

1. **Web Scraping**: The app fetches the article's content from a URL provided by the user.
2. **Text Extraction**: The main text of the article is extracted from the HTML using BeautifulSoup.
3. **Summarization**:

   * **Full version**: Uses the Hugging Face Transformers for AI-based **abstractive summarization**.
   * **Basic version**: Uses simple **extractive summarization** by picking the first few sentences and key points.
4. **Key Points Extraction**: Important sentences are identified based on key indicators and relevance.
5. **Sentiment Analysis**: NLTK’s Sentiment Intensity Analyzer determines the overall sentiment of the article.

## Troubleshooting

If you encounter issues during installation or while running the application:

* Ensure that you have the correct versions of dependencies.
* If you face issues with PyTorch installation, use the basic version:

  ```bash
  python fallback.py
  ```
* Try upgrading pip and setuptools:

  ```bash
  pip install --upgrade pip setuptools wheel
  ```

## Limitations

* The app works best with standard news article formats.
* Very long articles may be truncated for processing.
* The quality of the summary depends on the article’s structure and content.
* Some websites may block web scraping.
* The basic version provides simpler summaries without AI modeling.

## Future Improvements

* Add support for summarizing PDF articles.
* Implement more advanced key points extraction algorithms.
* Add multilingual support for article summarization.
* Include topic classification for articles.
* Enable saving and comparing multiple article summaries.

---

Feel free to ask any questions or submit issues via the GitHub Issues tab. Happy coding! 🚀
