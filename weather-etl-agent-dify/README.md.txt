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

##Features
#Multi-Stage LLM Workflow
Uses multiple LLM nodes for:

--Parsing
--Analysis
--Quality review
--Final synthesis

#Real-Time Weather Intelligence

Fetches live weather data using the wttr.in API.

#Iterative ETL Processing

Processes multiple cities dynamically using Dify Iteration nodes.

#AI-Based Risk Assessment

Detects:

--High temperatures
--Low visibility
--Heavy rainfall
--High humidity
--Strong wind conditions

#Structured Error Handling

Gracefully handles:

--Invalid cities
--API failures
--Timeout scenarios

#Agentic Workflow Orchestration

Demonstrates modern AI workflow orchestration concepts using Dify.

#Technologies Used
Technology	Purpose
Dify	Workflow orchestration
Groq Llama 4	LLM inference
Python	Data transformation
wttr.in API	Weather data source
Langfuse	Tracing and observability
Agentic AI	Multi-stage AI orchestration

#Workflow Components
1. City Parser

Normalizes and validates city names.

2. JSON Parser

Converts LLM JSON string output into iterable arrays.

3. Iteration Node

Processes cities sequentially.

4. HTTP Request Node

Fetches weather data from wttr.in.

5. IF/ELSE Logic

Handles API success/failure conditions.

6. Weather Analyst

Analyzes:

Temperature rankings
Anomalies
Risk levels
Regional weather patterns
7. Quality Reviewer

Reviews and critiques the analyst findings.

8. Report Generator

Produces the final weather intelligence report.

#Sample Output
Weather Report Summary

Data Freshness: 2026-05-10 05:44 AM - 07:04 AM

Overview:
A generally warm and sunny weather pattern is observed across major Indian cities...

Risk Assessment:
🟢 NORMAL
🟡 WATCH
🔴 ALERT

#Repository Structure
weather-etl-agent-dify/
│
├── README.md
├── workflow.yml
├── sample-output.txt
├── screenshots/
│   ├── workflow.png
│   ├── test-run.png
│   └── final-report.png
│
└── docs/
    └── architecture.png

#How to Run
	Prerequisites
		Dify account
		Groq API key
		Langfuse account (optional)
	Setup
		Import the workflow.yml file into Dify
		Configure Groq model provider
		Add API credentials
		Run the workflow using sample city inputs

	Example input:
		
		Delhi, Mumbai, Kolkata, Chennai, Bangalore

#Observability

This project supports tracing and monitoring using Langfuse.

Tracked metrics include:

--Token usage
--LLM latency
--Node execution time
--Workflow traces
--Cost monitoring
--Branch execution paths

