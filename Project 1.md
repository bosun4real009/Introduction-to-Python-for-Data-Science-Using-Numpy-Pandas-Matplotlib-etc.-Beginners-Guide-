### Python is really a beautiful and amazing programming language.  It's really intuitive and in a simplified form for all who are committed to working with its vast libraries that makes execution of tasks simply

### I thought I've experienced it all with Python until i ventured into packages/libraries like numpy pandas, matplotlib, scipy, seaborn, scikit_learn etc. It opened me up to a whole new world. My excitement new no bounds as well as the possibility of what i can do with it. It gave me a whole new learning and practical experience

### This session contains my starting point trying out my learning and application of numpy and pandas libraries. And I'll upload more of it in subsequent sessions. The reading text that i used and will recommend asides other video courses was "Python for Data Analysis by Wes McKinney".

### Follow with the instructions and you can replicate all I've done and more

### Pandas supports loading and reading of files like excel, csv, html or from a database. Each of these requires its special command prompt or code

### First, you'll import the pandas library and you'll load the data, which is an excel file. Note that the command used is specifically for loading excel. To load other files require different command. The file is a dummy data from my end.


```python
import pandas as pd
file = pd.read_excel("Excursion Withdrawals.xls")
file.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Unnamed: 1</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>1</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>2</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Items</td>
      <td>Quantity</td>
      <td>Price</td>
      <td>Amount</td>
    </tr>
    <tr>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Departmental T-shirt</td>
      <td>NaN</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Accommodation ( Nnewi )</td>
      <td>NaN</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Feeding</td>
      <td>NaN</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
  </tbody>
</table>
</div>



### Note that the file can be loaded in such a way that most of the unwanted rows will be filtered out. But for now, we'll go about that in a counter intuitive manner

### The file has been loaded and .head() reads the first 10 lines of the data

### The first thing you should do after loading the data is to familiarize yourself with the data by getting several information about it. Examples of that is included below


```python
file.shape
```




    (16, 6)




```python
file.size
```




    96




```python
file.dtypes
```




    Unnamed: 0    float64
    Unnamed: 1    float64
    Unnamed: 2     object
    Unnamed: 3     object
    Unnamed: 4     object
    Unnamed: 5     object
    dtype: object




```python
file.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 16 entries, 0 to 15
    Data columns (total 6 columns):
    Unnamed: 0    0 non-null float64
    Unnamed: 1    0 non-null float64
    Unnamed: 2    12 non-null object
    Unnamed: 3    5 non-null object
    Unnamed: 4    11 non-null object
    Unnamed: 5    10 non-null object
    dtypes: float64(2), object(4)
    memory usage: 576.0+ bytes



```python
file.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Unnamed: 1</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>count</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <td>mean</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>std</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>min</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>25%</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>50%</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>75%</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <td>max</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



### Now, we'll drop i.e delete the unwanted rows. Note that i assigned the outcome to another variable. I can choose to retain the outcome in the same variable container by setting "inplace" to be True.


```python
file1 = file.drop([0,1,2,10,14,15])
```

### I checked the outcome of the action to know what the Dataset looks like and have a clue of what next to do


```python
file1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 0</th>
      <th>Unnamed: 1</th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Items</td>
      <td>Quantity</td>
      <td>Price</td>
      <td>Amount</td>
    </tr>
    <tr>
      <td>4</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Departmental T-shirt</td>
      <td>NaN</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Accommodation ( Nnewi )</td>
      <td>NaN</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Feeding</td>
      <td>NaN</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Fixing of Bus</td>
      <td>NaN</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>12</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>13</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Miscellaneous</td>
      <td>NaN</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>



### Next, i deleted some of the unwanted columns. Notice that i set "axis = 1" in the syntax and line of code below


```python
file2 = file1.drop(["Unnamed: 0","Unnamed: 1"], axis = 1)
```


