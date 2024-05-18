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

## Used Tools and Libraries

### Tools:
- **PyTerrier**: Utilized for indexing, retrieval models (TF-IDF), and query expansion techniques.
- **Streamlit**: Used to create the graphical user interface (GUI) for the search engine.
- **NLTK (Natural Language Toolkit)**: Employed for text preprocessing tasks such as tokenization, stopword removal, lemmatization, and stemming.
- **IR-Datasets**: Used for loading and handling the Wikipedia CLIR dataset for information retrieval tasks.

### Models:
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Traditional information retrieval model used for initial document ranking based on the frequency of terms.
- **RM3 (Relevance Model 3)**: Query expansion technique applied to improve retrieval performance by expanding the initial query with additional relevant terms.
- **BERT (Bidirectional Encoder Representations from Transformers)**: Utilized for advanced document ranking using contextual embeddings and neural network-based ranking.

### Libraries:
- **PyTerrier**: A Python framework for large-scale information retrieval research.
- **TensorFlow**: Deep learning library used for training and inference of neural network models.
- **NLTK (Natural Language Toolkit)**: Python library for natural language processing tasks.
- **Transformers**: Library providing pre-trained models and utilities for working with transformer-based models like BERT.
- **Streamlit**: Open-source Python library for creating web applications for data science and machine learning projects.

These tools, models, and libraries were instrumental in building an effective and efficient search engine for Wikipedia documents, combining traditional IR techniques with modern deep learning approaches for improved retrieval performance and user experience.


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
