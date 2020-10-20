# tls-covid19 dataset

## What

The *tls-covid19* is a dataset for multi-document timeline summarization. It consists of news stories regarding specific topics from portuguese and english news outlets. The news sources include [Jornal Público](https://www.publico.pt/) (PT) and [CNN](https://edition.cnn.com/) (EN).
For each news source and topic there is a ground truth timeline and a set of news articles. The goal is to predict the timeline from the set of news articles.

The following image shows the summarization task and an example of the general structure of the dataset for one topic.

![Dataset structure](img/tls-covid19-struct.png?raw=true "Task and dataset structure")

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

As of **12/10/2020**

<table>
<thead>
  <tr>
    <th colspan="3"></th>
    <th colspan="4">Input Docs</th>
    <th colspan="3">Ground-Truth</th>
    <th colspan="2">Compression</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Lang</td>
    <td>Source</td>
    <td>#Topics</td>
    <td>#Docs</td>
    <td>Avg #sents</td>
    <td>Avg #dates</td>
    <td>Avg sents/dates</td>
    <td>Avg #sents</td>
    <td>Avg #dates</td>
    <td>Avg sents/dates</td>
    <td>Sents</td>
    <td>Dates</td>
  </tr>
  <tr>
    <td>PT</td>
    <td>Público</td>
    <td>368</td>
    <td>34,745</td>
    <td>801.20</td>
    <td>49.62</td>
    <td>16.15</td>
    <td>33.02</td>
    <td>20.05</td>
    <td>1.65</td>
    <td>4.12</td>
    <td>40.41</td>
  </tr>
  <tr>
    <td>EN</td>
    <td>CNN</td>
    <td>35</td>
    <td>16,332</td>
    <td>4690.17</td>
    <td>123.14</td>
    <td>38.09</td>
    <td>27.11</td>
    <td>18.17</td>
    <td>1.49</td>
    <td>0.58</td>
    <td>14.76</td>
  </tr>
</tbody>
</table>


Distribution of topics type:

| Type  |   PT   |   EN   |
| :---: | :----: | :----: |
|  PER  |   52   |    3   |
|  ORG  |   25   |    4   |
|  LOC  |   198  |    19  |
|  MISC |   9    |    5   |
|  KW   |   84   |    4   |


WordClouds EN/PT:

![Word Clouds](img/wc_en-pt_merged.png?raw=true "English and portuguese word clouds")