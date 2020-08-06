# tls-covid19 dataset

## What

The *tls-covid19* is a dataset for multi-document timeline summarization. It consists of news stories regarding specific topics from portuguese and english news outlets. The news sources include [Jornal Público](https://www.publico.pt/), [Jornal Observador](https://observador.pt/), [CNN](https://edition.cnn.com/) and [The Guardian](https://www.theguardian.com/international).
For each news source and topic there is a ground truth timeline and a set of news articles. The goal is to predict the timeline from the set of news articles.

The following image shows the summarization task and an example of the general structure of the dataset for one topic.

![Dataset structure](tls-covid19-struct.png?raw=true "Task and dataset structure")

## Why

Multi-document timeline summarization is a challenging task with a lack of datasets. This deficit is even more noticeable for low resource languages.

Portuguese is a low resource language, despite being the sixth most spoken language in the world [Ethnologue (2019, 22nd edition)]. In fact, we do not know any document summarization corpus for the portuguese language.

The worldwide coverage of the coronavirus pandemic presents a good opportunity to create a large multilingual dataset for timeline summarization.

## How

We take advantage of liveblog platforms to create the dataset. A liveblog is a daily live coverage about an ongoing event. Each liveblog consists of a set of news stories and a set of key moments. The key moments stories are manually selected by journalists from the whole set of news articles.
Therefore, we consider the key moments as the ground-truth timeline.
The liveblogs are collected through either the news source API (if available) or web scraping.

We intend to continue updating the corpus as long as the liveblogs are updated.

The source code to reproduce the dataset is available in a Google Colab notebook. Try it here: [<img src="https://colab.research.google.com/assets/colab-badge.svg" align="center">](https://colab.research.google.com/drive/1sJIiURksx-Y6doNuZQNAezWXEZ1NVfwv?usp=sharing)

## Statistics

As of **30/06/2020**

Number of topics:
   - PT: 50
   - EN: 12

Number of documents:
   - PT: 18674
   - EN: 11354
