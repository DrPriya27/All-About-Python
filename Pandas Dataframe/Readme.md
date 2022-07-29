* Creating, Reading and Writing
https://www.kaggle.com/code/residentmario/creating-reading-and-writing/tutorial

* Ultimate Guide to Pandas Groupby & Aggregate
https://www.kaggle.com/code/akshaysehgal/ultimate-guide-to-pandas-groupby-aggregate/notebook

* 15 Pandas interview Questions for data Science
https://devenum.com/15-pandas-programs-interview-questions-on-data-filter/

* Easy Guide To Data Preprocessing In Python
https://www.kdnuggets.com/2020/07/easy-guide-data-preprocessing-python.html

* Data Preprocessing for Machine Learning
https://codesource.io/data-preprocessing-for-machine-learning/

* Data Clensing
https://www.kaggle.com/learn/data-cleaning
https://www.linkedin.com/posts/aleksandra-p%C5%82o%C5%84ska-42047432_automating-eda-machine-learning-activity-6954726851755790336-F18F/?utm_source=linkedin_share&utm_medium=android_app



* Data Science Hackathon Implementation
https://blog.devgenius.io/data-science-hackathon-implementation-25d07d5e5d56

* Hackathon-Experiments-With-Data-Analytics-Vidhya
https://github.com/anirudhjayaraman/Hackathon-Experiments-With-Data-Analytics-Vidhya/blob/master/Experiments%20with%20Data.ipynb

* Data wrangling Python
https://www.linkedin.com/posts/activity-6931211880719949824-HHKv/?utm_source=linkedin_share&utm_medium=android_app



