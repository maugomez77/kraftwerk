# Application 17.1: Bank Marketing Campaigns

## Data Understanding

This data was originated from around 17 real-world marketing campaigns from a Portuguese bank with the purpose of promoting bank deposit subscriptions. 

These campaigns between May 2018 till November 2010 involved interactions from around 79,354 contacts. 

The dataset, which was already cleaned at its source, is primarily focused on phone based marketing campaigns.

Key observations on the dataset:

- The dataset does not have missing values.

## Business Objective

### Background

The overall business is to augment the efficiency of these campaigns for long-term deposit subscriptions by minimizing the required contacts.

### Goal 

The primary goal is to identify a model that can be able to explain the success of a contact engagement: whether the client would be able to subscribe to the deposit or not. 

A successful model can potentially enhance this efficiency campaign by identifying pivotal characteristics influencing successful factors, there for a better managing of the resources and selecting a high-quality, cost-effective potential customer base.

This is accomplished by doing a benchmarking / comparison between k-nearest neighbors, logistic regression, decision trees, and support vector machines models.

## Business Impact

The outcome of this project will influence the bank marketing strategies, leading to the following potential benefits:

1. **Cost efficiency**: Predicting the customers who are most likely to subscribe to a term deposit will allow the bank to target these individuals specifically, thus reducing the costs associated with broad spectrum marketing.
2. **Increased conversion rate**: By focusing the marketing efforts on the clients that are predicted to subscribe, the bank can increase the effectiveness of the marketing campaign, resulting in higher conversion rates.
3. **Customer satisfaction**: Properly directed marketing efforts will reduce the number of unwanted contacts for customers that are not interested in the product, leading to higher customer satisfaction.

## Approach being taken

The project will follow the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology.

The objective is to select the best model that gives the highest accuracy while also considering the interpretability of the model, as well as  understanding the factors that influence the client's decision to provide additional insights for the business

Data Understanding, Data Preparation, Modeling and Evaluation is attached in the following notebook:

- [python notebook](prompt_III_mauricio.ipynb) 

Dataset and Data Dictionary are available:

- /data/bank-additional-full.csv
- /data/bank-additional-names.txt
- /data/bank-additional.csv (subset of the full dataset)

Attaching the article accompanying the dataset [here](CRISP-DM-BANK.pdf) for information related to the description data and features.

## Conclusions

Due to the unbalanced dataset labels, the model performance is limited. 
To address this issue, I have chosen the F1 score as the primary performance metric and used AUC to compare the different models and be able to make a final decision.

All the different models outperformed the baseline, indicating positive outcomes.

The Decision Tree Classifier emerges as the best model for customer classification, offering potential to classify on both labels.

The data derived from marketing campaigns appears to lack relevance. Most of the features are not predictive of the outcome. The selected model relying only on the following features:
  - emp.var.rate
  - cons.conf.idx
  - duration
  - nr.employed
  - pdays
  - month
  - age

Despite the efforts, the model would be limited as a practical tool for customer classification.

## Next Steps

In order to improve our the current models, I think more data gathering related to the customers , such as income and bank profile would be ideal in order to reduce the number of unknown values.

Also another suggestion would be to use SMOTE (Synthetic Minority Oversampling Technique) in order to address the class imbalance, this to potentially improve the model accuracy, also as a side effect, noise would be added as well.