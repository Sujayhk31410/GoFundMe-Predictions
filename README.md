# **GoFundMe Campaign Success Prediction**

This project analyzes GoFundMe campaign data to predict fundraising success by analyzing narratives and visual content. Leveraging machine learning and image analysis, the goal is to provide actionable insights for campaign organizers to optimize their fundraising strategies and achieve their goals.

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [Data Collection and Processing](#data-collection-and-processing)
4. [Methodology](#methodology)
   - [Text Analysis](#text-analysis)
   - [Visual Feature Extraction](#visual-feature-extraction)
   - [Machine Learning Models](#machine-learning-models)
5. [Results](#results)
6. [Impact](#impact)
7. [Technologies Used](#technologies-used)
8. [Future Enhancements](#future-enhancements)
9. [How to Run](#how-to-run)
10. [Contributors](#contributors)

---

## **Project Overview**

GoFundMe is the world’s largest crowdfunding platform, helping individuals and organizations raise funds for various causes such as medical emergencies, education, and community projects. This project seeks to predict the success of campaigns by analyzing campaign narratives and visual features, using machine learning models to gain insights into fundraising behaviors.

---

## **Objectives**
- **Predict Campaign Success:** Build models to predict daily fundraising amounts and identify the likelihood of meeting campaign goals.
- **Analyze Narrative and Visual Features:** Evaluate how the narrative structure and visual content (images) influence donations.
- **Provide Actionable Insights:** Equip campaign organizers with insights to optimize their campaigns and increase their chances of success.

---

## **Data Collection and Processing**
- **Source:** Data was scraped from the GoFundMe website using Beautiful Soup and Playwright.
- **Dataset:** A total of 8,881 campaigns with the following features:
  - **Textual Data:** Titles, campaign stories.
  - **Visual Data:** Analyzed using the **Face++ API** for attributes like gender, emotion, smile intensity, etc.
  - **Additional Features:** Raised amount, goal amount, number of donations, location, category, and campaign organizer.

**Key Preprocessing Steps:**
- **Text Cleaning:** Removed special characters, extra spaces, and irrelevant symbols to clean the text.
- **Date Conversion:** Transformed relative dates into specific date formats.
- **Feature Extraction:** Created new features like word count, emotion categories, and goal achievement ratio.
  
---

## **Methodology**

### **1. Text Analysis**
- **TF-IDF:** Applied Term Frequency-Inverse Document Frequency (TF-IDF) to identify key words in the campaign narratives.
- **word2vec:** Used word embeddings to capture contextual meanings of words and phrases that impact donation behavior.

### **2. Visual Feature Extraction**
- Utilized the **Face++ API** to analyze images for features such as:
  - **Gender**
  - **Age**
  - **Emotion** (anger, sadness, happiness, etc.)
  - **Smile Intensity**
  - **Beauty Score**

### **3. Machine Learning Models**
- **Regression Models:** Built models to predict the amount raised based on campaign text and visual features.
- **Clustering (K-means):** Grouped campaigns by urgency levels to prioritize those needing immediate support.
- **Hyperparameter Tuning:** Applied **Grid Search** for optimizing model parameters.

---

## **Results**
- **Text and Image Data Correlation:** Both the campaign story text and visual features significantly influenced fundraising success.
- **Urgency Clustering:** Identified high-priority campaigns that could benefit from early intervention.
- **Model Accuracy:** The models showed strong predictive accuracy for daily fundraising amounts and the likelihood of meeting goals.

---

## **Impact**
This project provides valuable tools for campaign organizers to:
- **Optimize Campaigns:** Gain insights into how narrative elements and visuals impact donations.
- **Improve Engagement:** Identify key factors for increasing visibility and engagement in campaigns.
- **Prioritize Urgent Campaigns:** Use urgency clusters to focus on campaigns that require immediate attention.

---

## **Technologies Used**
- **Web Scraping:** Beautiful Soup, Playwright
- **Text Analysis:** TF-IDF, word2vec
- **Image Analysis:** Face++ API
- **Machine Learning:** Scikit-learn, K-means clustering
- **Data Visualization:** Matplotlib, Seaborn

---

## **Future Enhancements**
- **Sentiment Analysis:** Implement more advanced sentiment analysis techniques to better understand emotional tone in campaign narratives.
- **Topic Modeling:** Explore **Latent Dirichlet Allocation (LDA)** to identify key topics in campaigns and analyze their impact on donations.
- **Geographical Influence:** Study how the location of campaigns (e.g., city, state) impacts fundraising success.
- **Social Media Integration:** Add external data sources, such as social media mentions, to enhance prediction accuracy.
- **Temporal Trends:** Analyze the timing of campaigns (e.g., holiday seasons) and its effect on fundraising success.

---

## **How to Run**
1. **Clone this repository:**
   ```bash
   git clone https://github.com/Sujayhk31410/GoFundMe-Prediction.git
