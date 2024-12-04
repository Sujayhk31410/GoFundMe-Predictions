# **Predicting the Success of GoFundMe Campaigns**

This project explores how narrative and visual features influence GoFundMe campaigns and focuses on predicting the raised amount for a campaign on any given day. By leveraging machine learning techniques, we aim to provide actionable insights to help campaign organizers optimize their strategies and improve fundraising outcomes.

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

GoFundMe is the world’s largest crowdfunding platform, enabling individuals and organizations to raise funds for various causes, from medical emergencies to educational initiatives. While some campaigns exceed their goals, others struggle to gain momentum. This project investigates factors influencing campaign success, leveraging data science to predict outcomes and guide effective campaign management.

---

## **Objectives**
- **Predict Campaign Success:** Build models to estimate daily fundraising amounts and determine the likelihood of meeting goals.
- **Analyze Narrative and Visual Features:** Identify the influence of textual and visual elements on donation behaviors.
- **Provide Actionable Insights:** Offer data-driven recommendations to enhance campaign performance.

---

## **Data Collection and Processing**
- **Source:** Web-scraped GoFundMe campaigns using Beautiful Soup and Playwright.
- **Dataset:** 8,881 campaign entries with features including:
  - **Textual Data:** Titles, campaign stories.
  - **Visual Data:** Analyzed using the Face++ API for attributes like gender, emotion, and smile intensity.
  - **Other Variables:** Raised amount, goal amount, location, category, and number of donations.

**Key Preprocessing Steps:**
- Cleaned and formatted text (removed special characters, whitespace, etc.).
- Converted dates to a consistent format.
- Extracted additional features like word count, emotion categories, and goal achievement ratios.

---

## **Methodology**

### **1. Text Analysis**
- **TF-IDF**: Identified the importance of words in campaign narratives.
- **word2vec**: Captured contextual meanings to evaluate the impact of phrases on donations.

### **2. Visual Feature Extraction**
- Extracted image-based features using the Face++ API, including age, emotion, and smile intensity.

### **3. Machine Learning Models**
- **Regression Models:** Predicted the raised amount based on textual and visual features.
- **Clustering (K-means):** Grouped campaigns by urgency to prioritize high-need campaigns.
- **Hyperparameter Tuning:** Applied Grid Search for model optimization.

---

## **Results**
- Text and image data significantly influence the success of campaigns.
- Models demonstrated the potential to predict daily fundraising progress and identify urgent campaigns needing intervention.
- Clustering analysis revealed actionable patterns in donation timing and behaviors.
- The strongest predictors of the raised amount are numeric features like the number of donations, goal progress ratio, and goal amount, which directly impact fundraising success. Text-based features, such as specific words in the campaign description (e.g., family, little, health, world), enhance emotional and contextual appeal, motivating donors. Visual elements (e.g., beauty) and descriptive length also contribute, though their impact is secondary to numeric features.

---

## **Impact**
This project provides a practical tool for campaign organizers, enabling them to:
- Understand the factors that drive donations.
- Optimize campaign narratives and visuals.
- Prioritize efforts for maximum fundraising impact.

---

## **Technologies Used**
- **Web Scraping:** Beautiful Soup, Playwright.
- **Text Analysis:** TF-IDF, word2vec.
- **Image Analysis:** Face++ API.
- **Machine Learning:** Scikit-learn (for regression, clustering, and classification tasks).
- **Data Visualization:** Matplotlib, Seaborn.

---

## **Future Enhancements**
- **Predicting Campaign Duration**: Develop models to estimate the duration a campaign will take to meet its goal based on early donation patterns and narrative content.
- **Temporal Analysis**: Study how campaign timing (e.g., holiday seasons, weekday vs. weekend) influences fundraising success, potentially building time-based prediction models.
- **Fraud Detection in Crowdfunding**: Develop models to identify potentially fraudulent campaigns based on unusual patterns in text, image, and donation data, improving the integrity of the platform.
- **Social Media & User Engagement**: Integrate social media data (e.g., Twitter, Instagram) to assess the impact of social sharing, comments, shares, and likes on campaign success and performance.
- **Multi-Language Support**: Extend the project to support multi-language campaigns, using language translation tools and multilingual NLP models to analyze and predict success across different languages.

---

## **How to Run**
1. Clone this repository:
   ```bash
   git clone https://github.com/Sujayhk31410/GoFundMe-Prediction.git
