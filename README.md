# Dialogue Summarization using Generative AI with DialogSum Dataset

This project explores different prompting techniques (zero-shot, one-shot, and few-shot) for dialogue summarization using generative AI models on Amazon SageMaker Studio Lab. The project uses the [DialogSum dataset](https://huggingface.co/datasets/knkarthik/dialogsum) from Hugging Face, which contains dialogue-summary pairs specifically designed for conversation summarization.

## Project Overview

In this project, I:

1. Used the DialogSum dataset from Hugging Face as both test data and few-shot examples
2. Implemented dialogue summarization using FLAN-T5
3. Compared three prompting strategies:
   - Zero-shot: No examples provided
   - One-shot: Single example from DialogSum provided
   - Few-shot: Multiple examples from DialogSum provided
4. Evaluated results using ROUGE metrics
5. Analyzed the quality and characteristics of each approach
6. Visualized the results to identify patterns and insights

## Key Findings

- Adding examples from the DialogSum dataset significantly improves summarization quality
- Few-shot prompting consistently outperforms zero-shot and one-shot approaches across all ROUGE metrics
- Different dialogue types benefit differently from prompt engineering
- There's a trade-off between summary length and information density across methods

## Repository Structure

- `dialogsum_summarization.ipynb`: Main notebook with implementation and analysis
- `dialogue_summarization_results.csv`: Generated summaries and reference summaries
- `rouge_scores.csv`: ROUGE metrics for each approach
- `summary_lengths.csv`: Word count data for each summary
- `rouge_scores.png`: Visualization of ROUGE metrics
- `summary_lengths.png`: Visualization of summary lengths
- `prompt_engineering_observations.md`: Detailed observations and analysis

## Setup Instructions

To run this project on Amazon SageMaker Studio Lab:

1. Sign up for SageMaker Studio Lab at https://studiolab.sagemaker.aws/
2. Start a runtime (GPU recommended)
3. Clone this repository
4. Open `dialogsum_summarization.ipynb` and run all cells

## Requirements

- Python 3.8+
- PyTorch
- Transformers library
- Datasets library
- Evaluate library
- NLTK
- pandas, matplotlib

## Future Work

- Fine-tune models on the DialogSum dataset
- Test with additional LLMs beyond FLAN-T5
- Implement and compare more advanced prompting techniques
- Explore task-specific prompt engineering strategies for dialogue summarization
