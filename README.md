# PDF Question Answering

This project answers questions from PDF documents with a small retrieval and question-answering pipeline. It compares results from a clean PDF and a noisy PDF.

## How it works

1. Read the question and document PDFs.
2. Clean the noisy document text.
3. Split the text into small chunks.
4. Use TF-IDF and cosine similarity to find relevant chunks.
5. Use `deepset/roberta-base-squad2` to extract an answer.
6. Save the answers and confidence scores as JSON files.

## Requirements

- Python 3.10+
- Jupyter Notebook
- PyTorch
- Transformers
- pypdf
- scikit-learn

Install the packages with:

```bash
pip install jupyter pypdf scikit-learn transformers torch
```

## Input files

Place these files in the project folder:

- `Questions.pdf`
- `Test PDF (Easy).pdf`
- `Test PDF (Hard).pdf`

## Run the project

Open `1000128462_Assignment 2.ipynb` in Jupyter and run all cells. The first run downloads the RoBERTa QA model from Hugging Face.

The notebook creates:

- `easy_answers.json`
- `hard_answers.json`

Each result includes the question, extracted answer, and confidence score.
