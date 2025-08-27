

# Translation and Summarization Notebook

## Overview

This project demonstrates the use of **state-of-the-art Transformer models** for two main Natural Language Processing (NLP) tasks:

1. **Translation** – translating text from English to French using the `facebook/nllb-200-distilled-600M` model.
2. **Summarization** – generating a concise summary of long text using the `facebook/bart-large-cnn` model.

Both tasks are implemented in a Google Colab notebook for easy execution without local setup.

---

## Notebooks in this repository

1. **Translation\_and\_Summarization.ipynb**

   * This is the original notebook with all code, outputs, and results.
   * Can be downloaded and executed locally or in Colab.

2. **Translation\_and\_Summarization\_clean.ipynb**

   * This is a cleaned version of the notebook.
   * All outputs and execution counts have been cleared.
   * Useful for sharing, version control, or uploading to GitHub.

---

## What I Learned

* How to use **Hugging Face Transformers pipelines** for translation and summarization.
* How to manage GPU/CPU memory in Colab by deleting large objects and running garbage collection.
* How to structure NLP workflows for text processing and results extraction.
* The practical differences between raw and cleaned notebooks for version control.

---

## Libraries Used

* **[transformers](https://huggingface.co/transformers/)** – for pre-trained NLP models.
* **torch** – used for model computations and specifying data types.
* **gc (garbage collection)** – to free up memory during notebook execution.

---

## Features

### Translation Pipeline

* Uses the **NLLB (No Language Left Behind)** model: `facebook/nllb-200-distilled-600M`.
* Translates English text to French.
* Example input:

```text
My puppy is adorable, Your kitten is cute. Her panda is friendly. His llama is thoughtful. We all have nice pets!
```

* Example output:

```json
[
  {"translation_text": "Mon chiot est adorable, Votre chaton est mignon. Son panda est amical. Son lama est réfléchi. Nous avons tous de jolis animaux !"}
]
```

### Summarization Pipeline

* Uses the **BART model**: `facebook/bart-large-cnn`.
* Summarizes long paragraphs into concise summaries.
* Example input:

```text
Paris is the capital and most populous city of France, with an estimated population of 2,175,601 residents as of 2018, in an area of more than 105 square kilometres...
```

* Example output:

```json
[
  {"summary_text": "Paris is the capital and most populous city of France, home to over 2 million residents in the city and more than 12 million in the region."}
]
```

---

## How to Use

1. Open either notebook in **Google Colab**.
2. Install dependencies (if prompted):

```bash
!pip install transformers
```

3. Run each cell step by step to see translation and summarization results.

---
