# Prompt Engineering with FLAN-T5

This project demonstrates various prompt engineering techniques using the [FLAN-T5 Base](https://huggingface.co/google/flan-t5-base) model for dialogue summarization. It explores how different prompting strategies affect the quality of generated summaries using the [DialogSum](https://huggingface.co/datasets/knkarthick/dialogsum) dataset.

## Overview

The notebook covers the following concepts:
- **Zero-shot Inference**: Asking the model to summarize a dialogue without providing any examples.
- **One-shot Inference**: Providing a single example of a dialogue and its summary to guide the model.
- **Few-shot Inference**: Providing multiple examples to further improve the model's understanding of the task.
- **Generative Configuration**: Adjusting inference parameters (like `temperature` and `top_p`) to control the creativity and randomness of the output.

## Prerequisites

To run this notebook, you need the following Python libraries:

- `torch`
- `datasets`
- `transformers`

You can install them using pip:

```bash
pip install torch datasets transformers
```

## Dataset

The project uses the **DialogSum** dataset (`knkarthick/dialogsum`), which consists of real-life scenarios, including task-oriented dialogues and daily conversations. The goal is to generate a concise summary of the dialogue.

## Model

We use **Google's FLAN-T5 Base**, a sequence-to-sequence model fine-tuned on a variety of tasks. It is well-suited for text generation tasks like summarization.

## Usage

1.  Clone the repository or download the notebook.
2.  Ensure you have the required dependencies installed.
3.  Run the `prompt_engineering.ipynb` notebook in a Jupyter environment (like JupyterLab, VS Code, or Google Colab).

## Key Steps in the Notebook

1.  **Load Dataset & Model**: Initialize the DialogSum dataset and the FLAN-T5 model.
2.  **Zero-shot Inference**: Test the model's baseline performance without specific instructions.
3.  **Prompt Construction**: Create functions to dynamically generate prompts with varying numbers of examples.
4.  **One-shot & Few-shot Inference**: Evaluate how adding examples improves the summary quality.
5.  **Parameter Tuning**: Experiment with `GenerationConfig` to fine-tune the output style.

## Results

The notebook demonstrates that providing context through examples (One-shot and Few-shot) generally leads to better and more consistent summaries compared to Zero-shot inference.
