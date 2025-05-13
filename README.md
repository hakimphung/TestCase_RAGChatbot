# Manual Testing – RAG Chatbot

## Introduction

This project focuses on the manual testing of a RAG (Retrieval-Augmented Generation) Chatbot. The chatbot features dual modes: RAG from documents/URLs and Web Search via Tavily. These test cases and documentation cover UI interactions, query handling in both modes, response quality, and basic setup verification. The goal is to ensure the chatbot functions as expected and meets the specified requirements.

**Application Under Test (AUT):** RAG Chatbot (built on LangGraph, Pinecone, Tavily, OpenAI, Streamlit). This application is run locally.

**Project Sections:** This project focuses on the Testing section.

**Tools Used (assumed):**
* Test Case Management: Excel/Google Sheets
* UI and Functional Testing: Web browser
* Application Runtime Environment: Python, Streamlit, relevant libraries.

## Functional Specifications

The functionality of the RAG Chatbot is described as follows (similar to a User Story in JIRA):

*As a user, I want to use a chatbot capable of answering questions based on documents I provide (PDFs, web URLs) or based on real-time web search information, so I can quickly find the information I need.*

**Key Features:**
* **Dual Operating Modes:**
    * **RAG (Retrieval-Augmented Generation):** Answers questions based on information from user-provided documents/URLs.
    * **Web Search:** Answers questions based on real-time web search information (using Tavily).
* **RAG Data Sources:**
    * Upload PDF files.
    * Input web URLs (HTML).
* **LangGraph Orchestration:** Manages conversation flow and processing logic.
* **Vector Store Integration (Pinecone):** Stores and queries document embeddings.
* *(Other features like Streaming Responses, User-Friendly Interface would be listed here based on the full document)*

## Testing Section

### Risks Detected

* **Project Risks:**
    * Unstable or difficult-to-set-up local testing environment.
    * Lack of diversity in test data (PDFs, URLs) leading to missed defects.
    * Time constraints for project execution.
* **Product Risks:**
    * Slow response times when processing complex queries or large documents.
    * Incorrect handling of diverse PDF formats or complex web page structures.
    * *(Other product risks like inaccurate information retrieval, irrelevant search results, UI/UX issues would be listed here based on the full document)*

### Test Analysis

The testing process will be executed based on the stated requirements for the RAG Chatbot. The main test conditions identified include:
* Verify RAG data source processing (PDF upload, URL input, including supported URL types like HTML, direct PDF, arXiv).
* Verify the ability to ask questions and receive accurate answers in RAG mode based on processed sources.
* Verify the ability to ask questions and receive appropriate answers in Web Search mode.
* Verify smooth switching between operating modes.
* Verify all user interface elements (input fields, buttons, response display, detailed processing steps area) function correctly.
* Verify error handling for invalid inputs (e.g., malformed URLs, no RAG file uploaded) or (simulated) API connection issues.
* Verify responses are displayed via streaming.
* Verify configuration settings (e.g., `CHUNK_SIZE`, `TOP_K`) affect results as expected (exploratory testing).

### Test Summary Report

* **Total test cases planned:** 16
* **Total test cases executed:** 16 (100%)
* **Test cases passed:** 14
* **Test cases failed:** 2
* **Total defects found:** 2
    * **High Priority:** 2
