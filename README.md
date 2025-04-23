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

## **Required API Keys**  
Before running the project, ensure you have the following API keys set up in your environment variables:  

```bash
export TAVILY_API_KEY="your_tavily_api_key"
export AWS_ACCESS_KEY_ID="your_aws_access_key"
export AWS_SECRET_ACCESS_KEY="your_aws_secret_access_key"
export AWS_DEFAULT_REGION="your_aws_region"
# Required API Keys
SERPER_API_KEY=your_serper_api_key
REDDIT_CLIENT_ID=your_reddit_client_id
REDDIT_CLIENT_SECRET=your_reddit_client_secret
REDDIT_USER_AGENT=your_reddit_user_agent
GEMINI_API_KEY=your_gemini_api_key
ALPHA_VANTAGE_API_KEY=your_alpha_vantage_api_key

# Optional - Multiple Groq accounts for advanced parallelization
GROQ_API_KEY=your_groq_api_key
GROQ_API_KEY_1=your_first_groq_key
GROQ_API_KEY_2=your_second_groq_key

# Configuration Options
USE_PARALLEL_EXECUTION=true
SAVE_INTERIM_RESULTS=true
DEBUG_MODE=false
```

## Setting Up Your Development Environment
For an efficient development experience, please follow these two essential steps:
### 1. Install the Virtual Environment
First, create an isolated environment to house your project dependencies. Execute the following commands:

```bash
# For Windows
python -m venv venv
# For macOS and Linux
python3 -m venv venv
```

### 2. Install All Required Libraries
Next, activate your virtual environment and install the necessary libraries in one swift command:

```bash
# For Windows
.\venv\Scripts\activate
# For macOS and Linux
source venv/bin/activate
# Install all dependencies
pip install -r requirements.txt
```


