# **CHURN_CUSTOMERS**
## BUSINESS UNDERSTANDING
Syria Tel, a telecommunication company, wants to predict customer churn. Identifying customers who are likely to stop using their services soon. Churn represents a major financial challenge, as acquiring new customers is often more expensive than retaining existing ones. By analyzing customer data, Syria Tel can devolop targeted strategies to improve customer retention and reduce revenue loss
### Project Overview
In this project we aim to build a classifier to predict whether a customer will ('soon') stop doing business with Syria Tel, a Telecommunications company. 
#### Objective
- Are churned customers more likely to have high or low usage
- The corelation between churn and other variables
 ## DATA UNDERSTANDING
 The dataset has 21 variables with a record of 3,333 records
 ### Import the libraries
- **Data manipulation** : pandas, numpy
- **Visualization** : matplotlib, seaborn
- **Machine learning** : sklearn for Decision Tree, evaluation, and preprocessing
- **Handling Imbalanced Data** : imblearn.SMOTE for oversampling minority classes

### Load the dataset
- The dataset is loaded using pd.read_csv().
- It is inspected using .head(), .tail(), .dtypes(), .columns(), .info(), .describe() to understand the data structure.
-    **<class 'pandas.core.frame.DataFrame'>
-     RangeIndex: 3333 entries, 0 to 3332
-     Data columns (total 21 columns):
-     #   Column                  Non-Null Count  Dtype  
-     ---  ------                  --------------  -----  
-     0   state                   3333 non-null   object 
-     1   account length          3333 non-null   int64  
-     2   area code               3333 non-null   int64  
-     3   phone number            3333 non-null   object 
-     4   international plan      3333 non-null   object 
-     5   voice mail plan         3333 non-null   object 
-     6   number vmail messages   3333 non-null   int64  
-     7   total day minutes       3333 non-null   float64
-     8   total day calls         3333 non-null   int64  
-     9   total day charge        3333 non-null   float64
-     10  total eve minutes       3333 non-null   float64
-     11  total eve calls         3333 non-null   int64  
-     12  total eve charge        3333 non-null   float64
-     13  total night minutes     3333 non-null   float64
-     14  total night calls       3333 non-null   int64  
-     15  total night charge      3333 non-null   float64
-     16  total intl minutes      3333 non-null   float64
-     17  total intl calls        3333 non-null   int64  
-     18  total intl charge       3333 non-null   float64
-     19  customer service calls  3333 non-null   int64  
-     20  churn                   3333 non-null   bool   
-     dtypes: bool(1), float64(8), int64(8), object(4)
-     memory usage: 524.2+ KB **
## DATA PREPARATION
### Data Cleaning
The dataset is clean with 0 missing values
The column names were separated by space, so we had to replace the spaces with underscore
