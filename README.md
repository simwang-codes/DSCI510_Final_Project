> Note: This is not the final version of the README. More updates, code explanations, and visuals will be added soon.

# Video Game Insight System (RAG-Powered)

This project explores the intersection of data scraping, text processing, and AI-powered question answering through a Retrieval-Augmented Generation (RAG) chatbot. The system helps users (e.g., video game marketing professionals) interact with curated insights about some of the most acclaimed video games in history.

## Project Overview

- Extracted data from the "Best Video Games in Human History" HTML table and Steam Database (live player stats).
- Used additional scrapers to gather video game companies' headquarters and website information.
- Scraped full Wikipedia introduction pages for each game and cleaned the text for use in a RAG system.
- Built a custom AI chatbot with LangChain, OpenAI API, and FAISS to perform similarity-based Q&A.
- Integrated Streamlit UI to allow end-users to interact with the chatbot and understand analysis results.

## Workflow

1. **Web Scraping**  
   Collected structured game and company data from HTML tables, SteamDB, and Google Search via SerpApi. Retrieved and cleaned game descriptions from individual Wikipedia pages.

2. **Text Processing**  
   Split cleaned text into manageable chunks. Extracted keywords from each chunk using KeyBERT and stored the data in a local SQLite database.

3. **Embedding and Indexing**  
   Transformed text chunks into vector embeddings using OpenAI’s API via LangChain. Indexed the results using FAISS for similarity search.

4. **Q&A Interface**  
   User questions trigger similarity-based retrieval of relevant chunks. These are passed with the user’s query to GPT-4 for generating a coherent response. A custom Streamlit interface enables user interaction.

5. **Optional Enhancements**  
   Enhanced company data via SerpApi (headquarters and URLs). Planned deliverables include visualizations (e.g., heatmaps by region) and sentiment analysis.

## Libraries Used

- Python, pandas, BeautifulSoup
- LangChain, OpenAI API, FAISS
- KeyBERT, Streamlit, sqlite3
- SerpApi

## Current Features

- RAG chatbot trained on full-text data from 300+ Wikipedia game pages.
- Answers targeted questions about games using AI-driven search and summarization.
- Custom-built Streamlit UI for real-time interaction.
- Ongoing work to speed up keyword extraction, the most time-intensive step.

## Next Steps

- Optimize keyword extraction process.
- Add Jupyter-compatible input fallback in case UI issues arise.
- Finalize structured dataset and develop analysis notebook with visualizations and sentiment insights.

---

Hi Professor, thank you very much for reviewing this README. Please feel free to reach out with any feedback or questions about the RAG system or overall project design.

Best,  
Sim Wang – DSCI 510