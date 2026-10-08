# 📊 MexEE 402: Data Preprocessing Case Study

> **MexEE Elective 2: Data Science and Machine Learning**  
> Batangas State University, Alangilan Campus  
> **1st Semester, AY 2026-2027**

---

## 👥 Members

| Name | Student Number | Section |
|---|---|---|
| Cabatay, Alyssa Joyce D. | 23-03626 | MEXE-4101 |
| Real, Dustin A. | 23-09012 | MEXE-4101|

---

## 📓 Notebook Links

| Chapter | 👤 Member 1 | 👤 Member 2 |
|:---:|:---:|:---:|
| Ch1_2_3 |[https://colab.research.google.com/drive/1qddYEyor1uX5K5H54zY9yMsfmo5453dG?usp=sharing] | [View Notebook] |
| Ch4 |[https://colab.research.google.com/drive/19b6XNo1yItT6vG7NoxzQU5nLrWZ4R8XI?usp=sharing] | [View Notebook] |
| Ch5 |[https://colab.research.google.com/drive/1GP2fKjKhSMQd7XUP7HV39IJwEgTjvMK5?usp=sharing] | [View Notebook] |
| Ch6 |[https://colab.research.google.com/drive/1DapSmI8WYo3AGs_t5XZXjmkbcAFIdzPk?usp=sharing] | [View Notebook] |
| Ch7 |[https://colab.research.google.com/drive/1uXOnySdpYnLO0LI4nmrhgGoGXCAOWfNz?usp=sharing] | [View Notebook] |
| Ch8 |[https://colab.research.google.com/drive/1mu3qHdfY1AIkoXVppUObXTuLSKd5kFP5?usp=sharing] | [View Notebook] |
| Ch9 |[https://colab.research.google.com/drive/1ftBXLWWwKFJ4nEDqoCJ8y1EK91AkuuJZ?usp=sharing] | [View Notebook] |

## 💡 What We Learned

###  Chapter 1 - Introduction to Data Pre-processing

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In Chapter 1,we discovered that data preprocessing is an essential stage before conducting analysis as the data may contain errors such as missing values, inconsistencies, or redundant data. We understood that having processed and cleaned data makes the results of analysis more reliable. Moreover, what surprised us is that  even little inconsistencies can affect the entire process; hence it would be better to sort out the inconsistencies first and then analyze the data. It became clear to us that data pre-processing is indeed an important aspect of the analysis process and not an additional step.

###  Chapter 2 - The Power of Data: Initial Steps in Loading, Understanding, and Exploring Data with Python

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;From the second chapter, we learned  the significance of understanding the data before using it. We understood that loading the data is just the beginning, since there are other issues such as checking the type of the data, inspecting the actual values, and the general information of the data. In addition, the surprising thing that we have discovered is that looking at the dataset itself allows us  to find some issues or patterns that could go unnoticed if we immediately analyze the data . Another important thing that we found out is that the knowledge of the data structure makes it easier for us to make decisions about the next actions. Overall, this chapter helped us realize that we need to understand the data first before proceeding with the analysis. 

###  Chapter 3 - Cleaning Your Data 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In Chapter 3, we learned  that cleaning data is an essential step towards making the dataset more accurate. It was clear to us  that there are issues with missing values and duplicate or unnecessary data that influence the results, and thus they should be cleaned. Furthermore, What was surprising is that cleaning data does not mean deleting something. Sometimes, the missing values can be substituted or replaced based on some conditions. Also, we have seen that the approach we use for cleaning the data impacts the result of the analysis. Therefore, we realized that we should be careful in choosing what should be removed or kept.

###  Chapter 4 - Transformation, feature engineering, and encoding 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;From Chapter 4, we learned that feature engineering is an important part of data preparation since data can be transformed into features. We understood that methods such as binning, interaction features, and polynomial features can help discover relationships that would have been hard to find out from the raw data. The surprising thing about the chapter is that it is possible to create new features using existing data, such as combining features or converting numerical values into categorical values. We also learned that categorical data should be encoded into numerical data using methods such as one-hot encoding and ordinal encoding before it is used in a machine learning model. 

###  Chapter 5 - Scaling and normalization

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;In Chapter 5 we learned that scaling and normalization become essential if the features are in different numeric ranges. It was clear that a feature with  large numbers may be more dominant than other features even though it may not be more significant. What was surprising was that scaling can place the different features in a similar level, for example, the number of hours of studying and the grade. Another thing that we learned was that normalization can change the values into a scale of 0 to 1, while standard scaling changes the values based on their mean and standard deviation.

###  Chapter 6 - 	Outlier detection

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chapter 6 helped us understand why unusual values in a dataset should be checked before doing an analysis. We saw that different methods can identify different outliers, especially with the value 100, which was detected by the IQR method but not by the Z-score method. This showed us that one method may not always be enough when checking unusual data.

###  Chapter 7 - 	Feature selection

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This chapter showed us that not every feature in a dataset is needed for making predictions. Some features can be removed while keeping the ones that are more useful to the model. We also noticed that different feature selection methods can produce different results, so the method used can affect which features are chosen. 

###  Chapter 8 - 	Constructing a preprocessing pipeline

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;For Chapter 8, we understood how different preprocessing steps can be combined into one organized process. The conveyor belt example helped us picture how data goes through each step in order until it is ready for a machine learning model. We also saw that using a pipeline can make the process easier to repeat and less prone to mistakes.

###  Chapter 9 - Full pipeline and visualization

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Chapter 9 showed us that different types of data require different ways of preprocessing. Numerical values, categorical values, and missing data may need separate methods depending on the situation. This helped us understand that preparing the data properly is an important part of getting more reliable results from the analysis.



 ## 🔎 Errors We Found

 **Issue 1: Chained `inplace=True` on a column (Ch3, Handling Missing Values)**

- **Original:** `df['Year'].fillna(df['Year'].mean(), inplace=True)`
- **Problem:** `inplace=True` is used on a selected column, which may be a copy. This can cause a warning and may not modify the original DataFrame in newer pandas versions.
- **Correct version:**
  ```python
  df['Year'] = df['Year'].fillna(df['Year'].mean())
  df['Publisher'] = df['Publisher'].fillna(df['Publisher'].mode()[0]) 


## 🤖 Note on AI Tools

We used AI tools, specifically **Claude AI**  to check and improve our code and identify possible errors in the notebooks. We reviewed and verified the suggestions before including them in our work.


## 📚 References

- McKinney, W. (2021). *Python for Data Analysis*, 3rd ed. O'Reilly.
- VanderPlas, J. *Python Data Science Handbook*.

