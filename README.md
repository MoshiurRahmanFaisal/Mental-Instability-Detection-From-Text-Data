# Mental Instability Detection From Text Data

The project proposes Machine Learning, Deep Learning, Transformer Based Learning models, and Explainable Artificial Intelligence approaches to evaluate mental health problems from social media texts. Among the machine learning models, XGBoost has the highest accuracy for the English language dataset, 71.94%. The fusion of CNN+BiLSTM has an accuracy of 70.26%, which is the highest among the deep learning models. 80.53% is the best accuracy in transformer-based learning models achieved from the BERT Base model in the English Language. XGBoost and Logistic Regression have the highest accuracy of 56.75% for the Bangla language dataset. For Bangla, CNN+BiLSTM with an accuracy of 63.39% and XLM-RoBERTa with 76.68% are the best models trained from the deep learning and transformer-based learning models. The Cohen’s Cappa scores for English and Bangla datasets are 91% and 89%, respectively.


## Dataset

Data is collected from user posts on Reddit using web scraping. There are support groups on Reddit with people wanting to know about and suffering from mental health issues, and experts in those groups give them consultancy. These groups are known as "subreddits." We collected data from each subreddits for every mental state we worked on. There are subreddits specialized in mental health issues such as Bipolar, Schizophrenia, Addiction, Alcoholism, Asperger’s, Neutral, Suicidal Thought, Anxiety, Depression, and Self Harm. All these mental health issues. Web scraping techniques are used in this process. We used Reddit's API to scrape data from Reddit. Using scraping, we scraped 12000 English data from Reddit.

| **Class Name** | **English Data** | **Bengali Data**
| :-------- | :------- | :------- 
| Anxiety | 1024 | 991
| Bipolar | 1024 | 1000
| Borderline Personality | 1024 | 995
| Depression | 1024 | 943
| Schizophrenia | 1024 | 988
| Suicidal Thought | 1024 | 1001
| Alcoholism | 999 | 986
| Addiction | 998 | 921
| Asperger’s | 799 | 789
| Self Harm | 746 | 671
| Neutral | 1024 | 1002


## Embedding

- Word embedding methods like `TF-IDF`, `Word2Vec`, `GloVe` and `fastText` was used 
- Context embedding methods like `BERT` and `RoBERTa` was used. 


## Model Accuracy

From the dataset 80% data was used for training and 20% for testing.


| **Model** | **Embedding** | **Accuracy (English)** | **Accuracy (Bangla)**
| :-------- | :------- | :-------- | :------- 
| Naïve Bayes | TF-IDF | 60.83% | 52.13%
| SVM | TF-IDF | 65.63% | 52.62%
| XGBoost | TF-IDF | 71.94% | 56.75%
| AdaBoost | TF-IDF | 63.35% | 49.90%
| Decision Tree | TF-IDF | 53.68% | 41.25%
| Random Forest | TF-IDF | 66.57% | 51.16%
| Stochastic Gradient Descent | TF-IDF | 64.65% | 52.52%
| Logistic Regression | TF-IDF | 68.62% | 56.75%
| CNN | Word2Vec | 64.29% | 52.13%
| BiLSTM | Word2Vec | 64.52% | 54.89%
| CNN+BiLSTM | Word2Vec | 67.27% | 63.39%
| CNN+BiLSTM | GloVe | 70.26% | 50.80%
| CNN+BiLSTM | fastText | 63.77% | 54.45%
| BERT Base | BERT | 80.35% | -
| Bangla BERT | BERT | - | 72.55%
| Multilingual BERT | BERT | 78.90% | 75.36%
| XLM-RoBERTa | RoBERTa | 80.53% | 76.68%


## Explainable AI

#### Text explainer from `LIME` was used to explain model's output. 



