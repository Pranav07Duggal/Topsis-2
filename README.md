# TOPSIS for Text Sentence Similarity Model Selection

## Overview
This project applies the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method to rank various **pre-trained models** for **text sentence similarity** based on multiple evaluation criteria.

## Models Considered
The following **five pre-trained models** were evaluated:
1. **SBERT (Sentence-BERT)**
2. **Universal Sentence Encoder (USE)**
3. **GPT-Embedding**
4. **BERTScore**
5. **GloVe (Global Vectors for Word Representation)**

## Evaluation Criteria
Each model was assessed based on the following five key criteria:
- **Cosine Similarity Score** (Higher is better)
- **Inference Speed (Time per prediction in seconds)** (Lower is better)
- **Memory Usage (MB)** (Lower is better)
- **Model Size (MB)** (Lower is better)
- **Accuracy on a Benchmark Dataset** (Higher is better)

## Methodology
The **TOPSIS method** ranks models by measuring their **Euclidean distance** from the **ideal best** and **ideal worst** solutions. The steps followed are:
1. **Create a Decision Matrix** with models as rows and criteria as columns.
2. **Normalize the Matrix** to bring all values to a common scale.
3. **Assign Weights** to each criterion based on importance.
4. **Compute the Ideal Best & Worst Solutions**.
5. **Calculate the Euclidean Distance** of each model from both solutions.
6. **Compute the TOPSIS Score** (Closer to 1 means better ranking).
7. **Rank the Models** based on their TOPSIS scores.

## Results
The models were ranked based on their **TOPSIS scores**, with **higher scores indicating better performance**. Below is the final ranking:

| Rank | Model             | TOPSIS Score |
|------|------------------|--------------|
| 1    | GPT-Embedding    | 0.92         |
| 2    | SBERT            | 0.85         |
| 3    | BERTScore        | 0.82         |
| 4    | USE              | 0.78         |
| 5    | GloVe            | 0.70         |
