# Amazon Sales Data Analysis


## 🎥 Link to Data Analysis (Includes all Cleaning/Analysis/Visualizations/Conclusion):
[Amazon Sales Data Analysis](https://github.com/ManasaMaddi05/Amazon-Sales-Data-Analysis/blob/main/jupyter.ipynb)

## Project Overview
This project focuses on an in-depth analysis of Amazon product review data using Python, with the aim of uncovering valuable insights into customer behavior, product performance, and review patterns. The dataset contains over 568,000 reviews and includes attributes like product IDs, user IDs, helpfulness scores, review text, and ratings. By cleaning the data, removing duplicates, and applying both statistical and visual analyses, we aim to identify the most frequently purchased products, customer sentiment trends, and patterns in review ratings.

This project leverages Python's pandas, numpy, seaborn, matplotlib, and sqlite3 libraries for data manipulation, analysis, and visualization. Additionally, the TextBlob library was used for sentiment analysis of the reviews.

## Table of Contents

Installation
Dataset
Project Workflow
1. Data Loading and Cleaning
2. Handling Invalid Entries and Duplicates
3. Exploratory Data Analysis (EDA)
4. Frequent and Non-Frequent Buyers Analysis
5. Sentiment Analysis
Key Insights
Conclusion
Future Work
Installation
To run this project on your local machine, follow these steps:

Clone the repository:

bash
Copy code
git clone https://github.com/YourUsername/Amazon-Sales-Data-Analysis.git
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Ensure you have Python 3.x installed along with the following packages:

pandas
numpy
seaborn
matplotlib
sqlite3
TextBlob
Set up the SQLite database file in the correct directory.

Run the Jupyter Notebook to explore the analysis and visualizations.

## Dataset
The dataset used in this project consists of Amazon product reviews, containing the following columns:

Id: Unique identifier for each review.
ProductId: The ID of the product being reviewed.
UserId: The ID of the user who left the review.
ProfileName: The profile name of the reviewer.
HelpfulnessNumerator: The number of users who found the review helpful.
HelpfulnessDenominator: The total number of users who voted on the helpfulness of the review.
Score: The rating provided by the user (on a scale of 1 to 5).
Time: The time when the review was posted (as a Unix timestamp).
Summary: A brief summary of the review.
Text: The detailed review text.
Project Workflow

## 1. Data Loading and Cleaning
The dataset was loaded from an SQLite database using the sqlite3 library.
Initial data exploration showed 568,454 reviews.
Cleaned invalid entries where the helpfulness numerator was greater than the denominator.
Duplicates were identified by checking if the same user left the same review at the same time, which were subsequently removed for unbiased results.

## 2. Handling Invalid Entries and Duplicates
Rows with mismatched helpfulness scores were removed.
Duplicates in the reviews were eliminated based on user ID, profile name, and review text.

## 3. Exploratory Data Analysis (EDA)
Key tasks in this stage:
Grouped users by review behavior, identifying frequent and non-frequent buyers.
Plotted the top 10 users in terms of products purchased and reviews left.
Identified and visualized the most frequently reviewed products.
Counted the frequency of each product being reviewed, and selected those with over 500 reviews for further analysis.

## 4. Frequent and Non-Frequent Buyers Analysis
Classified users into two categories: "Frequent Buyers" and "Non-Frequent Buyers" based on the number of products purchased.
Analyzed the distribution of ratings among these two categories.
Frequent buyers generally provided higher ratings than non-frequent buyers.

## 5. Sentiment Analysis
Performed sentiment analysis using the TextBlob library.
Extracted polarity values for each review summary to understand the sentiment behind each review.
Identified common words used in positive and negative reviews using Python’s collections.Counter.
Visualized the most common words in both positive and negative reviews.

### Key Insights

## Frequent Buyers Behavior:
Frequent buyers tend to leave more positive feedback, with over 60% of their ratings being 5 stars.

## Sentiment Analysis:
Positive reviews were dominated by terms like "Delicious", "Great", and "Excellent", while negative reviews often contained terms like "Disappointed", "Poor", and "Horrible".

## Product Review Trends:
Most products had over 500 reviews, indicating high engagement and reliability of feedback for popular items.

## Conclusion
This analysis highlights key patterns in customer behavior and product performance, providing actionable insights for Amazon sellers and product managers. Frequent buyers, in particular, have a tendency to leave positive reviews, which can help sellers understand their most loyal customers and further target marketing efforts. The sentiment analysis also provides valuable insights into customer preferences, enabling more tailored product recommendations.
