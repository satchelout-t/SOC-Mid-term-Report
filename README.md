# Project Report: Character-Level Text Generation with a Transformer Model

**Name:** Harpreet Singh 
**Project:** SoC - ChatGPT from Scratch (End-Term Submission)
**Date:** July 31, 2025

## 1. Project Overview

This project implements a decoder-only Transformer model for character-level text generation. The primary goal was to explore the model's ability to learn and replicate distinct writing styles from varied text corpora. Two separate models were developed and analyzed:

1.  A model trained from scratch on the movie script of *Mission: Impossible - Fallout*.
2.  A model utilizing pre-trained weights to generate text in the style of Sir Arthur Conan Doyle's Sherlock Holmes stories.

The project covers the entire machine learning pipeline, including data preprocessing, model implementation, training, and text generation, using Python and the PyTorch library within Jupyter Notebooks.

## 2. Project Development Journal

This project was built over several weeks, starting from foundational concepts and progressing to the final implementation. The detailed weekly progress, covering topics from Python basics to backpropagation and PyTorch, is documented separately.

**➡️ [Click here to view the detailed week-by-week progress log.](PROGRESS_LOG.md)**

---

## 3. Model Architecture

The core of this project is a Transformer-based language model, specifically a GPT-like decoder-only architecture. This architecture was chosen for its proven effectiveness in sequential data processing and language modeling tasks.

The key parameters, consistent across both notebooks, are:

* **Vocabulary Size (`vocab_size`):** 92
* **Embedding Dimension (`n_embd`):** 384
* **Context Length (`block_size`):** 256 characters
* **Number of Transformer Blocks (`n_layer`):** 4
* **Number of Attention Heads (`n_head`):** 4
* **Dropout Rate:** 20% to prevent overfitting

## 4. Datasets

Two distinct datasets were used to train and evaluate the models:

* **`MI_Fallout.txt`**: The complete movie script for *Mission: Impossible - Fallout*.
* **`sh.txt`**: A text file containing excerpts from Sir Arthur Conan Doyle's "A Scandal in Bohemia."

## 5. Implementation and Execution

The project is implemented in two separate Jupyter Notebooks.

* **`Skynet.ipynb`**: Details the process of training a model from scratch on the `MI_Fallout.txt` dataset.
* **`Skynet_SH.ipynb`**: Demonstrates inference using a pre-trained model (`farturConanDoyle.pth`) to generate text in the style of Sherlock Holmes.

## 6. Results and Analysis

Both models were executed successfully, confirming that the entire pipeline—from data loading to final text generation—is fully functional.

The results demonstrated that the models learned the distinct stylistic patterns of their respective training corpora:
* The **Mission: Impossible model** generated text that captured the vocabulary and script-like format of the source material.
* The **Sherlock Holmes model** produced prose that clearly mimicked the classic, literary style of Sir Arthur Conan Doyle.

A video recording of the live demonstration is available in the project's shared drive.

**➡️ [View Project Demonstration Video in Shared Folder](https://drive.google.com/drive/folders/1wo5KXhYMYptJblPmpVuY7Fc-F4QsqwfZ?usp=sharing)**

## 7. Conclusion and Future Work

This project successfully demonstrates that a character-level Transformer model can learn and reproduce complex stylistic patterns. For future improvements, subword tokenization and a larger model scale could be explored.

## 8. Instructions to Run

1.  Ensure you have Python, PyTorch, and Jupyter Notebook installed.
2.  Place all project files (`.ipynb`, `.txt`, `.pth`) in the same directory.
3.  To see the *Mission: Impossible* model train and generate, run all cells in **`Skynet.ipynb`**.
4.  To see the *Sherlock Holmes* model generate text, run all cells in **`Skynet_SH.ipynb`**.
