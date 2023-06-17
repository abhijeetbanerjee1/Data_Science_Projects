
Python 3.9.13

### Libraries
* numpy - For mathematical calculations
* pandas - For data frame manipulation
* string - For string manipulation
* seaborn & matplotlib - For data visualization
* ipywidgets - For interactive analysis

## Problem Statement 
Tabulate all drugs that a Pharmaceutical Startup Company has sold and account for the effectiveness of each drug. The dataset contains information such as the Name of the Drug, Customer Reviews, Popularity, and Use case of the drug.

### Task of this Project
* Provide a sophisticated and useful model using NLP or ML techniques. 
* Find the most useful drug for each condition.
Find some of the hidden trends and patterns that could help the company to make precise data-driven decisions.

### Summarizing the Dataset
* To summarize the dataset, the describe() has been used on the columns containing numeric values which are the "rating" and "usefulCount" columns of the dataset.
* Then the Useful and Useless Drugs are analyzed, in this context, useful drugs comprise drugs with greater than or equal to 1000 Useful Count and useless drugs are drugs with No i.e. 0 Useful Count. 
* Now, summarizing the categorial data present in the dataset.
* Using the describe() on the categorial columns i.e. "drugName", "condition" and "review".
* Then checking for missing values shows that the "condition" column has a lot of missing values. As the condition is a piece of very important information regarding the use case of the Drugs present in the dataset we remove all records where the condition is missing.

### Unveiling Hidden Patterns from the Data
* Using the distplot() to check the distribution of Ratings and Useful Counts.
* Using the barplot() with a 'hot' palette to check the impact of Rating on Usefulness
* Checking if there is any direct correlation between the length of the reviews and ratings by using the groupby() and agg().

### Cleaning the reviews
* Removing Punctuations using string.punctuation
* Removing Stop Words using stopwords from nltk.corpus
* Removing Numbers using regular expression

### Analysing the Sentiments of the Reviews
* Using the NLTK library's Vader sentiment analysis tool to calculate the sentiment scores for each review in the 'review' column.
* The sentiment scores are then stored in a new column called 'sentiment'.
* Checking the Impact of Sentiments on Reviews by calculating the minimum, mean, and maximum values of the 'sentiment' column grouped by the 'rating' column in the DataFrame 'data', using the groupby() function in combination with the agg() function.

### Calculate Effective Rating
* Calculating an effective rating based on the original 'rating' column.
* First, calculate the minimum and maximum values from the 'rating' column in the DataFrame 'data' using the min() and max() functions, respectively. These values will be used to scale the ratings.
* Second, the function scale_rating() takes a 'rating' as input and scales it between 0 and 5. The scaled rating is then rounded to the nearest integer using round(). If the rounded rating is 0, 1, or 2, it is mapped to an effective score of 0; otherwise, it is mapped to an effective score of 1.

### Calculating Usefulness Scores
* Calculating the usefulness score for each drug in the DataFrame 'data' based on the 'rating', 'usefulCount', and 'effec_score' columns.
* This id done by multipling the 'rating', 'usefulCount', and 'eff_score' columns element-wise.

### Analyzing the Medical Condition
* By providing an interactive widget displaying the number of useless and useful drugs for the selected condition.
* Then, a bar plot is used to visualize the effective number of drugs for few of the popular conditions.
* There are 884 unique medical conditions present in the dataset.
* Finding the most common conditions.
* Findings drugs with the highest useful count.

### Finding Most Useful and Useless Drugs for each Condition
* An interactive dropdown menu is displayed, allowing you to select a condition. 
* After selecting a condition, the code will print the 5 drugs with the highest rating and the 5 drugs with the lowest rating for that condition, based on the 'usefulness' column.