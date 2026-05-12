# Student Performance-and-Dropout-Risk-Analysis-using-Python-and-PowerBI

## Table of Contents
-  [Project Overview](#ProjectOverview)
-  [Objectives](#Objectives)
-  [Dataset Information](#DatasetInformation)
-  [Technologies Used](#TechnologiesUsed)
-  [Purpose of the Dataset](#PurposeoftheDataset)
-  [Important Columns in Dataset](#ImportantColumnsinDataset)
-  [Data Preprocessing](#DataPreprocessing)
-  [Exploratory Data Analysis (EDA)](#ExploratoryDataAnalysis(EDA))
-  [Univariate Analysis](#UnivariateAnalysis)
-  [Bivariate Analysis](#BivariateAnalysis)
-  [Multivariate Analysis](#MultivariateAnalysis)
-  [Advanced plot](#Advancedplot)
-  [Power BI Dashboard](#PowerBIDashboard)
-  [Insights](#Insights)
-  [Conclusion](#Conclusion)
  
# Project Overview

This project focuses on analyzing student engagement and academic performance using Python and Power BI. The main goal of this project is to identify learning patterns, engagement levels, and risk factors that affect student performance.

The project includes data cleaning, preprocessing, exploratory data analysis (EDA), visualization, and dashboard creation to generate meaningful insights from the dataset.

---

# Objectives

* Analyze student engagement and performance.
* Identify high-risk and low-performing students.
* Understand the relationship between engagement and academic scores.
* Create interactive dashboards for better decision-making.
* Generate insights using Python visualizations and Power BI.

---

#  Dataset Information
 * source:Kaggle
 * domain:Education
* timeline: Not specified in dataset 
* Format: CSV File
* Data size: 32593 rows and 14 columns
* Data Type: Numerical and Categorical

  
# Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Power BI
  

-- 

## Purpose of the Dataset

The dataset helps analyze:

* Student engagement behavior
* Academic performance trends
* Learning activity patterns
* Risk identification
* Performance prediction

## Important Columns in Dataset

| Column Name       | Description                                    |
| ----------------- | ---------------------------------------------- |
| Student ID        | Unique ID for each student                     |
| Total Clicks      | Number of interactions with learning materials |
| Studied Credits   | Total credits completed by students            |
| Average Score     | Academic performance score                     |
| Engagement Level  | Categorized as Low, Medium, or High            |
| Risk Level        | Indicates Safe, Low Risk, or High Risk         |
| Performance Level | Student performance category                   |


---

# Data Preprocessing

The following preprocessing steps were performed:

* Handled missing values
* Cleaned duplicate records
* Converted data types
* Created categorical columns
* Performed binning for score categories(at power bi)
  

---

# Exploratory Data Analysis (EDA)

Different charts and visualizations were created to analyze the dataset:

## Univariate Analysis

* Histogram: This chart shows distribution of student scores.
* Most students fall in medium to high score range(70 to 90).

* Feature used: avg_score

* It means that a larger proportion of students are achieving higher scores, while fewer students are struggling with very low scores.
* <img width="1027" height="836" alt="Screenshot 2026-05-08 195159" src="https://github.com/user-attachments/assets/f643cae2-3aac-4e68-8a28-5f61eadbf1f4" />

* Box Plot: This chart shows spread of clicks and identifies outliers.
* Most users click between 400 to 1400,with a median around 800. The data is right skewed and there are some outliers with very high click values above 3000.

* Feature used: total_clicks

* This shows that only small number of users highly active compared to majority .
* <img width="914" height="750" alt="Screenshot 2026-05-08 195312" src="https://github.com/user-attachments/assets/b48b4c1b-e30e-41f0-a5e8-d4b3bb1a1eb3" />


* Count Plot: This chart shows number of students in each result category.
* Majority students passed.

* Feature used: final_result

* This shows success rate is high and the characteristics of 'Fail' and 'Withdrawn' students to understand the reasons behind their outcomes and potentially intervene.
*  <img width="1011" height="741" alt="Screenshot 2026-05-08 195241" src="https://github.com/user-attachments/assets/9f201796-372a-4579-b55a-09a871a41ee3" />



## Bivariate Analysis

* Scatter Plot: This chart shows relationship between clicks and avg_score.
* As the number of clicks increases,average scores also increases indicating positive correlation. most students with higher click score between 60 to 100.

* Features used: total_clicks, avg_score

* Higher engagement leads to better performance, though the correlation is weak.
* <img width="946" height="761" alt="Screenshot 2026-05-08 195416" src="https://github.com/user-attachments/assets/8d3f9882-2630-4f24-b23b-f1efe05825c3" />


* Bar Chart: This chart shows average score based on engagement level.
* High engagement students have the highest average score(75-78), Medium engagement students have the slightly lower scores(70-72), low engagement students have the lowest scores(68-70).

* Features used: engagement_level, avg_score.

* This indicates that increased engagement positively impacts students performance.
* <img width="935" height="736" alt="Screenshot 2026-05-08 195452" src="https://github.com/user-attachments/assets/d7a8a3d9-6bc8-4691-96bc-748b94be68dc" />


* Correlation Heatmap: This chart shows correlation between numerical variables.
* There is a weak positive correlation(0.19)between clicks and score, indicating that increased activity slightly improves performance.however studied credits (0.0029)shows almost no correlation with score and clicks,meaning they don't signifiantly impact performance.

* Features used: total_clicks, avg_score, studied_credits

* There is a positive relationship between clicks and score, other features(studied_credits)do not strongly affect performance.
* <img width="915" height="685" alt="Screenshot 2026-05-08 195544" src="https://github.com/user-attachments/assets/2840c84a-5589-4d52-b688-bbbe5841802c" />



## Multivariate Analysis
* pairplot: It is a pairplot used to show relationship between multiple numerical features.
* 1.Diagonal(histograms):

total_clicks: right skewed(most students have low clicks, few have very high clicks).

avg_score: mostly between 40 to 100 (many students scoring in higher range).

studied_credits: concentrated values (most students take similar number of credits)

* 2.total_click vs avg_score:

slight upward trend -weak positive relationship(more clicks lead to slightly higher scores).
* 3.total_click vs studied credits:

points scattered randomly- no clear pattern(click activity not related to credits)
* 4.avg_score vs studied_credits:

no clear trend- no relationship(credits do not strongly affect score)
* Features used: total_clicks, avg_score, studied_credits.

* Clicks have some impact on score( but weak) and studied_credits have almost no impact while scores are mostly concentrated in higher ranges.
* <img width="1082" height="773" alt="Screenshot 2026-05-09 065329" src="https://github.com/user-attachments/assets/d0be64f0-761d-4618-82b1-3b01147a0857" />


* grouped analysis: This  shows the relationship between students' engagement level and their pass rate.
* Students with high engagement have a higher pass rate. Students with low engagement have a lower pass rate. There is a clear positive relationship between engagement and success

* Features used: engagement_level, pass_flag.

* Low engagement students may need extra attention or support
* <img width="808" height="391" alt="image" src="https://github.com/user-attachments/assets/7c82f032-019d-4c74-93bb-c83bf284f471" />


# Advanced plot
* violin plot: This violin plot shows the distribution and density of students average scores across different performance levels.
* The width of each "violin" indicates where more students are concentrated within that performance level.

* features used: performance_level, avg_score.

* Performance level strongly influences student scores, with high performers consistently achieving better results.
* <img width="934" height="795" alt="Screenshot 2026-05-08 195703" src="https://github.com/user-attachments/assets/d1a21df9-55f3-4038-a39c-1d662f994485" />  

# Power BI Dashboard

An interactive Power BI dashboard was created to visualize:
<img width="1353" height="775" alt="Screenshot 2026-05-08 142026" src="https://github.com/user-attachments/assets/2f3b24e8-f86c-47ba-b358-080d4daff8e8" />


* Total Students
* Pass Percentage
* High Risk Students Count
* Average Scores
* Engagement Distribution
* Performance Analysis
* Risk Analysis

The dashboard helps users quickly understand student behavior and academic performance.


## Insights 
1. What is the strongest factor influencing student performance in this dataset?

* Student engagement, measured through total clicks, appears to be the strongest factor influencing academic performance. The scatter plot shows that students with higher interaction levels consistently achieve higher average scores, indicating that active participation improves learning outcomes.

2. What does the dashboard reveal about dropout risk?

* The dashboard identifies a significant number of high-risk students with lower engagement and lower academic scores. These students are more likely to withdraw or fail, showing a direct connection between reduced learning activity and dropout probability.

3.  What pattern is observed between engagement level and pass percentage?

* Students with high engagement levels achieved the highest pass rate (around 74%), while low-engagement students showed very poor pass rates. This suggests that learning platform activity is strongly associated with academic success.

4. Which group of students requires immediate academic intervention?
* Students classified under:


  High Risk


  Low Engagement


  Low Average Scores


  require immediate intervention because they show poor participation and weak academic performance, increasing the likelihood of dropout.

5.  What does the violin plot reveal about student performance behavior?

* The violin plot shows that high-performing students maintain consistently strong scores with less variation, whereas low-performing students have unstable and widely distributed scores. This indicates inconsistency in learning behavior among struggling students.

6. What insight is obtained from the final result distribution?

* A large number of students are categorized under pass and withdrawal outcomes. The withdrawal count indicates that many students disengage before successful completion, highlighting the need for early-risk monitoring systems.

7.  What does the engagement vs average score chart indicate?

* The chart confirms that average scores increase with engagement levels. Students who actively access learning materials and interact with the platform tend to perform better academically.

8. What hidden behavioral trend is visible in the dataset?

* The dataset reveals that some students have moderate engagement but still achieve lower scores, indicating that engagement alone is not sufficient. Learning quality, study effectiveness, or prior academic ability may also influence outcomes.

9.  What business or institutional value does this project provide?

* This project helps educational institutions:


   Detect at-risk students early


   Improve retention rates


   Monitor student engagement


   Support academic decision-making


   Reduce dropout percentages through targeted intervention


 10.  What is the overall conclusion of the project?

* The overall analysis concludes that student engagement plays a critical role in academic success. Low-engagement students are more likely to perform poorly and fall into high-risk or dropout categories. By monitoring engagement metrics and performance indicators, institutions can proactively support vulnerable students and improve educational outcomes.

---

# Conclusion

This project demonstrates how data analytics can be used in the education domain to monitor student engagement and predict performance trends. The analysis helps institutions identify at-risk students and improve learning outcomes through data-driven decisions.



---

# Author

Rajeswari K 


