# Retrieval-Augmented Generation (RAG) Evaluation

Carnegie Mellon University – Fall 2025
95820 Applications of NL(X) and LLM - Science, Engineering and Applications Assignment 2

This project implements and evaluates a Retrieval-Augmented Generation (RAG) pipeline using the RAG Mini Wikipedia dataset. The system compares multiple prompting strategies, embedding models, and retrieval depths, and further integrates enhancements (query rewriting + reranking). Evaluation combines traditional token-level metrics (F1, Exact Match) with semantic quality metrics (RAGAs).

## Project Structure

```
Assignment2/
├── data/                  # Datasets
│   ├── processed/         # Cleaned passages and QA pairs
│   └── evaluation/        # Golden evaluation queries
├── results/               # Experimental results
│   ├── evaluation_f1_em.csv      # F1 / EM results
│   └── ragas_eval_results.json   # RAGAs results
├── src/                   # Source notebooks
│   ├── step0_data_exploration.ipynb
│   ├── step1_naive_rag.ipynb
│   ├── step2_evaluation.ipynb
│   ├── step3_enhanced_rag.ipynb
│   ├── step4_enhancement_analysis.ipynb
│   ├── step5a_add_contexts.ipynb
│   └── step5b_RAGAS.ipynb
└── Evaluation Report.docx # Final written report
```

## How to Run

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Run notebooks in order


## Key Results

- **Best Baseline**: Persona + MPNet + k=5 → F1 ≈ 49.9, EM ≈ 40.0
- **Enhanced System** (query rewriting + reranking):
  - F1/EM plateaued near baseline
  - RAGAs metrics improved, especially Context Precision (0.73 → 0.87)

*(See Evaluation Report.pdf for full analysis.)*

## Attribution & AI Usage

This project used ChatGPT (OpenAI GPT-4/GPT-5) for:
- Debugging RAG coding issues (e.g., input type correction, RAGAs API key handling)
- Documentation drafting and report structuring
- Explaining evaluation metrics and trade-offs

All code and analysis were verified manually and cross-checked against assignment requirements.

## License

This project is for academic coursework only. Do not distribute outside the CMU course without permission.
