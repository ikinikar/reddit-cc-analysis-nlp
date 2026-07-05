# Reddit Climate Change Discourse Analysis

An NLP exploration of how people talk about climate change on Reddit, using a public dataset of Reddit posts on the topic.

## Questions explored

1. Is climate change a polarizing topic on Reddit?
2. Are people generally optimistic about our chances of fighting or adapting to climate change?
3. What topics do people commonly connect to climate change?
4. Are post scores correlated with topic or sentiment?
5. How much variation exists within Reddit discourse on the subject?

## Approach

- **Preprocessing**: cleaned and deduplicated posts, then used NLTK for tokenization, stop word removal, and lemmatization.
- **Sentiment analysis**: used NLTK's VADER (Sentiment Intensity Analyzer) to label posts as positive, negative, or neutral.
- **Topic modeling**: used Latent Dirichlet Allocation (LDA) via gensim to surface the main topics in the dataset.
- **Statistical testing**: used the Kruskal-Wallis test to check whether post scores differ significantly across sentiment and topic groups, followed by Dunn's post-hoc test with Bonferroni correction to find where those differences lie.
- **Clustering**: used hierarchical clustering to look at overall variation in discourse across sentiment, topic, and post score.

## Data

[Public Opinion on Climate Change](https://www.kaggle.com/datasets/asaniczka/public-opinion-on-climate-change-updated-daily), a Reddit posts dataset available on Kaggle. The dataset isn't included in this repo; download it from Kaggle if you want to run the notebook yourself.

## Tech

Python, pandas, NLTK, gensim, scikit-learn, scipy, scikit-posthocs, seaborn, matplotlib. Written and run in Google Colab.
