# tls-covid19 dataset

## Overview

The tls-covid19 dataset for multi-document timeline summarization, consists of news stories regarding specific queries from portuguese and english news outlets. The news sources include Jornal Público, Jornal Observador, CNN and The Guardian.

Each query dataset is composed of:

1.  Timeline: set of human-selected stories, retrieved from the key moments of the news outlet covid's liveblog
2.  Input documents:
    * Liveblog: set of news stories from the liveblog, i.e, a serie of posts which intended to provide a rolling textual coverage of an ongoing event;
    * API/Google: set of news stories collected from either the news source API (if available) or from Google;
    
The timeline summarization task consists of predicting the timeline stories, from the input documents.

The following illustrations show the summarization task and an example of the general structure of the dataset.

![Dataset structure](tls-covid19-struct.png?raw=true "Task and dataset structure")

## Dataset Generation

We do not provide a link to directly download the dataset. Instead, we provide a Google Colab notebook with the steps to collect the dataset. Try it here: [<img src="https://colab.research.google.com/assets/colab-badge.svg" align="center">](https://colab.research.google.com/drive/1sJIiURksx-Y6doNuZQNAezWXEZ1NVfwv?usp=sharing)
