# tls-covid19 dataset

## What

The *tls-covid19* is a multi-lingual and multi-document Timeline Summarization (TLS) annotated dataset built to foster the emergence and evaluation of new algorithms, and, at the same time, enable the study of news coverage about the COVID-19 pandemic. It consists of a number of curated topics related to the Covid-19 outbreak, with associated news articles from portuguese and english news outlets and their respective reference timelines as gold-standard. The news sources include [Jornal Público](https://www.publico.pt/) (PT) and the[CNN](https://edition.cnn.com/) (EN). The following figure shows the format and the structure  of the dataset.

![Dataset structure](img/tls-covid19-structure.jpg?raw=true "Dataset structure")

## Why

The rise of social media and the explosion of digital news in the web sphere have created new challenges to extract knowledge and make sense of published information. Automated timeline generation appears in this context as a promising answer to help users dealing with this information overload problem. Formally, Timeline Summarization (TLS) can be defined as a subtask of Multi-Document Summarization (MDS) conceived to highlight the most important information during the development of a story over time by summarizing long-lasting events in a timely ordered fashion. As opposed to traditional MDS, however, TLS has a limited number of publicly available datasets. This lack of datasets is even more noticeable for low resource languages, including Portuguese, which despite being the sixth most spoken language in the world [Ethnologue (2019, 22nd edition)] lacks a specific TLS dataset.

Following the worldwide coverage of the coronavirus pandemic, we propose the TLS-Covid19 dataset, a novel corpus for the Portuguese and English languages. 

## How

To create this dataset, we take advantage of liveblogs, a webpage where news media outlets offer a daily live coverage about an ongoing event. Each liveblog (usually with a different URL) consists of a set of news stories and a set of key moments. The key moments stories are manually selected by journalists from the whole set of news articles, thus giving rise to the ground-truth timeline. Data from CNN is collected through the use of the [Newspaper 3k](https://newspaper.readthedocs.io/) python library. Instead, data from Público is obtained through an API.

As a rule-of-thumb, we consider the beginning of the liveblog coverage as the start time-period. For instance, CNN is tracked since April 4th, 2020 and Público since March 16th. Our aim is to continue expanding the dataset with further articles and possibly new topics until the end of the outbreak and/or the end of the liveblogs’ coverage. We anticipate that as the pandemic evolves, the amount of data collected will grow significantly.   

The source code to reproduce the dataset is available in a Google Colab notebook. Try it here: [<img src="https://colab.research.google.com/assets/colab-badge.svg" align="center">](https://colab.research.google.com/drive/1sJIiURksx-Y6doNuZQNAezWXEZ1NVfwv?usp=sharing). You can also reach us for further details about the dataset.

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
