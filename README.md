# CapstoneProject2 

This is study is about prediction of personality type of people from their social media posts. The information below regarding personality type Following information is obtained from <https://www.myersbriggs.org/my-mbti-personality-type/mbti-basics/>  and <https://www.kaggle.com/datasnaek/mbti-type/home>

First we will describe the MBTI test and its purpose then explain what is our aim in this study. Let's start with giving information about personality type test.

The purpose of the __Myers-Briggs Type Indicator® (MBTI®)__ personality inventory is to make the theory of psychological types described by C. G. Jung understandable and useful in people's lives. The essence of the theory is that much seemingly random variation in the behavior is actually quite orderly and consistent, being due to basic differences in the ways individuals prefer to use their perception and judgment.

"Perception involves all the ways of becoming aware of things, people, happenings, or ideas. Judgment involves all the ways of coming to conclusions about what has been perceived. If people differ systematically in what they perceive and in how they reach conclusions, then it is only reasonable for them to differ correspondingly in their interests, reactions, values, motivations, and skills."

In developing the Myers-Briggs Type Indicator [instrument], the aim of Isabel Briggs Myers, and her mother, Katharine Briggs, was to make the insights of type theory accessible to individuals and groups. They addressed the two related goals in the developments and application of the MBTI instrument:

The identification of basic preferences of each of the four dichotomies specified or implicit in Jung's theory.

The identification and description of the 16 distinctive personality types that result from the interactions among the preferences."

Excerpted with permission from the MBTI® Manual: A Guide to the Development and Use of the Myers-Briggs Type Indicator®

__Favorite world:__ Do you prefer to focus on the outer world or on your own inner world? This is called `Extroversion (E)` or `Introversion (I)`.

__Information:__ Do you prefer to focus on the basic information you take in or do you prefer to interpret and add meaning? This is called `Sensing (S)` or `Intuition (N)`.

__Decisions:__ When making decisions, do you prefer to first look at logic and consistency or first look at the people and special circumstances? This is called `Thinking (T)` or `Feeling (F)`.

__Structure:__ In dealing with the outside world, do you prefer to get things decided or do you prefer to stay open to new information and options? This is called `Judging (J)` or `Perceiving (P)`.

__Your Personality Type:__ When you decide on your preference in each category, you have your own personality type, which can be expressed as a code with four letters.

__The 16 personality types of the Myers-Briggs Type Indicator® instrument__ are listed here as they are often shown in what is called a "type table." letter type code. 

__All types are equal:__ The goal of knowing about personality type is to understand and appreciate differences between people. As all types are equal, `there is no best type`.

The MBTI instrument sorts for preferences and does not measure trait, ability, or character. The MBTI tool is different from many other psychological instruments and also different from other personality tests.

The best reason to choose the MBTI instrument to discover personality type is that hundreds of studies over the past 40 years have proven the instrument to be both valid and reliable. In other words, it measures what it says it does (validity) and produces the same results when given more than once (reliability). 

The Myers Briggs Type Indicator (or MBTI for short) is a personality type system that divides everyone into 16 distinct personality types across 4 axis:

`Introversion (I) – Extroversion (E)`

`Intuition (N) – Sensing (S)`

`Thinking (T) – Feeling (F)`

`Judging (J) – Perceiving (P)`

So for example, someone who prefers `introversion`, `intuition`, `thinking` and `perceiving` would be labelled an `INTP` in the MBTI system, and there are lots of personality based components that would model or describe this person’s preferences or behaviour based on the label.

The theory of psychological type was introduced in the 1920s by Carl G. Jung. The MBTI tool was developed in the 1940s by Isabel Briggs Myers and the original research was done in the 1940s and '50s. This research is ongoing, providing users with updated and new information about psychological type and its applications. Millions of people worldwide have taken the Indicator each year since its first publication in 1962. It is one of, if not the, the most popular personality test in the world. It is used in businesses, online, for fun, for research and lots more. A simple google search reveals all of the different ways the test has been used over time. It’s safe to say that this test is still very relevant in the world in terms of its use.

From scientific or psychological perspective it is based on the work done on cognitive functions by Carl Jung i.e. Jungian Typology. This was a model of 8 distinct functions, thought processes or ways of thinking that were suggested to be present in the mind. Later this work was transformed into several different personality systems to make it more accessible, the most popular of which is of course the MBTI.

Recently, its use/validity has come into question because of unreliability in experiments surrounding it, among other reasons. But it is still clung to as being a very useful tool in a lot of areas, and the purpose of this dataset is to help see if any patterns can be detected in specific types and their style of writing, which overall explores the validity of the test in analysing, predicting or categorising behaviour.

## Data Source: 

The Kaggle states that the data was collected through the `PersonalityCafe forum`, as it provides a large selection of people and their MBTI personality type, as well as __what they have written.__

We have 8675 observations in our data set. Each observation contains a post which is written by a person and his/her personality type in another column. 

## What we will do in this study?

In this context, we will use machine learning models to predict the MBTI personality type of the people from their posts. 

In the original Kaggle data set, some peoples' names are replaced with their MBTI profiles in their post. For example "...Who wants their most reliable asset gone for that long? ENTJ employer..."  is from one of the posts in the data set. The person name is replaced by ENTJ due to his/her MBTI test result is already ENTJ. This helps to classify the personality type.

In our study, __first__ we will predict the personality types __keeping the personality type names such as INTJ or ENTJ etc in our posts__ and we will figure out how these words are important for our predictions and affect the accuracy of the models. Then we will __remove those words__ from the posts and predict the personality types. 
