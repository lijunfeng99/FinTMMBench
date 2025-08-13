# FinTiMMBench: Temporal-Aware Multi-Modal Retrieval Augmented Generation Benchmark in Finance

## Overview

FinTiMMBench is the first comprehensive benchmark designed to evaluate temporal-aware multi-modal Retrieval-Augmented Generation (RAG) systems in the financial domain. It comprises 5,676 high-quality QA pairs built from heterogeneous data of NASDAQ-100 companies, including financial tables, news articles, daily stock prices, and visual technical charts. Each question requires retrieving and interpreting data over specific time periods, addressing 10 diverse financial analysis tasks.

## Dataset Features

- **Multi-Modal Corpus**:  
  - 1,500 financial tables  
  - 3,133 news articles  
  - 25,200 daily stock price records  
  - 6,267 visual technical charts  

- **Temporal-Aware Questions**:  
  Questions are designed to require information retrieval and reasoning over specific time periods (daily, weekly, monthly, quarterly, or annual).  

- **Diverse Financial Tasks**:  
  Covers 10 tasks: Information Extraction, Arithmetic Calculation, Trend Analysis, Logical Reasoning, Sentiment Classification, Event Detection, Counterfactual Reasoning, Comparison, Sorting, and Counting.  

## Dataset Statistics

| Statistic                     | Number       |
|-------------------------------|-------------|
| Total Number of Companies     | 100         |
| Total Number of Raw Data      | 36,100      |
| Total Number of Questions     | 5,676       |
| Avg. Words per Question       | 18.88       |
| Avg. Words per Answer         | 6.87        |

## File Structure

The repository is organized as follows:
```
FinTiMMBench/
├── QA.json # All question-answer pairs with reasoning chains
├── data/
│ ├── FinancialTable.json # Raw financial table data
│ ├── News.json # Financial news articles
│ ├── StockPrice.json # Daily stock price records
│ ├── Chart/ # Directory containing visual technical charts
│ ├── schema.xlsx # Templates used for question generation
│ └── Prompt/ # Prompt templates for generating questions
├── LICENSE
└── README.md
```


- **QA.json**: Contains all 5,676 question-answer pairs with Chain-of-Thought reasoning and references to raw data
- **FinancialTable.json**: Structured financial data for NASDAQ-100 companies
- **News.json**: Filtered Reuters financial news articles with metadata
- **StockPrice.json**: Daily stock records (open, close, high, low, volume)
- **Chart/**: Weekly and monthly candlestick charts in PNG format
- **schema.xlsx**: Excel templates defining question patterns and constraints
- **Prompt/**: Contains the prompt templates used with GPT-4o-mini for QA generation