```
### viewing the first few rows and last rows of the dataset
df.head()
df.tail()

### viewing statistical info about dataset
df.describe()
df.info()  #will print not-null values
df.shape

### print the values of dataset
df.values()

df.dropna()
x = df["col"].values
df["col"].value_counts()

### print the column index of dataset
df.columns

### print the row index of dataset
df.index
df.iloc[3,:]  #retrive row by "index" row label

### print missing values
df.isna().sum()
df.isna().any() #provides true and false
df.isnull().sum()
df.isna().sum().plot(kind="bar")

### sorting and subsetting
df.sort_values(["col1", "col2"], ascending = [True,False])
df[["col1", "col2"]] #subsetting multiple columns
cols_to_subset = ["col1", "col2"]
df[cols_to_subset]

df[df["col1"] > 50]      #subsetting rows
df[df["col1"] == "SampleString"]
df[(df["col1"] > 50]) & (df["col1"] == "SampleString"])]

df["col1"].isin(["Black","White"])    #subsetting using .isin()

### setting new columns
df["newCol"] = df["col1"] / 1000

### summary statistics
df["col1"].mean()   [.median(), .mode(), .min(), .max(), .var(), .std(), .sum(), .quantile(), .cumsum(), .cummax(), .cummin(), .cumprod()]
#.agg method

def pct30(column):
   return column.quantile(0.3)
df[["col1", "col2"]].agg(pct30)   

def pct40(column):
   retuen column.quantile(0.4)
df["col1"].agg([pct30, pct40])

### summarize categorical data
df.drop_duplicates(subset=["col1","col2"])
df["col1"].value_counts(sort=True)  #use normalize=True for normalizing value counts


### 
df.groupby("color")["weight"].mean()   #group by color column and take the mean on weight column
df.groupby(["color","breed"])[["weight","height"]].mean() 
df.groupby("color")["weight"].agg([min,max,sum]) 

### grouping by pivot table
df.pivot_table(values="weight", index="color", aggfunc=np.mean)  # by defaul it is np.mean
df.pivot_table(values="weight", index="color", aggfunc=[np.mean, np.median])
df.pivot_table(values="weight", index="color", columns="breed")  # for performing df.groupby(["color","breed"])[["weight","height"]].mean() 
df.pivot_table(values="weight", index="color", columns="breed",fill_value=0) # filling nan values with zero, other options are margins=True for producing total column
modified_df.mean(axis="index") #use axis="columns" for computing across columns

# Add a year column to temperatures
temperatures["year"] = temperatures["date"].dt.year

# Pivot avg_temp_c by country and city vs year
temp_by_country_city_vs_year = temperatures.pivot_table("avg_temp_c", index = ["country", "city"], columns = "year")

# See the result
print(temp_by_country_city_vs_year)


### explicit indexing rather than by row number
df.set_index["col1"]
df.reset_index()
df.reset_index(drop=True)  #entirely drop index column

modified_df.loc[["Black","White"]]  # use it in place of df["col1"].isin(["Black","White"]) after making col1 as an index. loc works on index column
df.set_index(["col1", "col2"])

# to subset inner levels with a list of tuples
modified_df.loc[[("aa","bb"),("cc","dd")]]  aa & cc is in col1 and bb && dd is in col2

modified_df.sort_index()
modified_df.sort_index(level=["color","breed"], ascending=[True, False])

### slicing and subsetting by .loc and .iloc
modified_df=df.set_index(["col1", "col2"]).sort_index()
modified_df.loc["name1":"name4"] # slicing the outer index level
modified_df.loc[("aa","bb"):("cc","dd")] # slicing the inner index level

modified_df.loc[:, "somecol":"fewmore"]  # slicing columns
modified_df.loc[("aa","bb"):("cc","dd"), "somecol":"fewmore"]

df.iloc[2:5,1:2] # slicing by iloc with index numbers

### visualization
import matplotlib.pyplot as plt
df["col1"].hist() #use bins=20 or something for chaning hist
plt.show()

# List the columns with missing values
cols_with_missing = ["small_sold", "large_sold", "xl_sold"]
# Create histograms showing the distributions cols_with_missing
avocados_2016[cols_with_missing].hist()   #three histogram will show up

# Show the plot
plt.show()

#bar plots
df.groupby("col1")["weight"].mean()
modified_df.plot(kind="bar",title="mean weight")
plt.show()

#line plots
df.plot(kind="line",x="date",y="weight")  #use rot=45 to rotate x-axis text
plt.show()

#scatter plots
df.plot(kind="scatter",x="date",y="weight")  
plt.show()

#to know which is categorical and which is continous
df.dtype #if object is there than it is categorical and when float64 and int that's a numerical feature

#number of unique values in each column
df.nunique()

#put everything in categorical and continous columns
[col for col in df.columns if df[col].dtype="object"]  #similarly do for another

#missing values across columns
df.isnull().sum(axis=0)

#to check for outlier (consider numerical columns only)
for col in numerical_cols:
   sns.boxplot(df[col])
   plt.show()
   
#if there is missing value so apply hard thresholding
df['col1'][df['col1']>0.2]=0.2  #do the same for testing

#look at correlation of target variable with all other numerical variables
train_df.corr()

#for categorical plot the count value by checking number of unique values are less than something  #UNIVARIATE PLOTS
for col in categorical_cols:
   if train_df[col].nunique() < 30:
      sns.countplot(train_df[col])
      plt.xticks[rotate=90]
      plt.show()

#BIVARIATE PLOTS
sns.scatterplot(x='',y='target', data=train_df)
#overlaying plots
df[df["sex"]=="F"]["height"].hist(alpha=0.7)  #alpha to make plots transparent
df[df["sex"]=="M"]["height"].hist(alpha=0.7)
plt.legand(["F","M"])
plt.show()

### dropping duplicate values
df = df.drop_duplicates()

### Dropping categorical data rows with missing values
df.drona()
df.dropna(how='any', subset=['Country', 'Purchased'], inplace=True)

df['col'].fillna(df['col'].mean(), inplace = True)  # fill test missing value also with this mean
#fill categorical missing values with mod

In the code above, for the parameter ‘how’, the argument ‘any’ drops the row if any value is null. But the argument ‘all’ will only drop the row if all the values are null. The argument for the ‘subset’ parameter is a list containing the columns we want to remove missing values from. ‘inplace=True’ modifies our original dataframe, instead of returning a copy of the dataframe.

### creating data frame
1) from list of dictionaries
eg = [
  {"name":"priya", "gender":F},...
  ]
df=pd.DataFrame(eg)

2) from dictionary of list
eg={
"name" ["priya","parv"],
}

### printing lenght of any text column
df['text'].str.len()

### printing word count 
df['text'].str.split().str.len()

## checking for specific keyword or digits count per row
df['text'].str.contains['start']  # will return true and false
df['text'].str.count(r'\d')
df['text'].str.finadall(r'\d')    #will return position of digits per row

## pull out hour and minutes from string
df['text'].str.findall(r'(\d?\d):(\d\d)')

## replace any instances of week day with three question marks
df['text'].str.replace(r'\w+day\b','???')

## using iterators to load large files into memory
specify chunksize in read_csv

for chunk in pd.read_csv('.csv', chunksize=1000):
   result.append(sum(chunk['col']))

df.duplicated().sum()

df.nunique()  #unique values in each column
for i in df.columns:
  print(df[i].unique())
  print(df[i].value_counts())
  
  plt.figure(figsize=(15,6))
  sns.countplot(df[i], data=df, palette='his')
  df[i].value_counts().plot(king='pie',autopct='   %1.1f%%')
  plt.xticks(rotation = 90)
  plt.show()
  
df.groupby(['year','quota']).size().plot(kind='line',color='purple')

df['col1'].mean(axis=0)
df['col1'].min()
df['col1'].max()
```






