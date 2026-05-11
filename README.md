# Agentic Weather ETL Pipeline using Dify and Groq Llama 4

An AI-powered multi-stage Weather ETL workflow built using Dify, Groq Llama 4, iterative orchestration, and real-time weather APIs.  
This project demonstrates how Agentic AI workflows can be applied to modern data engineering pipelines for intelligent data collection, analysis, validation, and report generation.

---

# Project Overview

This workflow fetches live weather data for multiple Indian cities, processes the data through a structured ETL pipeline, and uses multiple LLM stages to generate a polished weather intelligence report.

The system includes:

- City name parsing and normalization
- Real-time weather data ingestion
- Iterative ETL orchestration
- Multi-LLM analysis pipeline
- AI-based quality review
- Final intelligence report generation
- Error handling and fallback mechanisms

---

# Architecture

```text
User Input
   ↓
City Parser (LLM)
   ↓
JSON Parser (Code Node)
   ↓
Iteration Loop
   ├── HTTP Request (wttr.in API)
   ├── IF/ELSE Validation
   ├── Weather Extraction
   └── Error Fallback
   ↓
Weather Analyst (LLM)
   ↓
Quality Reviewer (LLM)
   ↓
Report Generator (LLM)
   ↓
Final Output
