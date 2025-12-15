# ML Workflow — PYQ Revision Model

## 1. Data Ingestion
- Load complete past question papers in structured format (JSON/CSV).  
- Extract per-question details: marks, question type, OR/choice constraints, and year metadata.  
- Validate papers for completeness and version the dataset for reproducibility.

## 2. Data Cleaning & Structuring
- Normalize question text and standardize notation.  
- Tag question types, OR pairs, and “answer k of n” groups.  
- Ensure metadata consistency (marks, IDs, year, constraints).  
- Output a structured question-level dataset ready for NLP classification.

## 3. Exploratory Analysis
- Understand exam structure and patterns rather than numeric distributions.  
- Analyze:
  - Question-type distributions  
  - Topic coverage per paper  
  - OR/choice patterns  
  - Temporal trends (topic stability vs newly introduced topics)  
- Produce summary tables and sanity checks to guide modeling.

## 4. Modeling

### 4.1 Question → Topic Classification
- Assign each question to a fine-grained syllabus topic (multi-class text classification).  
- Baseline: TF-IDF + Logistic Regression  
- Improved: Linear SVM  
- Optional stretch goal: Fine-tuned transformer

### 4.2 Topic Normalization & Semantic Compression
- Merge semantically similar topics and build a syllabus-aligned hierarchy.  
- Consolidate frequency-weighted topics to produce human-readable, condensed topic labels.

### 4.3 Coverage-Aware Optimization
- Select the minimal set of topics such that ≥55% of marks are achievable per paper.  
- Respect OR/choice constraints and process papers from most recent to oldest.  
- Incrementally expand topics only when needed.

## 5. Evaluation
- Assess topic classification with accuracy and F1-score on labeled questions.  
- Evaluate coverage:
  - % marks achievable per paper  
  - Topic stability  
  - Minimality of the final topic set  
- Summarize results in structured reports.

## 6. Deployment / Demo
- Minimal Streamlit app to upload past papers and visualize:
  - Extracted topics  
  - Coverage per paper  
  - Final recommended revision list  
- Include concise documentation:
  - Problem motivation  
  - Pipeline diagram (Layers 1–4)  
  - Example dataset and demo screenshots / short video
