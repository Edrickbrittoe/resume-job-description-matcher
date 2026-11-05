# Resume & Job Description Matcher

An automated text-matching tool that parses PDF resumes and evaluates alignment against target job descriptions using Natural Language Processing (NLP) techniques[cite: 1].

## Overview

This project provides a straightforward pipeline to extract raw text content from a candidate's PDF resume and calculate a similarity match score against a provided job description[cite: 1]. By leveraging word-frequency vectorization and cosine distance, the script quantifies how closely a resume's terminology reflects the role's specified qualifications, technical requirements, and core responsibilities[cite: 1].

## Key Features

- **Automated PDF Parsing:** Extracts text directly from multi-page PDF documents using `PyPDF2`[cite: 1].
- **Text Vectorization:** Converts resume text and job description specifications into frequency count vectors via Scikit-Learn’s `CountVectorizer`[cite: 1].
- **Cosine Similarity Scoring:** Measures the cosine angle between vector representations using `cosine_similarity` to deliver a normalized percentage match score[cite: 1].

## Tech Stack & Dependencies

- **Language:** Python[cite: 1]
- **Libraries:**
  - `PyPDF2` (PDF extraction)[cite: 1]
  - `scikit-learn` (Text vectorization and cosine similarity calculations)[cite: 1]

## How It Works

1. **Text Extraction:** `PyPDF2.PdfReader` reads and compiles text content across all pages of the input PDF resume[cite: 1].
2. **Preprocessing & Vectorization:** The combined resume text and target job description are converted to lowercase and transformed into count vectors using `CountVectorizer`[cite: 1].
3. **Similarity Analysis:** `cosine_similarity` evaluates the mathematical alignment between both vectors, outputting a match score rounded to two decimal places[cite: 1].
