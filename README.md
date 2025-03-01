# NLP Project

This project focuses on natural language processing (NLP) techniques to analyze and classify textual data. It utilizes various machine learning models and embeddings to evaluate performance.

## Installation

Ensure you have the required dependencies installed before running the notebook:

```bash
pip install nltk scikit-learn xgboost transformers gensim
```

## Selecting a Dataset

The script supports three different datasets. To choose a dataset, uncomment one of the following lines in the notebook:


1. Primary dataset: Custom python code extraction of Gilbert Strang’s textbook
   [questions_with_chapters.json]
2. Synthetic dataset: Manually extracted dataset with synthetic question generation to create balanced dataset of Gilbert Strang’s textbook
[questions_with_chapters1_manual.json]
3. Noiseless dataset: Only latex questions with no noise for book3
   [questions_with_chapters3.json]
   
```python
# df = pd.read_json("/kaggle/input/data-book1json/questions_with_chapters.json")
# df = pd.read_json("/kaggle/input/data-book3json/questions_with_chapters3.json")
# df = pd.read_json("/kaggle/input/data-book1manualjson/questions_with_chapters1_manual.json")
```

For example, if you want to use `questions_with_chapters.json`, modify the code like this:

```python
df = pd.read_json("/kaggle/input/data-book1json/questions_with_chapters.json")
```

## Running the Notebook

1. Open the Jupyter Notebook.
2. Select and uncomment the desired dataset (as mentioned above).
3. Run all cells in the notebook.

## Evaluating Individual Embeddings

The section **Individual Embedding Evaluation** is currently commented out. If you want to evaluate the performance of each embedding method, uncomment the relevant lines in that section.

To do this, locate the section in the notebook and remove the `#` symbols before the lines of code to enable execution.

## Results;
You can find the final results under the section "Best Model" at the end. 

## Authors

This project was developed as part of an NLP research initiative.

## License

This project is open-source and available for further development and enhancement.

