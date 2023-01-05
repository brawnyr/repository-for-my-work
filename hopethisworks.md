![weenie](https://user-images.githubusercontent.com/94146962/210137703-e2da8d5e-c315-4c89-aba7-af2aa6a9c17b.gif)

 # The purpose of this project is to draw insight from a dog breed characteristic dataset.

### We will be using the pandas library to examine this dataset.


```python
import pandas as pd
```

Now we will create a dataframe from our dataset which is in csv format.
*dogc = name of dataframe


```python
dogc = pd.read_csv('https://github.com/brawnyr/repository-for-my-work/blob/cc0505de25d6d56895d1bbf868fe21d49a072f06/dog.csv?raw=true')
dogc
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
      <th>Breed</th>
      <th>Affectionate With Family</th>
      <th>Good With Young Children</th>
      <th>Good With Other Dogs</th>
      <th>Shedding Level</th>
      <th>Coat Grooming Frequency</th>
      <th>Drooling Level</th>
      <th>Coat Type</th>
      <th>Coat Length</th>
      <th>Openness To Strangers</th>
      <th>Playfulness Level</th>
      <th>Watchdog/Protective Nature</th>
      <th>Adaptability Level</th>
      <th>Trainability Level</th>
      <th>Energy Level</th>
      <th>Barking Level</th>
      <th>Mental Stimulation Needs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Retrievers (Labrador)</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>Double</td>
      <td>Short</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>1</th>
      <td>French Bulldogs</td>
      <td>5</td>
      <td>5</td>
      <td>4</td>
      <td>3</td>
      <td>1</td>
      <td>3</td>
      <td>Smooth</td>
      <td>Short</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>5</td>
      <td>4</td>
      <td>3</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>German Shepherd Dogs</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>Double</td>
      <td>Medium</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>5</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Retrievers (Golden)</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>4</td>
      <td>2</td>
      <td>2</td>
      <td>Double</td>
      <td>Medium</td>
      <td>5</td>
      <td>4</td>
      <td>3</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>1</td>
      <td>4</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Bulldogs</td>
      <td>4</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>Smooth</td>
      <td>Short</td>
      <td>4</td>
      <td>4</td>
      <td>3</td>
      <td>3</td>
      <td>4</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>190</th>
      <td>Cesky Terriers</td>
      <td>4</td>
      <td>5</td>
      <td>3</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>Wavy</td>
      <td>Medium</td>
      <td>4</td>
      <td>3</td>
      <td>3</td>
      <td>4</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
    <tr>
      <th>191</th>
      <td>American Foxhounds</td>
      <td>3</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>Smooth</td>
      <td>Short</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>3</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Azawakhs</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>2</td>
      <td>1</td>
      <td>Smooth</td>
      <td>Short</td>
      <td>1</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>3</td>
      <td>1</td>
      <td>3</td>
    </tr>
    <tr>
      <th>193</th>
      <td>English Foxhounds</td>
      <td>5</td>
      <td>5</td>
      <td>5</td>
      <td>3</td>
      <td>1</td>
      <td>2</td>
      <td>Double</td>
      <td>Short</td>
      <td>4</td>
      <td>4</td>
      <td>3</td>
      <td>4</td>
      <td>4</td>
      <td>4</td>
      <td>5</td>
      <td>4</td>
    </tr>
    <tr>
      <th>194</th>
      <td>Norwegian Lundehunds</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>2</td>
      <td>1</td>
      <td>Double</td>
      <td>Short</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
      <td>3</td>
    </tr>
  </tbody>
</table>
<p>195 rows × 17 columns</p>
</div>




```python
dogc.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 195 entries, 0 to 194
    Data columns (total 17 columns):
     #   Column                      Non-Null Count  Dtype 
    ---  ------                      --------------  ----- 
     0   Breed                       195 non-null    object
     1   Affectionate With Family    195 non-null    int64 
     2   Good With Young Children    195 non-null    int64 
     3   Good With Other Dogs        195 non-null    int64 
     4   Shedding Level              195 non-null    int64 
     5   Coat Grooming Frequency     195 non-null    int64 
     6   Drooling Level              195 non-null    int64 
     7   Coat Type                   195 non-null    object
     8   Coat Length                 195 non-null    object
     9   Openness To Strangers       195 non-null    int64 
     10  Playfulness Level           195 non-null    int64 
     11  Watchdog/Protective Nature  195 non-null    int64 
     12  Adaptability Level          195 non-null    int64 
     13  Trainability Level          195 non-null    int64 
     14  Energy Level                195 non-null    int64 
     15  Barking Level               195 non-null    int64 
     16  Mental Stimulation Needs    195 non-null    int64 
    dtypes: int64(14), object(3)
    memory usage: 26.0+ KB

