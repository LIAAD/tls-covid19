# TLS-Covid19 dataset

## What

The *TLS-Covid19* is a multi-lingual and multi-document Timeline Summarization (TLS) annotated dataset built to foster the emergence and evaluation of new algorithms, and, at the same time, enable the study of news coverage about the COVID-19 pandemic. It consists of a number of curated topics related to the Covid-19 outbreak, with associated news articles from portuguese and english news outlets and their respective reference timelines as gold-standard. The following figure shows the format and the structure  of the dataset.

![Dataset structure](img/tls-covid19-structure.jpg?raw=true "Dataset structure")

## Why

The rise of social media and the explosion of digital news in the web sphere have created new challenges to extract knowledge and make sense of published information. Automated timeline generation appears in this context as a promising answer to help users dealing with this information overload problem. Formally, Timeline Summarization (TLS) can be defined as a subtask of Multi-Document Summarization (MDS) conceived to highlight the most important information during the development of a story over time by summarizing long-lasting events in a timely ordered fashion. As opposed to traditional MDS, however, TLS has a limited number of publicly available datasets. This lack of datasets is even more noticeable for low resource languages, including Portuguese, which despite being the sixth most spoken language in the world [Ethnologue (2019, 22nd edition)] lacks a specific TLS dataset.

Following the worldwide coverage of the coronavirus pandemic, we propose the TLS-Covid19 dataset, a novel corpus for the Portuguese and English languages. 

## How

To create this dataset, we take advantage of liveblogs, a webpage where news media outlets offer a daily live coverage about an ongoing event. Each liveblog (usually with a different URL) consists of a set of news stories and a set of key moments. The key moments stories are manually selected by journalists from the whole set of news articles, thus giving rise to the ground-truth timeline.

## Data Sources

We consider two Portuguese news sources, [*Público*](https://www.publico.pt/) and [*Observador*](https://observador.pt/), and two English news sources, [*CNN*](https://edition.cnn.com/) and [*The Guardian*](https://www.theguardian.com/).

As a rule-of-thumb, we consider the beginning of the liveblog coverage as the start time-period. For instance, *Público* liveblog is tracked since March 16, 2020; *Observador* since January 30, 2020; *CNN* since January 22, 2020; and *The Guardian* since January 24, 2020. Our aim is to continue expanding the dataset with further articles and possibly new topics until the end of the outbreak and/or the end of the liveblogs’ coverage. We anticipate that as the pandemic evolves, the amount of data collected will grow significantly.   

The source code to reproduce the dataset is available in a Google Colab notebook. Try it here: [<img src="https://colab.research.google.com/assets/colab-badge.svg" align="center">](https://colab.research.google.com/drive/1--oHb0ia5kaKjAZl0sr1mqAEleOwB8G8?usp=sharing)

## Statistics

As of **December 31, 2020**

The following tables describe detailed statistics about the dataset. As of the date of December 31, 2020, we have collected 143 common topics for *Publico* and *Observador*, and 35 common topics for *CNN* and *The Guardian*.

By news source:

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
    <td>Sources</td>
    <td>#Topics</td>
    <td>Lang</td>
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
    <td>Público</td>
    <td>143</td>
    <td>PT</td>
    <td>28,327</td>
    <td>1092.15</td>
    <td>99.93</td>
    <td>10.93</td>
    <td>62.82</td>
    <td>40.05</td>
    <td>1.57</td>
    <td>5.75</td>
    <td>40.08</td>
  </tr>
  <tr>
    <td>Observador</td>
    <td>143</td>
    <td>PT</td>
    <td>40,181</td>
    <td>1652.22</td>
    <td>120.52</td>
    <td>13.72</td>
    <td>114.90</td>
    <td>57.77</td>
    <td>1.99</td>
    <td>6.95</td>
    <td>47.93</td>
  </tr>
  <tr>
    <td>CNN</td>
    <td>35</td>
    <td>EN</td>
    <td>26,043</td>
    <td>6178.54</td>
    <td>189.71</td>
    <td>32.57</td>
    <td>30.11</td>
    <td>20.97</td>
    <td>1.44</td>
    <td>0.49</td>
    <td>11.05</td>
  </tr>
  <tr>
    <td>Guardian</td>
    <td>35</td>
    <td>EN</td>
    <td>5,848</td>
    <td>1118.86</td>
    <td>80.69</td>
    <td>13.87</td>
    <td>25.26</td>
    <td>21.97</td>
    <td>1.15</td>
    <td>2.26</td>
    <td>27.23</td>
  </tr>
</tbody>
</table>

By news source language:

<table>
<thead>
  <tr>
    <th colspan="2"></th>
    <th colspan="4">Input Docs</th>
    <th colspan="3">Ground-Truth</th>
    <th colspan="2">Compression</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Lang</td>
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
    <td>143</td>
    <td>68,508</td>
    <td>1372.69</td>
    <td>110.23</td>
    <td>12.45</td>
    <td>88.86</td>
    <td>48.91</td>
    <td>1.82</td>
    <td>6.47</td>
    <td>44.37</td>
  </tr>
  <tr>
    <td>EN</td>
    <td>35</td>
    <td>31,891</td>
    <td>3648.70</td>
    <td>135.20</td>
    <td>26.99</td>
    <td>27.69</td>
    <td>21.47</td>
    <td>1.29</td>
    <td>0.76</td>
    <td>15.89</td>
  </tr>
</tbody>
</table>

Distribution of topics by type:

| Type  |   PT   |   EN   |
| :---: | :----: | :----: |
|  PER  |   17   |    3   |
|  ORG  |   33   |    6   |
|  LOC  |   82  |    25  |
|  KW   |   11   |    1   |

WordClouds EN/PT:

![Word Clouds](img/wc_en-pt_merged.png?raw=true "English and portuguese word clouds")

## Use Cases

The TLS-Covid19 allows one to see the evolution of a topic over time and to compare what is being said about a certain topic by different news outlets. 

One can also look at keywords, part-of-speech tags, entities or events to see how things have changed over time.

As is common with most of the datasets of this kind, one can also look at collocates. A few examples might be: keywords that were common in the same time-period, words that appear near covid-19 in different time-periods, entites, events, nouns or verbs that were more common at the beginning of the pandemics than in December 2020.

Finally, one can also create a sub-set of the dataset based on the publication date, the source, the country, etc.

## Publication

Pasquali, A., Campos, R., Ribeiro, A., Santana, B., Jorge, A., and Jatowt, A. (2021). TLS-Covid19: A New Annotated Corpus for Timeline Summarization. In: Hiemstra D., Moens M-F., Mothe J., Perego R., Potthast M., Sebastiani F. (eds), Advances in Information Retrieval. ECIR'21 (Lucca, Italy. March 28 - April 1). Lecture Notes in Computer Science, vol ..., pp. x - x. Springer. To Appear

## Contact

For further information related to the *TLS-Covid19* dataset please contact Alexandre Ribeiro (alexandre.m.ribeiro@inesctec.pt), Arian Pasquali (arian.r.pasquali@inesctec.pt), or Ricardo Campos (ricardo.campos@ipt.pt).
