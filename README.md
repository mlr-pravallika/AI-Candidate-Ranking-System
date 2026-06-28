# AI-Powered Candidate Ranking System

## Overview

Recruiters often review thousands of candidate profiles for a single job opening. Traditional Applicant Tracking Systems (ATS) rely heavily on keyword matching, which can overlook highly qualified candidates whose profiles do not exactly match the job description.

This project presents an AI-powered candidate ranking system that analyzes candidate profiles, extracts meaningful recruitment signals, and generates a ranked shortlist of candidates based on their suitability for a given role.

The system combines recruiter-inspired scoring, semantic understanding, and a hybrid ranking framework to identify candidates who best match the requirements of a job description.

---

# Problem Statement

Build an intelligent ranking engine that:

* Understands job requirements
* Evaluates candidate profiles holistically
* Goes beyond simple keyword matching
* Produces a ranked list of recommended candidates

The objective is to simulate how an experienced recruiter evaluates candidate suitability while maintaining scalability across large candidate datasets.

---

# Key Features

## Candidate Profile Analysis

* Parses and processes candidate profiles
* Extracts relevant candidate attributes
* Identifies experience, education, skills, certifications, and recruiter signals

---

## Recruiter-Based Scoring Engine

A custom recruiter-inspired scoring mechanism designed to evaluate candidates using multiple profile signals, including:

* Relevant experience
* Technical skills
* Educational qualifications
* Certifications
* Profile completeness
* Recruiter engagement signals

---

## Large-Scale Candidate Processing

* Successfully processed **100,000 candidate profiles**
* Ranked candidates using recruiter-inspired scoring
* Generated submission-ready ranked output

---

## Semantic Matching Prototype

Implemented semantic similarity using **Sentence Transformers (all-MiniLM-L6-v2)** to compare:

* Job Description
* Candidate Profiles

This enables contextual understanding beyond traditional keyword matching.

---

## Skill Match Prototype

Developed a skill matching module to measure alignment between:

* Required Job Skills
* Candidate Skills

This score is designed to complement semantic similarity and recruiter scoring.

---

## Hybrid Ranking Framework

Designed a hybrid ranking framework combining:

* Semantic Similarity Score
* Recruiter Score
* Skill Match Score

The proposed scoring formula is:

**Final Score = 0.5 × Semantic Score + 0.3 × Recruiter Score + 0.2 × Skill Match Score**

This architecture is designed for more intelligent and recruiter-aligned candidate ranking.

---

# System Architecture

```text
                    Job Description
                           │
                           ▼
                 Document Processing
                           │
                           ▼
                  JD Text Extraction
                           │
                           ▼

         Candidate Dataset (100,000 Profiles)
                           │
                           ▼
                 Feature Extraction Layer
                           │
                           ▼
              Recruiter Scoring Engine
                           │
                           ▼
              Semantic Matching Module
                           │
                           ▼
                 Skill Match Prototype
                           │
                           ▼
                 Hybrid Ranking Engine
                           │
                           ▼
         ranked_candidates_hybrid.csv
```

---

# Technology Stack

| Category                | Technology            |
| ----------------------- | --------------------- |
| Programming Language    | Python                |
| Data Processing         | Pandas, NumPy         |
| Machine Learning        | Sentence Transformers |
| Similarity Computation  | Scikit-learn          |
| Data Format             | JSONL                 |
| Development Environment | Google Colab          |

---

# Repository Structure

```text
AI-Candidate-Ranking-System/
│
├── Redrob_Hackathon.ipynb
├── README.md
├── requirements.txt
├── ranked_candidates_hybrid.csv
├── candidate_schema.json
├── job_description.docx
└── LICENSE
```

---

# Dataset Note

The original **candidates.jsonl** dataset (approximately **434 MB**) is not included in this repository because it exceeds GitHub's file size limits.

To execute the notebook, place the original hackathon dataset in the project directory before running the notebook.

---

# Output

The system generates a ranked candidate list in CSV format.

Output File:

`ranked_candidates_hybrid.csv`

Example:

| Candidate ID | Score |
| ------------ | ----: |
| CAND_008025  | 93.55 |
| CAND_005238  | 93.15 |
| CAND_007337  | 91.45 |

Higher scores indicate stronger alignment with the target job role.

---

# Future Improvements

### Advanced Semantic Search

* Cross-Encoder re-ranking
* BERT-based candidate ranking
* Context-aware profile understanding

### Intelligent Skill Analysis

* Skill synonym detection
* Skill ontology mapping
* Industry-specific skill weighting

### Explainable AI

Provide recruiter-friendly explanations such as:

> Candidate ranked highly because of strong Python expertise, relevant experience, high recruiter score, and excellent semantic alignment with the job description.

### Production Deployment

* REST API
* Streamlit Dashboard
* Recruiter Analytics Panel
* Real-Time Candidate Ranking
* Vector Database Integration (FAISS / Pinecone)

---

# Results

* Successfully processed **100,000 candidate profiles**
* Generated recruiter-based candidate rankings
* Produced **ranked_candidates_hybrid.csv**
* Implemented semantic matching and hybrid ranking prototypes
* Designed a scalable architecture for AI-assisted recruitment

---

# Author

**Marri Lalitha Raga Pravallika**

B.Tech – Electronics and Communication Engineering

Pragati Engineering College
