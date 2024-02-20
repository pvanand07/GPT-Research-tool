# GPT-Research-tool
GPT Research tool for market research, competition analysis, etc. Built using Gemini API, Beautiful Soup and FastEmbed

## Steps Involved in Creating the Solution

### Install and Import Libraries: 
Installing necessary Python packages like `google-generativeai` for accessing Google's generative AI models and `qdrant-client` for leveraging Qdrant's capabilities for fast embeddings on CPU. Essential libraries like `nltk`, `requests`, `bs4` (BeautifulSoup), and others are imported for text processing and web scraping.

### Define Research Questions: 
The project aims to analyze Canoo EV's industry, competitors, market trends, and financial performance through a set of predefined research questions.

### Data Gathering:
- Utilizing Google's Custom Search API to gather data based on generated search queries relevant to the research questions.
- Scraping web content using BeautifulSoup for detailed analysis.

### Data Processing:
- Tokenizing and cleaning the scraped data using `nltk`.
- Organizing data into a structured format (dictionary) for analysis.

### Analysis and Report Generation:
- Employing generative AI (Gemini model from Google Generative AI) to interpret the gathered data and generate insights.
- Writing the insights into a markdown file as a comprehensive report.

## Techniques and Libraries Used

- **Natural Language Processing (NLP):** Used for generating multiple research queries for the user question, processing text data, and summarizing content. Libraries like `nltk` for tokenization and `google.generativeai` for generating content based on questions.
- **APIs for Data Gathering:** Google's Custom Search API for fetching relevant online links for research queries.
- **Web Scraping:** Utilizing `requests` and `BeautifulSoup` to extract information from web pages.
- **Concurrent Processing:** Using `ThreadPoolExecutor` for efficient data gathering and processing.
- **Qdrant Client:** For leveraging fast embeddings using quantization and semantic search.
- **sentence-transformers/all-MiniLM-L6-v2:** Maps sentences & paragraphs to a 384 dimensional dense vector space.

## Reference
[GPT Researcher by assafelovic](https://github.com/assafelovic/gpt-researcher)