```python
file2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Unnamed: 2</th>
      <th>Unnamed: 3</th>
      <th>Unnamed: 4</th>
      <th>Unnamed: 5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3</td>
      <td>Items</td>
      <td>Quantity</td>
      <td>Price</td>
      <td>Amount</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Departmental T-shirt</td>
      <td>NaN</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Accommodation ( Nnewi )</td>
      <td>NaN</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Feeding</td>
      <td>NaN</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Fixing of Bus</td>
      <td>NaN</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Miscellaneous</td>
      <td>NaN</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>



### Now, i renamed the columns of the dataset to make it more sensible and relatable


```python
file2.columns = ['ITEMS','QUANTITY', 'PRICE','AMOUNT']
```


```python
file2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ITEMS</th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3</td>
      <td>Items</td>
      <td>Quantity</td>
      <td>Price</td>
      <td>Amount</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Departmental T-shirt</td>
      <td>NaN</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Accommodation ( Nnewi )</td>
      <td>NaN</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Feeding</td>
      <td>NaN</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Fixing of Bus</td>
      <td>NaN</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Miscellaneous</td>
      <td>NaN</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>



### And again, I dropped another column that i found irrelevant in the dataset


```python
file3 = file2.drop(3)
```


```python
file3
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ITEMS</th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Departmental T-shirt</td>
      <td>NaN</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Accommodation ( Nnewi )</td>
      <td>NaN</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Feeding</td>
      <td>NaN</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Fixing of Bus</td>
      <td>NaN</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Miscellaneous</td>
      <td>NaN</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>




```python
file3.isna().sum()
```




    ITEMS       0
    QUANTITY    5
    PRICE       0
    AMOUNT      0
    dtype: int64



### There are some values in the Dataset that are "nan" which means not a number. It's been revealed that 5 null values are present in the quantity column. These values needs to be treated to make the Dataset clean. It's either you drop them or you correct them by replacing them with another value. There are many ways to go about this but in this case, it'll be replaced with a number using the fillna method


```python
file4 = file3.fillna(1)
```


```python
file4
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ITEMS</th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>6</td>
      <td>Departmental T-shirt</td>
      <td>1</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Accommodation ( Nnewi )</td>
      <td>1</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Feeding</td>
      <td>1</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Fixing of Bus</td>
      <td>1</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>13</td>
      <td>Miscellaneous</td>
      <td>1</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>




```python
link = list(file4["ITEMS"])
```


```python
link
```




    ['Fuelling of Coaster Bus',
     'Fuelling of Small Bus',
     'Departmental T-shirt',
     'Accommodation ( Nnewi )',
     'Feeding',
     'Renting Of Sound System',
     'Fixing of Bus',
     'Drivers',
     'Miscellaneous']



### I gave the dataset a new index label that's more befitting. And i deleted the column that i used


```python
file4.index = link
```


```python
file4
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>ITEMS</th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Fuelling of Coaster Bus</td>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>Fuelling of Small Bus</td>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>Departmental T-shirt</td>
      <td>Departmental T-shirt</td>
      <td>1</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>Accommodation ( Nnewi )</td>
      <td>Accommodation ( Nnewi )</td>
      <td>1</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>Feeding</td>
      <td>Feeding</td>
      <td>1</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>Renting Of Sound System</td>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>Fixing of Bus</td>
      <td>Fixing of Bus</td>
      <td>1</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>Drivers</td>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>Miscellaneous</td>
      <td>Miscellaneous</td>
      <td>1</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>




```python
file5 = file4.drop("ITEMS", axis = 1)
```


```python
file5
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Fuelling of Coaster Bus</td>
      <td>5</td>
      <td>13775</td>
      <td>68875</td>
    </tr>
    <tr>
      <td>Fuelling of Small Bus</td>
      <td>4</td>
      <td>10875</td>
      <td>43500</td>
    </tr>
    <tr>
      <td>Departmental T-shirt</td>
      <td>1</td>
      <td>40000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>Accommodation ( Nnewi )</td>
      <td>1</td>
      <td>32000</td>
      <td>32000</td>
    </tr>
    <tr>
      <td>Feeding</td>
      <td>1</td>
      <td>28000</td>
      <td>28000</td>
    </tr>
    <tr>
      <td>Renting Of Sound System</td>
      <td>4</td>
      <td>2000</td>
      <td>8000</td>
    </tr>
    <tr>
      <td>Fixing of Bus</td>
      <td>1</td>
      <td>25000</td>
      <td>25000</td>
    </tr>
    <tr>
      <td>Drivers</td>
      <td>4</td>
      <td>10000</td>
      <td>40000</td>
    </tr>
    <tr>
      <td>Miscellaneous</td>
      <td>1</td>
      <td>15000</td>
      <td>15000</td>
    </tr>
  </tbody>
