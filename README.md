# Resume & Job Description Matcher

An automated text-matching tool that parses PDF resumes and evaluates alignment against target job descriptions using Natural Language Processing (NLP) techniques.

## Overview

This project provides a straightforward pipeline to extract raw text content from a candidate's PDF resume and calculate a similarity match score against a provided job description. By leveraging word-frequency vectorization and cosine distance, the script quantifies how closely a resume's terminology reflects the role's specified qualifications, technical requirements, and core responsibilities.

## Key Features

- **Automated PDF Parsing:** Extracts text directly from multi-page PDF documents using `PyPDF2`.
- **Text Vectorization:** Converts resume text and job description specifications into frequency count vectors via Scikit-Learn’s `CountVectorizer`.
- **Cosine Similarity Scoring:** Measures the cosine angle between vector representations using `cosine_similarity` to deliver a normalized percentage match score.

## Tech Stack & Dependencies

- **Language:** Python
- **Libraries:**
  - `PyPDF2` (PDF extraction)
  - `scikit-learn` (Text vectorization and cosine similarity calculations)

## How It Works

1. **Text Extraction:** `PyPDF2.PdfReader` reads and compiles text content across all pages of the input PDF resume.
2. **Preprocessing & Vectorization:** The combined resume text and target job description are converted to lowercase and transformed into count vectors using `CountVectorizer`.
3. **Similarity Analysis:** `cosine_similarity` evaluates the mathematical alignment between both vectors, outputting a match score rounded to two decimal places.
   
