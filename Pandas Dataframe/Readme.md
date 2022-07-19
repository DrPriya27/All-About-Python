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

* Data Science Hackathon Implementation
https://blog.devgenius.io/data-science-hackathon-implementation-25d07d5e5d56

* Hackathon-Experiments-With-Data-Analytics-Vidhya
https://github.com/anirudhjayaraman/Hackathon-Experiments-With-Data-Analytics-Vidhya/blob/master/Experiments%20with%20Data.ipynb

* Data wrangling Python
https://www.linkedin.com/posts/activity-6931211880719949824-HHKv/?utm_source=linkedin_share&utm_medium=android_app


```
### viewing the first few rows of the dataset
df.head()

### viewing statistical info about dataset
df.describe()

df.info()
df.shape

### print the values of dataset
df.values()

### print the column index of dataset
df.columns

### print the row index of dataset
df.index

### print missing values
df.isna().sum()
df.isnull().sum()

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
 
```


### Dropping categorical data rows with missing values
dataset.dropna(how='any', subset=['Country', 'Purchased'], inplace=True)

In the code above, for the parameter ‘how’, the argument ‘any’ drops the row if any value is null. But the argument ‘all’ will only drop the row if all the values are null. The argument for the ‘subset’ parameter is a list containing the columns we want to remove missing values from. ‘inplace=True’ modifies our original dataframe, instead of returning a copy of the dataframe.

### dropping duplicate values
dataset = dataset.drop_duplicates()


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
l1.fit(catDf['Country'])
catDf.Country = l1.transform(catDf.Country)  #this is not inplace
print(catDf)

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
pd.sort_values()
pd.append()
pd.rename()
pd.groupby()
pd.join()
pd.to_csv()
pd.set_index()

pd.tail()
pd.info()
pd.mean()
pd.median()
pd.count()
pd.std()
pd.max()
pd.min()








