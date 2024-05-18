# Wikipedia Document Search Engine

This project is an information retrieval system designed as a search engine for Wikipedia documents. The project utilizes various natural language processing techniques, including data cleaning with NLTK, TF-IDF ranking with PyTerrier, and document ranking with BERT.

## Table of Contents
- [Data Collection](#data-collection)
- [Preprocessing](#preprocessing)
- [Indexing](#indexing)
- [Query Processing](#query-processing)
- [Ranking](#ranking)
- [Query Expansion](#query-expansion)
- [Evaluation](#evaluation)
- [BERT-based Ranking](#bert-based-ranking)
- [GUI](#gui)
- [Installation](#installation)
- [Usage](#usage)

## Data Collection
We used the `ir_datasets` library to load the Wikipedia CLIR (Cross-Language Information Retrieval) dataset.

## Preprocessing
The preprocessing step includes:
- Converting text to lowercase
- Removing HTML tags, punctuations, and numbers
- Tokenizing the text
- Removing stopwords
- Lemmatizing and stemming the tokens

## Indexing
We indexed the preprocessed text data using PyTerrier's `DFIndexer`.

## Query Processing
Queries are processed in a similar way to the documents:
- Converted to lowercase
- HTML tags, punctuations, and numbers removed
- Tokenized
- Stopwords removed
- Lemmatized and stemmed

## Ranking
We used the TF-IDF model for initial document ranking based on the query terms.

## Query Expansion
To improve retrieval performance, we used the RM3 query expansion technique provided by PyTerrier.

## Evaluation
The system was evaluated using the queries and qrels from the Wikipedia CLIR dataset.

## BERT-based Ranking
For enhanced document ranking, we incorporated a BERT-based model using the `xpmir` library.

## GUI
A simple graphical user interface (GUI) was created using Streamlit to allow users to input search queries and display the relevant documents.

## Installation
To set up the environment, run the following commands:

```bash
!pip install python-terrier --quiet
!pip install nltk --quiet
!pip install --ignore-installed blinker --quiet
!pip install git+https://github.com/experimaestro/experimaestro-ir.git --quiet
!pip install transformers --quiet
!pip install streamlit --quiet
```

## Usage
To run the search engine, execute the following script:
```bash
!streamlit run main.py & npx localtunnel --port 8501
```

## Code

The main code for the project is provided in the main.py file, which handles data collection, preprocessing, indexing, query processing, and the Streamlit GUI.
main.py is included in the Jupyter notebook provided

## Conclusion
This project demonstrates the implementation of an information retrieval system with various models and methods to enhance retrieval performance, including traditional TF-IDF and modern BERT-based approaches.
