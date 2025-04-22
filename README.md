# StockLensAI
A wise, finance-savvy chatbot for Stock &amp; Finance Q&amp;A with Price Trend Prediction

## **Overview**  
StockSenseAI is a two-part AI-driven project that combines a **RAG-based LLM chatbot** for stock market and finance Q&A with a **time series stock trend prediction model**. This system enables users to retrieve financial insights from multiple sources and predict stock price movement, backed by a fully automated MLOps pipeline.  

---

## **Project Components**  

### **1. RAG-Based LLM Chatbot for Stock & Finance Q&A**  
The chatbot answers finance-related questions using a **Retrieval-Augmented Generation (RAG)** approach, retrieving data from two sources:  
1. **Internet Search Results** – The top search engine results for real-time market trends and news.  
2. **SEC Filings Stored in ChromaDB** – Latest company filings retrieved from the **SEC API** and stored in **ChromaDB** for fast and efficient retrieval.  

💡 *This ensures users receive accurate, up-to-date information from reliable sources.*  

#### **Workflow**  
- User submits a stock/finance-related question.  
- The system retrieves answers from:  
  - **Internet Search**: Fetches the latest top results.  
  - **ChromaDB**: Retrieves the latest SEC filings for the queried company.  
- The LLM processes and synthesizes the retrieved data to generate a response.  

---

### **2. Stock Price Trend Prediction Model**  
This module predicts the **direction** of a stock (up or down) over a user-selected timeframe. The system is trained on **S&P 500** stocks and uses a **time series forecasting model**.  

#### **Key Features**  
✅ **Predict stock direction** for different timeframes (e.g., daily, weekly, monthly).  
✅ **Automated MLOps Pipeline** for periodic retraining and deployment.  
✅ **Scalable and flexible** to expand to more stocks or improve model performance over time.  

#### **MLOps Pipeline**  
The entire stock prediction workflow is automated using an **MLOps pipeline**, which:  
1. **Retrieves the latest stock market data** at fixed intervals.  
2. **Retrains the model** periodically to ensure updated predictions.  
3. **Deploys the trained model** to provide real-time predictions based on user-selected timeframes.  

---

## Project Directory Overview

There are four major directories in this project that you should explore to better understand and run the code:

1. **Chatbot**  
   Contains the final chatbot architecture along with detailed explanations of its components.

2. **Data Preparation**  
   Includes the datasets and preprocessing steps used throughout the project.

3. **LLM_Dashboard**  
   Demonstrates the use of predictive models for stock price prediction, integrated into a dashboard format.

4. **Stock EDA and Trend Prediction**  
   Provides exploratory data analysis (EDA) of stock data and illustrates trend prediction methods.

---
