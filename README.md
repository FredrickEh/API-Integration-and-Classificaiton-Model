# API-Integration-and-Classificaiton-Model
This project harnesses the Yelp API and web scraping to collect reviews, balances data via oversampling, and uses a decision tree for sentiment analysis. It adeptly classifies reviews into positive or negative sentiments, showcasing a blend of data extraction, preprocessing, and machine learning.
This project encompasses a comprehensive approach to sentiment analysis by leveraging the Yelp API, web scraping techniques, data preprocessing, and machine learning modeling. Here's a detailed breakdown of each step:

Connecting to the Yelp API: The initial stage involves connecting to the Yelp API to retrieve business information. This connection is crucial for accessing structured data about various businesses, such as their names, locations, and URLs to their Yelp review pages.

Web Scraping Reviews: Once we have the URLs from the Yelp API, the next step is to perform web scraping. This process involves making HTTP requests to each URL and parsing the HTML content to extract review text and ratings. We use BeautifulSoup, a Python library, to navigate through the HTML structure of the Yelp review pages and systematically extract the relevant data, typically limiting ourselves to a certain number of reviews per business due to display constraints on the web pages.

Balancing the Rating Data: An inherent challenge in sentiment analysis is dealing with imbalanced datasets, where one sentiment class (e.g., positive) might be overrepresented compared to another (e.g., negative). To address this, we use the "imblearn" library to either oversample the minority class or undersample the majority class. For this project, we chose oversampling, which enhances the dataset by replicating instances of the underrepresented class, thus providing a more balanced and richer dataset for training our model.

Sentiment Assignment: We then assign a sentiment label to each review. This is done by converting the numerical ratings into categorical sentiment labels—reviews with ratings of 4 or higher are labeled as 'positive', while those with ratings of 3 or lower are labeled as 'negative'. This binary classification aligns with typical sentiment analysis objectives, simplifying the model's task.

Building a Classification Model: The core of this project is the development of a machine learning model for sentiment classification. We employ a decision tree classifier, a fundamental yet powerful algorithm in machine learning. Decision trees are particularly suited for this task due to their ability to handle varied feature types and their interpretability. They work by learning decision rules inferred from the data features.

Text Analysis Processes: Alongside the numerical analysis of ratings, we also perform text analysis on the review content. This involves extracting features from the text data, such as word frequencies or presence of specific keywords or phrases, which are then fed into the decision tree classifier. The combination of text analysis with the sentiment labels allows the model to learn how different textual patterns correlate with positive or negative sentiments.

Model Evaluation and Refinement: Once the model is built, we evaluate its performance using standard metrics like accuracy, precision, recall, and the confusion matrix. Based on these evaluations, we refine the model through techniques like hyperparameter tuning or feature selection to enhance its predictive accuracy.

Final Output: The end goal of this project is to create a robust model capable of accurately classifying Yelp reviews into positive or negative sentiments. This model can be utilized for various purposes, such as understanding customer satisfaction, gauging public opinion on certain services or establishments, or even guiding business strategy.

Each step in this project contributes to the overarching goal of developing a reliable sentiment analysis tool using data from Yelp, showcasing the interplay between API data retrieval, web scraping, data preprocessing, and machine learning.