</table>
</div>




```python
file5.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>count</td>
      <td>9.000000</td>
      <td>9.000000</td>
      <td>9.000000</td>
    </tr>
    <tr>
      <td>mean</td>
      <td>2.444444</td>
      <td>19627.777778</td>
      <td>33375.000000</td>
    </tr>
    <tr>
      <td>std</td>
      <td>1.740051</td>
      <td>12261.572623</td>
      <td>17793.959649</td>
    </tr>
    <tr>
      <td>min</td>
      <td>1.000000</td>
      <td>2000.000000</td>
      <td>8000.000000</td>
    </tr>
    <tr>
      <td>25%</td>
      <td>1.000000</td>
      <td>10875.000000</td>
      <td>25000.000000</td>
    </tr>
    <tr>
      <td>50%</td>
      <td>1.000000</td>
      <td>15000.000000</td>
      <td>32000.000000</td>
    </tr>
    <tr>
      <td>75%</td>
      <td>4.000000</td>
      <td>28000.000000</td>
      <td>40000.000000</td>
    </tr>
    <tr>
      <td>max</td>
      <td>5.000000</td>
      <td>40000.000000</td>
      <td>68875.000000</td>
    </tr>
  </tbody>
</table>
</div>



### The Dataset is now clean and ready for analysis. I just checked the Dataset with some methods to. confirm its new state. I checked its info,statistics, null values and data types. 


```python
file5.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Index: 9 entries, Fuelling of Coaster Bus to Miscellaneous
    Data columns (total 3 columns):
    QUANTITY    9 non-null int64
    PRICE       9 non-null int64
    AMOUNT      9 non-null int64
    dtypes: int64(3)
    memory usage: 252.0+ bytes



```python
file5.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>QUANTITY</th>
      <th>PRICE</th>
      <th>AMOUNT</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>count</td>
      <td>9.000000</td>
      <td>9.000000</td>
      <td>9.000000</td>
    </tr>
    <tr>
      <td>mean</td>
      <td>2.444444</td>
      <td>19627.777778</td>
      <td>33375.000000</td>
    </tr>
    <tr>
      <td>std</td>
      <td>1.740051</td>
      <td>12261.572623</td>
      <td>17793.959649</td>
    </tr>
    <tr>
      <td>min</td>
      <td>1.000000</td>
      <td>2000.000000</td>
      <td>8000.000000</td>
    </tr>
    <tr>
      <td>25%</td>
      <td>1.000000</td>
      <td>10875.000000</td>
      <td>25000.000000</td>
    </tr>
    <tr>
      <td>50%</td>
      <td>1.000000</td>
      <td>15000.000000</td>
      <td>32000.000000</td>
    </tr>
    <tr>
      <td>75%</td>
      <td>4.000000</td>
      <td>28000.000000</td>
      <td>40000.000000</td>
    </tr>
    <tr>
      <td>max</td>
      <td>5.000000</td>
      <td>40000.000000</td>
      <td>68875.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
file5.isnull().sum()
```




    QUANTITY    0
    PRICE       0
    AMOUNT      0
    dtype: int64




```python
file5.notnull().sum()
```




    QUANTITY    9
    PRICE       9
    AMOUNT      9
    dtype: int64




```python
file5.dtypes
```




    QUANTITY    int64
    PRICE       int64
    AMOUNT      int64
    dtype: object



### There are several ways and more efficient methods to get this done. This is majorly the basics. In subsequent lessons, you'll learn the advanced methods of data cleaning, data wrangling and data manipulation

### The best way to learn is by doing.  So practice with these basics and you'll learn advanced techniques in subsequent lessons. ♥️❣️♥️❣️♥️


```python

```
