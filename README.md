# Tweets Sentiment Analysis on Abortion Rights


## Introduction

Abortion has been one of the most contentious issues in the last 50 years. The Roe v. Wade decision by the United States Supreme Court in 1973 was a landmark that granted all women the right to a safe and legal abortion. According to the Supreme Court, a woman's constitutional right to privacy includes her decision on whether or not to continue her pregnancy. The Court defined this right as "fundamental" to a woman's "life and future," and held that the state could not interfere with abortion decisions unless there was a compelling reason.
In the first half of 2022, 43 abortion restrictions were enacted in 12 states. On June 24, 2022, the United States Supreme Court overturned the landmark Roe v. Wade decision from 1973, which recognized women's constitutional right to abortion. The ruling restored states' ability to prohibit abortion. Twenty-six states are either certain or likely to prohibit abortion. Following the Supreme Court's historic decision in June to overturn Roe v. Wade, abortion is now illegal or severely restricted in at least 12 states nationwide. At least ten other states have laws in place that pave the way for abortion to be quickly banned or severely restricted.
Abortion rights are a hot topic in the United States right now. Countless media posts in support or opposition to abortion rights are circulating on social media. We'd like to take a journey through all of the tweets this year that included the hashtag #AbortionRights. The data will be collected and cleaned using the Twitter API. Then we'll dig into the data and assess the sentiment of all the tweets. Finally, an unsupervised clustering model will be used to delve deep into this dataset and uncover hidden correlations between posts. This would give us a wealth of information about what people think about the subject, who supports or opposes abortion rights, and so on.

## Related Work

There are data analysis projects that have been completed on analyzing tweets labeled #AbortionRights. However, this project was done on only 5000 tweets, which is a relatively small dataset. And the main result of that project was analyzing their political backgrounds. In our project, we will anticipate collecting all the tweets data related to #AbortionRights within 2022. With more data, we expect to train an unsupervised clustering model to find underlying patterns in these tweets.
There were qualitative analyses done on investigating the disclosure of abortion experience on twitter with tweets labelled #YouKnowMe and # YouKnowUs . Though the tweets shared were highly positive , some tweets are addressed the long-standing stigma associated with abortion. The campaign helped the people to open up about their experience which has the ability to reduce stigma, refute myths and stereotypes about abortion and its aftermath, and encourage more favorable public attitude. Abortion experience research, as well as public attitudes of abortion, is critical for improving reproductive justice and women's health care.  
Future work could also look at whether abortion disclosure protects against the negative long-term effects of stigma internalization or even promotes mental or physical health. Abortion limitations (or threats of such restrictions) in the discloser's geographic location or among social groupings (e.g., a religious denomination) may have an impact on these findings. Additional data can also help  us to understand whether social media disclosures diminish stigma for those who reveal their experiences or for those who read about others' experiences.

## Proposed work

We propose to perform a deep exploration on tweets with #AbortionRights posted this year, including statistical analysis and unsupervised machine learning. 
We will first collect all the tweets through the Twitter API. The collected data will be cleaned in several steps. All the urls will be deleted, emoji and special characters will be dealt with. After we obtain the cleaned dataset, we will analyze the statistics of the dataset. The number of tweets vs. time might show a strong correlation with the change in legislation about abortion. The analysis of word frequency might help us understand what the main themes are in these tweets. 
After doing a simple exploratory of the statistics of the dataset, we plan to apply an unsupervised sentiment analysis by using pre-trained model VADER in the NLTK package. We will obtain the labels of tweets, i.e., positive, negative, neutral. 
To go beyond this, we will also train an unsupervised clustering model on this corpus. The texts will be processed in the following steps: tokenization, feature extraction (vectorization), and clustering. Feature extraction can be done in many different ways. We propose using the word2vec model to train a word embedding. And then use the word embeddings as input for the k-mean clustering model to get information.  After applying the clustering model, we would get a meaningful understanding of the data that we are dealing with. Different subgroups can be analyzed individually based on their sentiments.

## Evaluation

Evaluating the performance of a clustering algorithm is not as trivial as counting the number of errors or the precision and recall of a supervised classification algorithm. Since ground truth labels of the tweets are unknown, evaluation must be performed using the model itself. We will use the Silhouette Coefficient to evaluate the clustering model. It is defined as the following: 
s=b-amax(a, b)
where a is the mean distance between a sample and all other points in the same class, and b is the mean distance between a sample and all other points in the next nearest cluster.

## Result:

After finetuning the scrapped twwets on distillbert pretrained model we got around 60% of tweets as of positive sentiment which means that people are in favour of abortion ban which is counter intutive. Around 23% of tweets are of negative sentiment and around 17% of tweets are neutral in nature.

