# Document Intelligence - RAG Pipeline

An AI-powered document analysis tool that simulates a Retrieval-Augmented Generation (RAG) workflow on legal documents. 

Built using Google Gemini and Python.


## What it does:

- Loads and extracts text from a PDF document with page-level tracking

- Retrieves the most relevant pages for any given query

- Returns AI-generated answers with exact page number citations

- Automatically extracts Risks, Dates, and Stakeholders into a Summary Dashboard



## Tools \& Technologies:

Python, Jupyter Notebook, Google Gemini API ('google.genai'), pypdf, python-dotenv



## Document Used

Google Terms of Service - May 2024 (20 pages)



## Setup

Create a '.env' file with your Google Gemini API key: **GOOGLE\_API\_KEY=** *your\_key\_here*

Then install dependencies and run the notebook.

