# Running Jupyter Notebooks from GitHub

## Running in Kaggle Notebooks
1. Download the `.ipynb` file from GitHub.
2. Upload it to **Kaggle Notebooks** (`https://www.kaggle.com/code`).
3. Run the notebook in Kaggle’s cloud environment.


## Loading a Dataset from GitHub
The notebook has dataset loaded directly from GitHub, if it doesn't work kindly manually download and upload dataset on kaggle

---

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
# ----- Primary Dataset
# df = pd.read_json("https://raw.githubusercontent.com/anushkachaubey/NLP/main/Datasets/Primary_Book1/questions_with_chapters.json")

# ----- Synthetic Dataset
# df = pd.read_json("https://raw.githubusercontent.com/anushkachaubey/NLP/main/Datasets/Synthetic_Book1/questions_with_chapters1_manual.json")

# ----- Noiseless Dataset
# df = pd.read_json("https://raw.githubusercontent.com/anushkachaubey/NLP/main/Datasets/Noiseless_Book3/questions_with_chapters3.json")
```

For example, if you want to use `questions_with_chapters.json`, modify the code like this:

```python
df = pd.read_json("https://raw.githubusercontent.com/anushkachaubey/NLP/main/Datasets/Primary_Book1/questions_with_chapters.json")
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


# Math Textbook Question Extraction

The `extract.ipynb` file is designed to extract questions from a math textbook PDF. It processes the text to identify chapters, problem sets, and individual questions.

## How to run
1. Download the `.ipynb` file from GitHub.
2. Upload it to **Kaggle Notebooks** (`https://www.kaggle.com/code`) or run it on local
3. Ensure book1.pdf is also downloaded in the same location
4. Run the notebook 

## How It Works

1. **PDF Extraction**: The script reads the PDF using `pdfplumber` and extracts the raw text.
2. **Problem Set Identification**: The script identifies problem sets using regex patterns.
3. **Question Extraction**: Questions are extracted based on number patterns (`1.`, `2.`, etc.) and common keywords like "Solve," "Prove," and "Evaluate."
4. **Chapter Mapping**: Each extracted question is mapped to its respective chapter.
5. **Saving Results**: The extracted questions are stored in `questions_with_chapters.txt` for further analysis.

## Running the Script

1. Ensure you have `pdfplumber` installed:
   ```bash
   pip install pdfplumber
   ```
2. Place your textbook PDF in the appropriate directory and update the file path:
   ```python
   pdf_path = "book1.pdf"
   ```
3. Run all cells to extract and save questions.

## Output Files
- `extracted_text.txt`: Contains the full extracted text from the PDF.
- `problem_sets.txt`: Contains identified problem sets.
- `questions_extracted.txt`: Contains raw extracted questions.
- `questions_with_chapters.txt`: Contains structured questions with their respective chapters.
- `questions_with_chapters.json`: Final Dataset

## Authors

This project was developed as part of an NLP research initiative.

## License

This project is open-source and available for further development and enhancement.



