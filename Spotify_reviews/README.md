# **Spotify Reviews Analysis**

## **Overview**

This project analyzes user reviews for Spotify to uncover patterns, sentiments, and insights about the platform. Using natural language processing (NLP) techniques and sentiment analysis, we explore what users love, dislike, or request as improvements in the service. The dataset contains text reviews, ratings, thumbs-up counts, and timestamps.

---

## **Table of Contents**

1. [Dataset Description](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#dataset-description)  
2. [Methodology](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#methodology)  
3. [Key Insights](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#key-insights)  
4. [Visualizations](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#visualizations)  
5. [Dependencies](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#dependencies)  
6. [Acknowledgments](https://chat.qwen.ai/c/e4492baa-3918-4c5f-b11d-365e33645835#acknowledgments)

---

## **Dataset Description**

The dataset consists of the following columns:

* Review : User-generated feedback about Spotify.  
* Rating : A numerical score (1–5) given by the user.  
* Total\_thumbsup : Number of "thumbs up" a review received from other users.  
* App\_Version : Version of the Spotify app associated with the review.  
* Timestamp : Date and time when the review was posted.

Each review is preprocessed and tokenized for further analysis.

---

## **Methodology**

### **1\. Data Preprocessing**

* Lowercasing : All text was converted to lowercase to ensure uniformity.  
* Tokenization : Reviews were split into individual tokens using nltk.word\_tokenize.  
* Stopword Removal : Common stopwords (e.g., "the," "and") were removed to focus on meaningful words.  
* TF-IDF Vectorization : Term Frequency-Inverse Document Frequency (TF-IDF) was applied to quantify word importance.

### **2\. Sentiment Analysis**

* VADER Sentiment Analysis : Valence Aware Dictionary and sEntiment Reasoner (VADER) was used to compute sentiment scores for each review. This tool is particularly effective for social media text.  
* Sentiment Categories : Reviews were classified into three categories:  
  * Positive (compound\_score \> 0)  
  * Neutral (compound\_score \== 0)  
  * Negative (compound\_score \< 0)

### **3\. Word Clouds**

* Generated word clouds for positive and negative reviews to visualize frequently mentioned terms.

### **4\. Distinguishing Words**

* Compared top words in 1-star vs. 5-star reviews to identify distinguishing factors between highly dissatisfied and satisfied users.

---

## **Key Insights**

### **1\. Reasons for Dissatisfaction (1-Star Reviews)**

* Users cited issues related to:  
  * Ads : Excessive advertisements were a major complaint.  
  * Music Quality : Poor audio streaming quality.  
  * App Performance : Bugs, crashes, and slow updates.

### **2\. Praise in Satisfied Reviews (5-Star Reviews)**

* Highly rated reviews highlighted:  
  * Audio Quality : High-quality streaming experience.  
  * User Interface : Intuitive and easy-to-use design.  
  * Offline Listening : Ability to download songs for offline playback.

### **3\. Sentiment Distribution**

* Most reviews fell under the neutral category, suggesting that many users do not express strong emotions in their feedback.  
* A significant portion of reviews had positive sentiment , reflecting overall satisfaction with Spotify's features.

### **4\. Feature Requests**

* Users frequently requested:  
  * Reduction in ads for free-tier users.  
  * Improved stability and fewer bugs.  
  * Enhanced personalization options.

---

## **Visualizations**

### **1\. Bar Plots**

* Top words in 1-star reviews: Highlighted complaints such as "ads," "updates," and "music."  
* Top words in 5-star reviews: Featured praise for "quality," "interface," and "offline."

### **2\. Word Clouds**

* Negative Reviews : Dominated by terms like "ad," "crash," and "slow."  
* Positive Reviews : Focused on "great," "love," "sound," and "easy."

### **3\. Boxplots**

* Showcased sentiment score distributions across different rating levels (1–5).

---

## **Dependencies**

To run this notebook, install the following Python libraries:

bash

1  
pip install numpy pandas matplotlib seaborn nltk vaderSentiment wordcloud

Additionally, ensure NLTK resources are downloaded:

python

1  
2  
import nltk  
nltk.download('punkt')  
---

## **Acknowledgments**

* Data Source : Reviews scraped from Spotify's app store page.  
* Tools Used :  
  * nltk for text preprocessing.  
  * vaderSentiment for sentiment analysis.  
  * matplotlib and seaborn for visualizations.  
  * wordcloud for generating word clouds.

Special thanks to the open-source community for providing robust tools and libraries\!

---

## **Conclusion**

This analysis provides valuable insights into user perceptions of Spotify. It highlights areas where the platform excels and identifies opportunities for improvement. By addressing common pain points (e.g., excessive ads and app stability), Spotify can enhance user satisfaction and retention.

For any questions or suggestions, feel free to reach out\!

