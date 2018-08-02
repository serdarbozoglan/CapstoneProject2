
## MBTI PERSONALITY TYPE PREDICTION

## The Problem
The purpose of the Myers-Briggs Type Indicator® (MBTI®) personality inventory is to make the theory of psychological types described by C. G. Jung understandable and useful in people's lives. The essence of the theory is that much seemingly random variation in the behavior is actually quite orderly and consistent, being due to basic differences in the ways individuals prefer to use their perception and judgment.

According to The Myers Briggs Type Indicator (or MBTI for short) is a personality type system that divides everyone into 16 distinct personality types across 4 axes:

`Introversion (I) – Extroversion (E)`

`Intuition (N) – Sensing (S)`

`Thinking (T) – Feeling (F)`

`Judging (J) – Perceiving (P)`

We have 16 different combination of personality types in our data set. In summary this is a personality classification prediction study based on MBTI test results. 
Who Might Care :
It is one of, if not the, the most popular personality test in the world. It is used in businesses, online, for fun, for research and lots more. It’s safe to say that this test is still very relevant in the world in terms of its use. The test is commonly used in many different business-oriented settings, including:

`Leadership development`

`Team building`

`Screening and interviewing employees`

`Career selection`

`Personal development`

In this context, companies, institution, organizations, and even people may care about it.  

## Data Set :
a.	The data has been obtained from the "Kaggle" (https://www.kaggle.com/datasnaek/mbti-type) and Kaggle states that the data has been obtained through ‘PersonalityCafe forum’ (https://www.personalitycafe.com/forum/)

b.	We have 8675 observations in our data set. Each data observation contains a post which is written by a person and his/her personality type stated in another column.

c.	We will preprocess the post before implementation of ML algorithms. In this context:

`We will lowercase the posts`

`We will remove the links from posts`

`We will expand the contractions such as I’m to I am`

`We will remove whitespace and eliminate all other things but words`

`We will remove punctuations, stopwords such as the, or, and, my etc`

`Finally, we will use stemmer to get the root of the words`

d.	Our target column is personality type which has 16 different class.

e.	We created new column which is called __[‘clean_text’]__ holding processed texts which are described above. This column contains MBTI personality types such as ‘ENFJ, INTP or ENTP’. Those words were not removed on purpose.

f.	 We have created another column __[‘clean_text_without_mbti’]__. This column is exactly same with [‘clean_text’] column but MBTI words.

## Machine Learning Aspect
1.	We have used Logistic Regression, Linear SVM and XGB ML algorithms.
2.	We followed two different approach to predict the personality type of people from their posts.
1.	In the original Kaggle data set, some peoples' names are replaced with their MBTI profiles in their post. For example, "...Who wants their most reliable asset gone for that long? ENTJ employer..."  is from one of the posts in the data set. The person name is replaced by ENTJ due to his/her MBTI test result is already known as ENTJ. This helps to classify the personality type. In this context we have used __[‘clean_text’]__ column as a data set.
2.	Later, we have removed MBTI profile labels from the posts. In this context, we have used __[‘clean_text_without_mbti’]__ column as our data set. 
 	Our aim is to evaluate how MBTI labels affect our predictions. What if we remove those labels in terms 	of accuracy of models.
3.	At the beginning we will try to predict all types of personalities at the same time. Due to 16 different classes we expect relatively low accuracy. Then we will predict controversial personality types with each other such as Introversion vs Extroversion, Thinking vs Feeling, Intuition vs Sensing and Judging vs Perceiving.

4.	We will use __80% of data as train set__ and rest for test set.

5.	We will implement gridsearch technique and pipeline workflow in this study.
