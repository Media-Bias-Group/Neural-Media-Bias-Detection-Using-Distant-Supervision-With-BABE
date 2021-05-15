# Neural-Media-Bias-Detection-Using-Distant-Supervision-With-BABE
The repository contains the data files and scripts corresponding to the paper "Neural Media Bias Detection Using Distant Supervision With BABE".

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

# Description of scripts
- "data_set_evaluation.ipynb": script containing relevant code and results for the evaluation of the data sets (agreement calculations, label distribution...).

# Other files
- "topics_keywords_platforms.txt": a file containing all news topics, keywords to retrieve relevant news articles, and news platforms for the data set creation.