### impute missing values or drop
from sklearn.impute import SimpleImputer
imputer = SimpleImputer(fill_value=np.nan, startegy='mean')
X = imputer.fit_transform(df)
X = pd.DataFrame(X, columns=df.columns)

dropedDf = df.dropna()



### train test split
# Splitting dataset into independent & dependent variable
X = dataset[['Country', 'Age', 'Salary']].values
y = dataset['Purchased'].values

# replacing the missing values in the age & salary column with the mean
# import the SimpleImputer class from the sklearn library
from sklearn.impute import SimpleImputer
print(X[:, 1:3])

from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2)

### taking care of Categorical Features
from sklearn.preprocessing import LabelEncoder
l1 = LabelEncoder()
l1.fit(catDf['Country'].astype(str).values)
catDf.Country = l1.transform(catDf.Country)  #this is not inplace
print(catDf)

https://www.linkedin.com/posts/letthedataconfess_learning-pandas-activity-6953751472069107712-0nwN/?utm_source=linkedin_share&utm_medium=android_app

### convert categorical values in a dataframe to a one-hot vector
catDf = pd.get_dummies(data=catDf)
      
Using Sklearn
from sklearn.preprocessing import OneHotEncoder
oh = OneHotEncoder()
s1 = pd.DataFrame(oh.fit_transform(catDf.iloc[:, [0,3]]))
pd.concat([catDf, s1], axis=1)

# Handling Categorical Data
from sklearn.compose import ColumnTransformer
from sklearn.preprocessing import OneHotEncoder

ct = ColumnTransformer(transformers=[('enconder', OneHotEncoder(), [0])], remainder='passthrough')
X = np.array(ct.fit_transform(X))
print(X)

https://www.linkedin.com/posts/giannis-tolios_python-datascience-machinelearning-activity-6954853371191136256-TNyI/?utm_source=linkedin_share&utm_medium=android_app

In the ColumnTransformer class, for the argument ‘transformers’, we have a list containing a tuple as the parameter. The first item ‘encoder’ is the type of transformation we want. ‘OneHotEncoder()’ is the class that will handle the transformation. ‘[0]’ is the index of the column we want to encode. If we have multiple columns to transform, we can put them in the list. In this case, we only have one column with index 0, so it is only 0 that is in the list. The remainder=’passthrough’ means we want to leave the other columns the way they are without transforming them.

# Encoding the target variable
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
y = le.fit_transform(y)
print(y)

### Normalizing the Dataset
Standard scalar
x=catDF
z = (x.values - np.mean(x.values)) / np.std(x.values) 

from sklearn.preprocessing import StandardScaler
ss = StandardScaler()
catDf.iloc[:,1:-1] = ss.fit_transform(catDf.iloc[:,1:-1])
print(catDf)
print(catDf.var(ddof=0))

Ddof means Delta Degrees of Freedom, which is the divisor used in calculations is N - ddof, where N represents the number of elements. ddof=0 provides a maximum likelihood estimate of the variance for normally distributed variables.

Normalization:- the process of scaling individual samples to have unit norm.
from sklearn.preprocessing import Normalizer
norm = Normalizer()
catDf.iloc[:,1:-1] = norm.fit_transform(catDf.iloc[:,1:-1])
catDf

pd.read_csv()
pd.read_table()
pd.read_excel()
pd.read_sql()
pd.read_json()
pd.read_html()
pd.DataFrame()
pd.concat()
pd.series()
pd.data_range()

pd.fillna()
pd.apply()

pd.append()
pd.rename()

pd.join()
pd.to_csv()

pd.mean()
pd.median()
pd.count()
pd.std()
pd.max()
pd.min()








