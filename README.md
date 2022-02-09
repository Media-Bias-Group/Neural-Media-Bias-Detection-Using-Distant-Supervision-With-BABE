# Neural Media Bias Detection Using Distant Supervision With BABE - Bias Annotations By Experts
The repository contains the data files and scripts corresponding to the paper "Neural Media Bias Detection Using Distant Supervision With BABE". 

The models are uploaded on https://zenodo.org/record/5861846#.YeUoolkxkvE because of the GitHub file size restrictions. 

# Description of the data files found in /data folder" (all files are also provided in csv format)
- "raw_labels_MBIC.xlsx": individual annotator labels of MBIC's crowdsourcers.  
- "raw_labels_SG1.xlsx": individual annotator labels of SG1 (8 expert annotators).
- "raw_labels_SG2.xlsx": individual annotator labels of SG2 (5 expert annotators).
- "final_labels_MBIC.xlsx": MBIC's aggregated labels over all annotators based on majority vote (1700 sentences).
- "final_labels_SG1.xlsx": SG1's aggregated labels over all annotators based on majority vote (same 1700 sentences as in MBIC).
- "final_labels_SG2.xlsx": SG2's aggregated labels over all annotators based on majority vote (3700 sentences).
- "silver-standart-dataset.xlsx": Silver standard dataset containing 1000 additional unlabeled sentences with potential biased text instances.

Columns:
- "text": sentences extracted from news articles and labeled in terms of bias and opinion.	
- "news_link": url to the news article from which the sentence is extracted.
- "outlet": news platform publishing the news article.
- "topic": news topic.
- "type": political orientation of news platform according to mediacloud.org.
- "label_bias": bias label for the sentence ("Biased" or "Non-biased").
- "label_opinion": opinion label for the sentence ("Expresses writer's opinion" or "Somewhat factual but also opinionated" or "Entirely factual".
- "biased_words": words marked as biased by the annotators.

# Additional data used for training purporses
- "bias_word_lexicon.xlsx": dictionary of biased words used to craft features
- "dt_final_SG1.xlsx": final SG1 with engineered features
- "dt_final_SG2.xlsx": final SG2 with engineered features 
- "news_headlines_usa_biased.csv": data set with distant labels of class biased
- "news_headlines_usa_neutral.csv": data set with distant labels of class neutral

# Description of scripts
- "data_set_evaluation.ipynb": script containing relevant code and results for the evaluation of the data sets (agreement calculations, label distribution...).
- "features_engineering.ipynb": engineering features for the baseline classifier
- "classification_baseline_model.ipynb": training and evaluation of the baseline classifier
- "classification.ipynb": training and evaluation of neural language models
- "distant_supervision.ipynb": pre-training on the data set with distant labels

# Other files
- "topics_keywords_platforms.txt": a file containing all news topics, keywords to retrieve relevant news articles, and news platforms for the data set creation.
- "annotator_demographics.csv": a file containing demographic information about the annotators (The corresponding demographic questionnaire can be found under "demographic_questionnaire.pdf") .

# Cite as
```
@InProceedings{Spinde2021f,
    title = "Neural Media Bias Detection Using Distant Supervision With {BABE} - Bias Annotations By Experts",
    author = "Spinde, Timo  and
      Plank, Manuel  and
      Krieger, Jan-David  and
      Ruas, Terry  and
      Gipp, Bela  and
      Aizawa, Akiko",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2021",
    month = nov,
    year = "2021",
    address = "Punta Cana, Dominican Republic",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2021.findings-emnlp.101",
    doi = "10.18653/v1/2021.findings-emnlp.101",
    pages = "1166--1177",
}

```


More about our work can be found here: https://media-bias-research.org/

