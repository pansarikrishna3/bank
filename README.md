# Retail Banking Customer Segmentation

### A data-driven approach to identifying customer personas for targeted marketing.

## Project Overview

This project involves analyzing a marketing dataset from a European retail bank to identify distinct customer segments. Using unsupervised machine learning (K-Means clustering), we group customers based on their demographics, financial status, and campaign interaction data. The primary outcome is the creation of actionable customer personas that can be used to develop targeted and more effective marketing strategies.

## Business Objective

The goal is to move from a generic, one-size-fits-all marketing approach to a data-driven, segmented strategy. By understanding the different types of customers, the bank can:

-   **Identify Key Customer Groups:** Discover the most valuable, most promising, and at-risk customer segments.
-   **Tailor Marketing Strategies:** Design personalized marketing campaigns, product offers, and communication styles for each segment.
-   **Improve Campaign Efficiency & ROI:** Increase conversion rates and customer engagement by sending the right message to the right person, while reducing marketing spend on less receptive groups.

## Dataset

The project utilizes the **"Bank Marketing"** dataset from the UCI Machine Learning Repository. It contains data on over 45,000 clients and includes information on:

-   Customer demographics (age, job, marital status)
-   Financial attributes (account balance, loans)
-   Past campaign interaction data (duration of contact, number of contacts)

## Methodology

The project followed a structured data science workflow:

1.  **Data Loading and Exploration:** The dataset was loaded and initial exploratory checks were performed to understand its structure and features.
2.  **Exploratory Data Analysis (EDA):** Visualizations were created using Matplotlib and Seaborn to analyze the distributions of key variables like customer age, job type, and account balance.
3.  **Data Preprocessing:** Key features (`age`, `balance`, `duration`, `campaign`) were selected for clustering. These features were then scaled using `StandardScaler` to ensure the K-Means algorithm treated them equally.
4.  **Model Validation:** To ensure a statistically sound segmentation, two methods were used to determine the optimal number of clusters:
    -   **The Elbow Method:** Plotted model inertia against the number of clusters, with the "elbow" indicating a good choice.
    -   **Silhouette Score:** Calculated to measure the density and separation of the clusters. A score of **0.303** was achieved for k=3, indicating a meaningful and well-defined segmentation.
5.  **Clustering:** The K-Means algorithm was applied to the preprocessed data to group customers into 3 distinct segments.
6.  **Persona Definition:** The characteristics of each cluster were analyzed to create detailed, business-focused customer personas.

## Key Findings & Business Recommendations

The analysis successfully identified three key customer personas with distinct characteristics and needs:

> ### Persona 1: The 'Engaged Champions'
>
> -   **Characteristics:** This group has the highest average account balance and the longest average call duration, indicating high engagement and value.
> -   **Business Recommendation:** Target this segment with premium financial products, such as wealth management services and investment opportunities. Nurture these relationships with dedicated client advisors.

> ### Persona 2: The 'Steady Savers'
>
> -   **Characteristics:** This segment represents the core customer base with moderate account balances and engagement levels. They are the largest group.
> -   **Business Recommendation:** Focus on increasing their value over time by cross-selling standardized products like credit cards, personal loans, and promoting digital banking adoption for higher efficiency.

> ### Persona 3: The 'Potentially Fatigued'
>
> -   **Characteristics:** This group has been contacted the most frequently during past campaigns but has a relatively low account balance.
> -   **Business Recommendation:** This segment is at risk of marketing fatigue. Immediately reduce their contact frequency. Re-engage them with a different, more personalized approach (e.g., a targeted email with a unique offer) to prevent churn and rebuild the relationship.

## Technical Stack

-   **Language:** Python
-   **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
-   **Environment:** Google Colab

## How to Run the Project

1.  Clone this repository.
2.  The project is contained within the `.ipynb` notebook file. Upload this file to Google Colab.
3.  The notebook is self-contained and includes the code to upload the `bank-full.csv` dataset when the first cell is run. Simply follow the prompt to upload the file from your local machine.
