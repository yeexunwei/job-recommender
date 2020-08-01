# job-recommender
A  Job Recommendation Engine with Implicit Feedback. Two models are developed. The first used content -basaed filtering; the second implemented [Collaborative Filtering for Implicit Feedback](http://yifanhu.net/PUB/cf.pdf).

## Project Intro
Develop a model to recommended jobs to users on a job portal. The dataset contains only implicit feedback thus algorithm that requires explicit feedback such as rating and user reviews are not applicable.

### Methods Used
* Language Prediction
* Natural Language Processing
* RNN, LSTM

### Technologies
* Python
* Python pandas, seaborn, regex
* Python scikit-learn

## Project Description
1. `job_recommender.ipynb` - TfidfVectorizer transforms text to feature vectors that can be used as input to estimator. Content-based filtering - job description based recommender (recommend jobs based on highest cosine similarity), similar user based recommender (recommend jobs of similar users).
2. `job_als.ipynb` - Alternating Least Square (ALS) algorithm is chosen since the dataset only contains implicit feedback. Python Implicit library made implementing the complex algorithm simpler and faster. ALS measures the confidence whether a user will apply for a job based on a constructed Matrix. The Matric factorises jobs and users into features. ALS algorithm keeps on refining the values based on training set.

Data source from [Kaggle CareerBuilder](https://www.kaggle.com/c/job-recommendation).

## Process Flow
- data processing/cleaning
- text processing
- words tokenizing
- model training

## Reference
[ALS Implicit Collaborative Filtering](https://medium.com/radon-dev/als-implicit-collaborative-filtering-5ed653ba39fe)  
[A Gentle Introduction to Recommender Systems with Implicit Feedback](https://jessesw.com/Rec-System/)  
[Finding Similar Music using Matrix Factorization](http://www.benfrederickson.com/matrix-factorization/)

## Future Improvement
Inlcude [evaluation](https://gist.github.com/jbochi/2e8ddcc5939e70e5368326aa034a144e#file-evaluation-ipynb).
