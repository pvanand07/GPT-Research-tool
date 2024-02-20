# GPT-Research-tool
GPT Research tool for market research, competition analysis, etc. Built using Gemini API, Beautiful Soup and FastEmbed

Author: [Anand Siva](https://github.com/pvanand07)
# Summary
The solution involves creating research questions from user query, gathering website data through Google Custom Search API and web scraping, processing data using NLP, using vector embeddings and semantic search to obtain relevant information and generating insights with generative AI.

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

## Current Bottlenecks/Suggestions to improve
- The time to create a vector embedding is 2min 46s for 29 websites by using Qdrant client and the model sentence-transformers/all-MiniLM-L6-v2 (83.2MB), which can be improved by utilizing a gpu or using other high performant vector embeddings.
- Perform text cleaning to eliminate website headers and other commonly occuring elements during NLP
- Summarization quality can be improved by using an openai model instead of gemini
- using selenium instead of requests can capture websites utilizing dynamic content loading.
- Provide reference links along with scraped context and improve the prompt for report generation to include citations

## Challenges Faced
- Most financial data is not readily available using a google search, using financial Api's such as yahoo finance might help to obtain fundamental stock details, this can be achieved using OpenAI function calling, but not implementing due to cost and limited time
- Sharing Api keys is not possible at the moment using colab, alternative would be to host the code in a platform such as Hugging Face spaces which can handle secrets. Not implementing due to limited time.

## Reference
[GPT Researcher by assafelovic](https://github.com/assafelovic/gpt-researcher)
