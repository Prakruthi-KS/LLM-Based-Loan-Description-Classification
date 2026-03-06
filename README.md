# LLM Based Loan Description Classification

## Project Overview

Financial datasets often contain large amounts of unstructured text, such as loan descriptions, that can provide valuable signals about borrower intent and risk. Traditional structured fields may not capture the full context of these descriptions.

This project uses Generative AI and prompt engineering techniques to automatically classify loan descriptions and evaluate the reliability of LLM-generated labels.

The workflow includes:

* Pre-testing an LLM prompt on a sample datase
* Comparing LLM-generated labels against manually labeled data
* Evaluating model accuracy
* Testing different temperature parameters
* Estimating the cost and runtime required for large-scale deployment

## Business Understanding

Lending platforms rely heavily on accurate risk assessment when evaluating loans. While structured variables such as credit scores and income ratios are useful, borrowers often provide additional context through text descriptions of loan purposes.

Analyzing these descriptions can help investors:

* Identify higher-risk loan categories
* Improve investment decision-making
* Detect patterns not captured in structured data
* Enhance loan classification accuracy
* LLMs offer a scalable solution for converting unstructured text into structured insights.

## Key Research Questions

This project focuses on answering the following questions:

* Can LLMs accurately classify loan purposes from text descriptions?
* How does temperature influence model consistency and labeling accuracy?
* How reliable are LLM outputs compared to human-labeled data?
* What are the cost and time implications of scaling LLM-based analysis to large datasets?

## Methodology

### 1. Data Sampling
A random sample of 100 loan descriptions labeled as major_purchase was extracted from the dataset to test the prompt design and classification approach.

### 2. Prompt Engineering
An iterative prompt design process was used to instruct the Gemini LLM to classify loan descriptions into three categories:
* Business loan
* Home improvement loan
* Other loan purposes

### 3. Model Validation
The LLM-generated labels were compared with manually labeled descriptions to measure classification accuracy and identify discrepancies.

### 4. Parameter Experimentation
Different temperature values (0, 1, and 2) were tested to analyze their effect on output consistency and model behavior.

### 5. Cost & Runtime Estimation
The project estimated the API cost and runtime required to classify all 126,053 loan descriptions using the Gemini API.

## Key Insights

Key findings from the analysis include:

* LLMs can effectively extract structured insights from unstructured financial text data.
* Lower temperature values produce more consistent and deterministic outputs, which is preferable for classification tasks.
* Human validation is essential to ensure the reliability of LLM-generated labels.
* Scaling LLM-based analyses requires careful planning due to API rate limits, processing time, and token-based costs.
