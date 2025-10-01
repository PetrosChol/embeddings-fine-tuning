# Fine-Tuning Sentence Transformer Models for Enhanced RAG Retrieval

This repository contains a complete, step-by-step Jupyter Notebook demonstrating how to fine-tune a sentence-transformer embedding model for a specialized domain.

While fine-tuning LLMs is a popular topic, optimizing the "Retrieval" part of Retrieval-Augmented Generation (RAG) is often overlooked. This project addresses that gap by providing a modern, robust, and easy-to-follow guide for specializing an embedding model, which is critical for high-quality retrieval.

This code is the basis for the Medium article: **[Most RAG Tutorials Are Incomplete. Here's How to Properly Fine-Tune Your Embedding Model](https://your-medium-link-here)**.

## Key Features

-   **Best-Practice Evaluation:** Implements a proper **train, validation, and test split** to ensure unbiased and trustworthy results.
-   **Modern Libraries:** Uses the latest, recommended libraries including `sentence-transformers`, `transformers`, and `datasets` from Hugging Face.
-   **Quantifiable Results:** Demonstrates a clear and significant improvement in retrieval performance, with a **10.59% increase in NDCG@10**.
-   **Step-by-Step Guide:** The notebook is structured as a tutorial, explaining the "why" behind each step, from data preparation to final evaluation.

## The Result: A Clear Performance Boost

The goal of this project was to prove that fine-tuning can significantly improve retrieval performance. By training the `all-MiniLM-L6-v2` model on a specialized financial dataset, we achieved a substantial uplift across all key information retrieval metrics on an unseen test set.

| Metric                      | Original Model | Fine-Tuned Model | Improvement |
| --------------------------- | :------------: | :--------------: | :---------: |
| **test_cosine_ndcg@10**     |    0.743877    |     0.822646     | **10.59%**  |
| **test_cosine_accuracy@1**  |    0.628571    |     0.717143     | **14.09%**  |
| **test_cosine_map@100**     |    0.711087    |     0.793453     | **11.58%**  |
| test_cosine_accuracy@3      |    0.762857    |     0.844286     |   10.67%    |
| test_cosine_accuracy@5      |    0.818571    |     0.891429     |    8.90%    |
| test_cosine_accuracy@10     |    0.860000    |     0.922857     |    7.31%    |
| test_cosine_mrr@10          |    0.706662    |     0.790068     |   11.80%    |

## Getting Started

> **Environment Note:** This notebook was developed and tested in a **Google Colab** environment using a **T4 GPU**, which is available on the free tier. The code should be compatible with any standard environment that has a CUDA-enabled GPU.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/PetrosChol/embeddings-fine-tuning.git
    cd your-repo-name
    ```

2.  **Create a virtual environment and install dependencies:**
    It is highly recommended to use a virtual environment.
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

## Repository Structure

```
.
├── embedding_finetuning_rag_demo.ipynb  # The main notebook with all the code and explanations.
├── requirements.txt                     # A list of Python packages required to run the notebook.
└── README.md                            # This file.
```
