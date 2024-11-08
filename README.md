# Purchase-Propensity-for-online-consumers
### Abstract
The study of online purchase behavior has become increasingly important with the exponential growth of e-commerce. This report delves into the various factors influencing consumer behavior in online shopping, including the social, and technological aspects derived from data. The research employs both qualitative and quantitative methodologies to explore these factors, providing a comprehensive understanding of the motivations, preferences, and deterrents for consumers engaging in online purchases.

For newly acquired customers, the data collected for analysis can help companies develop strategies to grow the right customers and decrease customer churn.In this study, predictive analysis is applied to estimate customers more likely to purchase online , therefore various predictive machine learning models have been applied. 
## 1. Introduction
### 1.1 Background
The advent of the internet has revolutionized the way consumers shop.The proliferation of digital technologies and the widespread accessibility of the internet have dramatically transformed the landscape of consumer shopping behavior. Online shopping, once a novelty, has become an integral part of daily life for millions of people worldwide. The shift from traditional brick-and-mortar stores to online retail platforms has been fueled by the convenience, variety, and often, better prices, contributing to its increasing popularity. As a result, understanding the intricacies of online purchase behavior has become essential for businesses looking to thrive in the digital age.Understanding the behavior of online consumers is crucial for businesses to strategize effectively and for researchers to develop theories that explain this modern shopping paradigm. 

In this fiercely competitive market, customers demand tailored products and better services at fewer prices, while service providers constantly focus on acquisitions as their business goals. The annual churn rate in the e-commerce industry can vary widely but is typically high. Studies show that the average churn rate for e-commerce businesses can range from 70% to 80%, indicating that a significant portion of customers do not return for repeat purchases​​. In terms of acquiring new customers, the average cost can also vary, but it tends to be substantial. For e-commerce businesses, the cost to acquire a new customer (CAC) often falls between $10 and $50. This cost includes marketing expenses, promotional offers, and other efforts to attract new buyers​​. Given the high churn rates and significant acquisition costs, e-commerce businesses must focus on customer retention strategies to improve profitability and sustain growth. Strategies such as personalized marketing, loyalty programs, and exceptional customer service are critical to reducing churn and fostering customer loyalty​​.
Conventional statistical methods are widely used in predicting customer churn and survival. Machine Learning models such as (Decision Tree , Random Forest, etc.) are developed to handle time-to-event data, making it a robust and efficient tool for predicting both the likelihood of customer churn and the expected duration until churn occurs.
This case study aims to delve into the specific behaviors, preferences, and decision-making processes of consumers in the context of online shopping. By focusing on a detailed examination of consumer interactions with online retail platforms, the study seeks to uncover the factors that drive online purchase decisions, the barriers consumers face, and the overall experience of shopping online. This case study is particularly relevant as it provides real-world insights and practical implications that can help e-commerce businesses optimize their strategies and improve customer satisfaction.
### 1.2 Objectives
The business objective of this study aims to uncover significant relationships, trends and patterns. 
To identify key metrics which contribute the most towards predicting a shopper's behavior and to suggest prioritized critical recommendations and performance improvements on the same.
To explore the psychological and social dynamics of online shopping: Understanding how social influences, peer reviews, and online communities affect consumer behavior.
To assess the impact of technological aspects: This involves evaluating the user experience on e-commerce websites, the importance of website design, functionality, and security features in shaping consumer trust and satisfaction.
To provide actionable insights for e-commerce businesses: Based on the findings, the study aims to offer recommendations for enhancing the online shopping experience and driving consumer loyalty.

### 1.3 Factors Influencing Online Purchase Behavior
Psychological Factors: Trust, perceived risk, and consumer attitudes.
Social Factors: Influence of social media, peer reviews, and word-of-mouth.
Technological Factors: Website design, ease of navigation, and security features.

## 2. Research Methodology:
### 2.1 Data Source
The dataset used in our analysis was obtained from the UC Irvine Machine Learning Repository, a popular website with hundreds of datasets available for analysis. The creators of the dataset are C. Sakar and Yomi Kastro, and the original dataset can be obtained at [Sakar and Kasto, 2018] link.
Source Link: 
### https://www.openml.org/search?type=data&status=active&id=45060&sort=runs
Since the data source is from a third party vendor, here is a brief description of some of the data follows. The dataset includes the following fields:

1.Administrative :The number of pages of this type (administrative) visited by the user in that session.

2.Administrative_Duration : The total amount of time (in seconds) spent by the user on administrative pages during the session.

3.Informational: The number of informational pages visited by the user in that session.

4.Informational_Duration : The total time spent by the user on informational pages.

5.ProductRelated : The number of product-related pages visited by the user.

6.ProductRelated_Duration : The total time spent by the user on product-related pages.

7.BounceRates : The average bounce rate of the pages visited by the user. The bounce rate is the percentage of visitors who navigate away from the site after viewing only one page.

8.ExitRates : The average exit rate of the pages visited by the user. The exit rate is a metric that shows the percentage of exits from a page.

9.SpecialDay : This indicates the closeness of the site visiting time to a specific special day (e.g., Mother’s Day, Valentine's Day) in which the sessions are more likely to be finalized with a transaction.

10.Month : The month of the year in which the session occurred. OperatingSystems: The operating system used by the user.

11.Browser : The browser used by the user.

12.Region : The region from which the user is accessing the website.

13.TrafficType : The type of traffic (e.g., direct, paid search, organic search, referral).

14.VisitorType : A categorization of users (e.g., Returning Visitor, New Visitor).

15.Weekend : A boolean indicating whether the session occurred on a weekend.

16.Revenue: This binary variable is the Target variable for prediction indicating whether the session ended in a transaction (purchase).

The target feature and class label in the dataset is called Revenue and contains either a True or False value, which correspond to whether or not the user made a purchase on the website during their visit, respectively. It is worth noting that the dataset is unbalanced, as 85% of the sessions contain a False class label, with the remaining 15% containing a True label.
The research methodology outlined provides a robust framework for investigating online purchase behavior. By combining qualitative and quantitative approaches, the study aims to generate comprehensive insights into the factors driving online consumer behavior, which can inform both academic understanding and practical strategies for e-commerce businesses.
### 3. Exploratory Data Analysis
Our dataset consists of numeric and categorical features. Amongst these features, the “BounceRates”, “ExitRates” and “PageValues” features represent the metrics measured by Google Analytics for each session on the e-commerce site. The key observations from our data analysis are:

Our dataset is imbalanced, where only 15% of sessions ended in a purchase

PageValues may be one of the most important feature in predicting a purchase conversion

Many numeric features are right-skewed.

![Screenshot 2024-11-08 102244](https://github.com/user-attachments/assets/ee1ecb1b-ef0c-4aa6-88b7-fb9cb5847d4b)


