#  Flipkart Smartphone Market Analysis

## Project Overview:
This project is an end-to-end data analytics workflow that analyzes the Indian smartphone market using data scraped from Flipkart.

The project covers:
* Web Scraping using Requests and BeautifulSoup
* Data Cleaning and Preprocessing
* Feature Engineering
* Exploratory Data Analysis (EDA)
* Business Insights and Market Analysis

A total of **984 smartphone listings** were collected and analyzed to understand pricing patterns, brand positioning, customer ratings, storage trends, RAM distribution, and value-for-money offerings in the smartphone market.



# Objectives:
The primary objectives of this project were:
* Extract smartphone data from Flipkart using web scraping.
* Build a structured dataset from raw HTML pages.
* Clean and preprocess real-world messy data.
* Engineer meaningful features for analysis.
* Explore pricing trends and brand strategies.
* Identify value-for-money smartphone brands and segments.
* Generate business insights from smartphone market data.



# Dataset Information:
### Total Records:
* 984 Smartphone Listings

### Features Collected
| Feature           | Description                 |
| ----------------- | --------------------------- |
| Product Name      | Smartphone model name       |
| Brand             | Smartphone brand            |
| Price             | Current selling price       |
| Original Price    | Original listed price       |
| Discount %        | Discount offered            |
| Rating            | Average customer rating     |
| Ratings Count     | Number of ratings           |
| Reviews Count     | Number of reviews           |
| RAM (GB)          | RAM capacity                |
| Storage (GB)      | Internal storage            |
| Rear Camera (MP)  | Rear camera specifications  |
| Front Camera (MP) | Front camera specifications |
| Battery (mAh)     | Battery capacity            |



# Technologies Used:
* Python
* Requests
* BeautifulSoup
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Regular Expressions (Regex)



# Project Workflow:

## 1. Web Scraping
Smartphone listings were scraped from Flipkart using:
* Requests
* BeautifulSoup

### Steps:
* Downloaded 125 Flipkart search result pages.
* Parsed HTML files locally.
* Extracted product information.
* Stored data in a structured DataFrame.
* Exported raw dataset as CSV.


## 2. Data Cleaning
Several data quality issues were identified and resolved.

### Cleaning Tasks
* Removed duplicate records.
* Standardized brand names.
* Fixed inconsistent text values.
* Investigated missing values.
* Recovered missing storage values from product names.
* Corrected invalid battery values.
* Recovered missing Original Price values.
* Recovered missing Discount % values.
* Cleaned camera-related fields.

### Example
Original Price was recovered using:
Original Price = Price / (1 - Discount%)


## 3. Feature Engineering
Several new analytical features were created.

### Price_per_GB
Measures storage value for money.
Price_per_GB = Price / Storage

### Price_Segment
Smartphones were categorized into:
* Budget
* Midrange
* Upper Midrange
* Premium

### Value_Score
A custom metric combining customer satisfaction and popularity.
Value_Score = Rating × log(1 + Ratings Count)

### Camera Features
Extracted:
* Rear_Main_MP
* Front_MP
* Rear_Camera_Count


# Exploratory Data Analysis
The following analyses were performed:

## Brand-wise Average Price
* Apple recorded the highest average smartphone price.
* Google emerged as the leading premium Android brand.
* Budget-focused brands offered significantly lower average prices.

## RAM Distribution
* 8GB RAM was the most common configuration.
* Indicates industry preference for balancing performance and affordability.

## Storage Distribution
* 128GB storage dominated the market.
* 256GB storage is becoming increasingly common.
* 512GB and 1TB remain niche premium offerings.

## Price Segment Analysis
* Midrange smartphones represented the largest market segment.
* Budget devices also accounted for a significant share.
* Premium smartphones formed a smaller portion of listings.

## Camera vs Price Analysis
* Higher camera megapixels generally corresponded to higher prices.
* Pricing was influenced by multiple factors beyond camera specifications.

## Value Score Ranking
* Apple devices dominated the highest Value Scores.
* Certain budget devices also ranked highly due to strong ratings and popularity.

## Price vs RAM Analysis
* Higher RAM configurations were generally associated with higher prices.
* Significant variation suggested additional pricing factors beyond RAM.

## Rating vs Price Analysis
* Higher-priced smartphones tended to receive slightly better ratings.
* Customer satisfaction depended on overall experience rather than price alone.

## Brand-wise Rating Analysis
* Most major brands maintained ratings above 4.0.
* Apple achieved the highest average customer rating.


# Business Questions Answered

## Which Brand Offers the Best Value?
Top-performing value brands included:
* CMF
* Lenovo
* Apple
* POCO
* MOTOROLA


## Which Brand Offers the Highest RAM per Rupee?
Top brands:
* POCO
* Infinix
* CMF
* MOTOROLA
* realme

These brands delivered the strongest memory-to-price ratio.


## Which Price Segment Has the Highest Average Rating?
Premium smartphones recorded the highest average customer ratings.

## Which Price Segment Provides the Highest Value Score?
Budget smartphones achieved the highest average Value Score, indicating stronger value-for-money performance.

# Key Insights
* The Indian smartphone market is heavily concentrated in the Midrange segment.
* 8GB RAM and 128GB storage have become the industry standard.
* Premium smartphones achieve higher customer satisfaction ratings.
* Budget smartphones provide the strongest value-for-money proposition.
* Brand reputation significantly influences smartphone pricing.
* Hardware specifications alone do not fully explain price differences.


# Repository Structure

```text
Flipkart-Smartphone-Market-Analysis/

│
├── data/
│   ├── smartphones_raw.csv
│   └── mobile_phones_cleaned.csv
│
├── notebooks/
│   ├── 1-Web Scraping.ipynb
│   ├── 2-Cleaning the Data.ipynb
│   └── 3-Exploratory Data Analysis.ipynb
│
├── images/
│   ├── brand_price.png
│   ├── ram_distribution.png
│   ├── storage_distribution.png
│   ├── value_score.png
│   └── other_visualizations.png
│
├── README.md
│
└── requirements.txt
```


# Future Improvements
* Smartphone Price Prediction using Machine Learning
* Interactive Dashboard using Tableau or Power BI
* Automated Data Collection Pipeline
* Sentiment Analysis on Customer Reviews
* Brand Recommendation System
