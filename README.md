# CS412 Machine Learning Course Project
***
## Project Description

The project aims to predict homework scores using various machine learning models. The approach involves extracting and preprocessing data from conversations, employing feature engineering techniques to enrich the dataset, and then applying multiple regression models to predict the scores. This multidimensional analysis ensures a thorough understanding and effective prediction of homework scores based on the given data.

The work presented is for the CS412 Machine Learning course at Sabanci University.

## Table of Contents
1. [General Info](#general-info)
2. [Methodology](#methodology)
3. [Results](#results)
4. [Team Contributions](#teamcontributions)
### General Info
***
## Methodology
***
A list of methodologies used within the project:

* Data Preparation

The data extracted from HTML files that store the ChatGPT conversations of students. The HTML files are read, parsed with BeautifulSoup and conversations are extracted based on specific patterns. The code is extracted from file path, acting as a key in the “code2convos” dictionary where results are stored. If there are errors, detailed information is recorded in the log file, aiding in debugging and analysis. Duplicated keys are removed to prevent overwriting. 

Texts in the dictionary are preprocessed by several steps, including lowercasing, removal of punctuation and special characters, stopword removal, stemming, and lemmatization. Tokenized words are then rejoined into a single string. The dictionary is updated with the preprocessed version.

Prompts written by students are matched with questions given in the assignment by the simple term frequency vectorizing method. The distances between vectors representing prompts and questions are calculated. Mapping between file codes and their cosine similarity scores for each question is done.

Since we ran multiple training models for the next parts, tokenization and vectorization of data were needed for the ones which require a numerical format as it is a common preprocessing step for natural language processing tasks. 
  
```ruby
print(snippet here)
```

* Feature Engineering (Links to Code Snippets?)

Many features were created and some with high correlations were selected for training our models. Here is the list of our features:

1. Number of prompts that a user asked
2. Number of complaints that a user makes (e.g., "the code gives this error!")
3. User prompts average number of characters
4. Total number of prompts
5. Ratio of error prompts to total prompts
6. Average entropy per prompt
7. Total characters per interaction (sum of prompt and response averages)
8. Ratio of prompt characters to response characters
9. Average Q per responses
10. Positive responses to negative responses ratio
11. Response Complexity
12. Response diversity
13. Prompts to errors ratio
14. Frequency of "thank you"
15. Average entropy of responses
16. Q_0 - Q_8 ratio to total prompts
17. Response length
18. Sentiment Analysis on Responses
19. Frequency of repeating prompts
20. Flesch-Kincaid readability score
21. Question number where the student starts consulting GPT
22. Primitive Grade (calculated based on similarity score and max point of each question)

* Select Features (Links to Code Snippets?)
  
* Different Models trainings (NN, randomForest etc.) (Links to Code Snippets?)
## Results
***
Discussion and conclusion

## Team Contributions
***
Give instructions on how to collaborate with your project.
> Maybe you want to write a quote in this part. 
> Should it encompass several lines?
> This is how you do it.


### Screenshot
<p align="center">
  <img src="Plots/image.png" alt="Ornek" width="50%">
</p>
