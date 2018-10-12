

```python
import pandas
df = pandas.read_csv('content_watch.csv')
```


```python
df.head()
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
      <th>57041</th>
      <th>None</th>
      <th>1375049758</th>
      <th>3180</th>
      <th>2018-03-24T15:23:42.000+03:00</th>
      <th>Web</th>
      <th>Таджикистан</th>
      <th>Khujand</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>1320</td>
      <td>2018-03-24T17:18:22.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>1</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>5223</td>
      <td>2018-03-24T13:40:52.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>2</th>
      <td>164367</td>
      <td>None</td>
      <td>-1975523248</td>
      <td>5057</td>
      <td>2018-03-27T15:10:23.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>3</th>
      <td>133756</td>
      <td>None</td>
      <td>1669448250</td>
      <td>168</td>
      <td>2018-03-25T18:28:56.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>4</th>
      <td>196380</td>
      <td>9714</td>
      <td>2146511241</td>
      <td>1203</td>
      <td>2018-03-28T04:40:21.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.columns = ['Content_id', 'Comp_id', 'User_id', 'Duration', 'time', 'platform', 'country', 'place']
```


```python
df.head()
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>1320</td>
      <td>2018-03-24T17:18:22.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>1</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>5223</td>
      <td>2018-03-24T13:40:52.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>2</th>
      <td>164367</td>
      <td>None</td>
      <td>-1975523248</td>
      <td>5057</td>
      <td>2018-03-27T15:10:23.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>3</th>
      <td>133756</td>
      <td>None</td>
      <td>1669448250</td>
      <td>168</td>
      <td>2018-03-25T18:28:56.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>4</th>
      <td>196380</td>
      <td>9714</td>
      <td>2146511241</td>
      <td>1203</td>
      <td>2018-03-28T04:40:21.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
  </tbody>
</table>
</div>




```python
df = df.drop(columns="User_id")
```


```python
df.head()
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>57041</td>
      <td>None</td>
      <td>1320</td>
      <td>2018-03-24T17:18:22.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>1</th>
      <td>57041</td>
      <td>None</td>
      <td>5223</td>
      <td>2018-03-24T13:40:52.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>2</th>
      <td>164367</td>
      <td>None</td>
      <td>5057</td>
      <td>2018-03-27T15:10:23.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>3</th>
      <td>133756</td>
      <td>None</td>
      <td>168</td>
      <td>2018-03-25T18:28:56.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>4</th>
      <td>196380</td>
      <td>9714</td>
      <td>1203</td>
      <td>2018-03-28T04:40:21.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
  </tbody>
</table>
</div>




```python
country = df['country'].value_counts()
```


```python
city = df['place'].value_counts()
```


```python
city.head()
```




    Moscow              7794400
    Saint Petersburg    2994114
    Krasnodar           1322524
    Yekaterinburg       1255552
    Novosibirsk         1190039
    Name: place, dtype: int64




```python
platform = df['platform'].value_counts()
```


```python
platform
```




    STB           39556779
    Web           12134217
    Mobile         6251537
    Web-Mobile     3336471
    Name: platform, dtype: int64




```python
Duration = df.sort_values(by='Duration', ascending=False)
```


```python
Duration.head(n=20)
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>7457819</th>
      <td>124111</td>
      <td>9534</td>
      <td>-1203352073</td>
      <td>1036910</td>
      <td>2018-03-29T17:07:55.000+03:00</td>
      <td>Mobile</td>
      <td>Казахстан</td>
      <td>Almaty</td>
    </tr>
    <tr>
      <th>15663478</th>
      <td>161608</td>
      <td>10213</td>
      <td>823009459</td>
      <td>928787</td>
      <td>2018-03-31T08:17:45.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Novosibirsk</td>
    </tr>
    <tr>
      <th>59372130</th>
      <td>191616</td>
      <td>10809</td>
      <td>1847715014</td>
      <td>179703</td>
      <td>2018-03-29T12:27:13.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Voronezh</td>
    </tr>
    <tr>
      <th>20529080</th>
      <td>10310</td>
      <td>7177</td>
      <td>-1369396608</td>
      <td>174828</td>
      <td>2018-03-24T21:58:50.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Ulyanovsk</td>
    </tr>
    <tr>
      <th>41042262</th>
      <td>45788</td>
      <td>None</td>
      <td>-1139308625</td>
      <td>94265</td>
      <td>2018-03-25T20:05:50.000+03:00</td>
      <td>Mobile</td>
      <td>Украина</td>
      <td>Pavlograd</td>
    </tr>
    <tr>
      <th>21756047</th>
      <td>185376</td>
      <td>9570</td>
      <td>141355555</td>
      <td>89233</td>
      <td>2018-03-30T00:28:29.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Belgorod</td>
    </tr>
    <tr>
      <th>27624739</th>
      <td>120567</td>
      <td>9475</td>
      <td>1990411591</td>
      <td>83559</td>
      <td>2018-03-27T16:29:17.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Irbit</td>
    </tr>
    <tr>
      <th>39216443</th>
      <td>191571</td>
      <td>10856</td>
      <td>1831347179</td>
      <td>78750</td>
      <td>2018-03-26T21:04:17.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Беларусь</td>
      <td>Gomel</td>
    </tr>
    <tr>
      <th>15695181</th>
      <td>209256</td>
      <td>11209</td>
      <td>1144983030</td>
      <td>77669</td>
      <td>2018-03-31T12:51:38.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Novosibirsk</td>
    </tr>
    <tr>
      <th>35126731</th>
      <td>51621</td>
      <td>None</td>
      <td>-1241399821</td>
      <td>76316</td>
      <td>2018-03-24T08:25:28.000+03:00</td>
      <td>Mobile</td>
      <td>Казахстан</td>
      <td>Казахстан</td>
    </tr>
    <tr>
      <th>174991</th>
      <td>97759</td>
      <td>7097</td>
      <td>224047458</td>
      <td>74870</td>
      <td>2018-03-30T17:54:07.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Zhukovskiy</td>
    </tr>
    <tr>
      <th>50657710</th>
      <td>197706</td>
      <td>11083</td>
      <td>499245990</td>
      <td>73948</td>
      <td>2018-03-25T14:48:34.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Orenburg</td>
    </tr>
    <tr>
      <th>29111902</th>
      <td>199146</td>
      <td>11160</td>
      <td>-1095050823</td>
      <td>73825</td>
      <td>2018-03-29T20:47:26.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Россия</td>
      <td>Taman</td>
    </tr>
    <tr>
      <th>41049704</th>
      <td>131255</td>
      <td>None</td>
      <td>-1784918468</td>
      <td>66423</td>
      <td>2018-03-28T11:52:22.000+03:00</td>
      <td>Web</td>
      <td>Украина</td>
      <td>Pavlograd</td>
    </tr>
    <tr>
      <th>41045936</th>
      <td>103900</td>
      <td>9258</td>
      <td>-1784918468</td>
      <td>56099</td>
      <td>2018-03-24T10:49:09.000+03:00</td>
      <td>Web</td>
      <td>Украина</td>
      <td>Pavlograd</td>
    </tr>
    <tr>
      <th>20484162</th>
      <td>178167</td>
      <td>10553</td>
      <td>1696274649</td>
      <td>55451</td>
      <td>2018-03-30T06:58:09.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Ulyanovsk</td>
    </tr>
    <tr>
      <th>18271460</th>
      <td>181681</td>
      <td>10618</td>
      <td>1958682334</td>
      <td>47816</td>
      <td>2018-03-29T00:37:56.000+03:00</td>
      <td>STB</td>
      <td>Германия</td>
      <td>Berlin</td>
    </tr>
    <tr>
      <th>18271472</th>
      <td>181680</td>
      <td>10618</td>
      <td>1958682334</td>
      <td>47503</td>
      <td>2018-03-29T00:18:30.000+03:00</td>
      <td>STB</td>
      <td>Германия</td>
      <td>Berlin</td>
    </tr>
    <tr>
      <th>20111861</th>
      <td>187193</td>
      <td>10274</td>
      <td>-1252915675</td>
      <td>46523</td>
      <td>2018-03-26T06:25:12.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Shira</td>
    </tr>
    <tr>
      <th>24265135</th>
      <td>166959</td>
      <td>None</td>
      <td>42</td>
      <td>46115</td>
      <td>2018-03-30T19:09:20.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Vilino</td>
    </tr>
  </tbody>
</table>
</div>




```python
df['country'].value_counts().reset_index().to_csv('country.csv')
```


```python
df['platform'].value_counts().reset_index().to_csv('platform.csv')
```


```python
df['place'].value_counts().reset_index().to_csv('city.csv')
```


```python
df.head(n=10)
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>1320</td>
      <td>2018-03-24T17:18:22.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>1</th>
      <td>57041</td>
      <td>None</td>
      <td>1375049758</td>
      <td>5223</td>
      <td>2018-03-24T13:40:52.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>2</th>
      <td>164367</td>
      <td>None</td>
      <td>-1975523248</td>
      <td>5057</td>
      <td>2018-03-27T15:10:23.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>3</th>
      <td>133756</td>
      <td>None</td>
      <td>1669448250</td>
      <td>168</td>
      <td>2018-03-25T18:28:56.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>4</th>
      <td>196380</td>
      <td>9714</td>
      <td>2146511241</td>
      <td>1203</td>
      <td>2018-03-28T04:40:21.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>5</th>
      <td>196380</td>
      <td>9714</td>
      <td>2146511241</td>
      <td>302</td>
      <td>2018-03-28T04:11:41.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>6</th>
      <td>196380</td>
      <td>9714</td>
      <td>2146511241</td>
      <td>434</td>
      <td>2018-03-28T04:25:21.000+03:00</td>
      <td>Web-Mobile</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>7</th>
      <td>2828</td>
      <td>None</td>
      <td>-376570852</td>
      <td>420</td>
      <td>2018-03-28T08:16:26.000+03:00</td>
      <td>Web</td>
      <td>Таджикистан</td>
      <td>Khujand</td>
    </tr>
    <tr>
      <th>8</th>
      <td>147659</td>
      <td>9991</td>
      <td>-522928405</td>
      <td>208</td>
      <td>2018-03-30T10:39:28.000+03:00</td>
      <td>Mobile</td>
      <td>Хорватия</td>
      <td>Pula</td>
    </tr>
    <tr>
      <th>9</th>
      <td>117484</td>
      <td>9412</td>
      <td>526076719</td>
      <td>2615</td>
      <td>2018-03-31T14:30:56.000+03:00</td>
      <td>STB</td>
      <td>Испания</td>
      <td>Torrelavega</td>
    </tr>
  </tbody>
</table>
</div>




```python
dur = df[df.Duration > 36000]
```


```python
dur.to_csv('dur.csv')
```


```python
dur['country'].value_counts().reset_index().to_csv('countryTop.csv')
```


```python
dur['platform'].value_counts().reset_index().to_csv('platformTop.csv')
```


```python
dur['place'].value_counts().reset_index().to_csv('cityTop.csv')
```


```python
dur['Comp_id'].value_counts()
```




    None     11
    10080     8
    10618     2
    10582     2
    7894      2
    9534      1
    7097      1
    9795      1
    10274     1
    6793      1
    10553     1
    11532     1
    11263     1
    9570      1
    11160     1
    11209     1
    11083     1
    9258      1
    7177      1
    10856     1
    9295      1
    7566      1
    10809     1
    9475      1
    8575      1
    10213     1
    Name: Comp_id, dtype: int64




```python
dur['Comp_id'].value_counts().reset_index().to_csv('contentTop.csv')
```


```python
country1 = df.sort_values(by="country", ascending = False)
```


```python
country1.head()
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9859753</th>
      <td>197731</td>
      <td>11086</td>
      <td>816946130</td>
      <td>1346</td>
      <td>2018-03-25T04:35:58.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Tokyo</td>
    </tr>
    <tr>
      <th>23536995</th>
      <td>94068</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>363</td>
      <td>2018-03-27T11:47:48.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>14504408</th>
      <td>157376</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>325</td>
      <td>2018-03-31T13:33:07.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504410</th>
      <td>186040</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T15:18:01.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504411</th>
      <td>157378</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T13:44:36.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
  </tbody>
</table>
</div>




```python
country11 = country1.head(n=133)
```


```python
country11
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9859753</th>
      <td>197731</td>
      <td>11086</td>
      <td>816946130</td>
      <td>1346</td>
      <td>2018-03-25T04:35:58.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Tokyo</td>
    </tr>
    <tr>
      <th>23536995</th>
      <td>94068</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>363</td>
      <td>2018-03-27T11:47:48.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>14504408</th>
      <td>157376</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>325</td>
      <td>2018-03-31T13:33:07.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504410</th>
      <td>186040</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T15:18:01.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504411</th>
      <td>157378</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T13:44:36.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504412</th>
      <td>157385</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:25:23.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504413</th>
      <td>174455</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T15:00:30.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504414</th>
      <td>157388</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:43:00.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504415</th>
      <td>157386</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:37:09.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>23537007</th>
      <td>94059</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>360</td>
      <td>2018-03-27T10:57:30.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>14504409</th>
      <td>157377</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>310</td>
      <td>2018-03-31T13:38:58.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>36683975</th>
      <td>127422</td>
      <td>9572</td>
      <td>-356510659</td>
      <td>2400</td>
      <td>2018-03-30T07:58:14.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Miura</td>
    </tr>
    <tr>
      <th>36683976</th>
      <td>133250</td>
      <td>None</td>
      <td>-356510659</td>
      <td>720</td>
      <td>2018-03-30T08:39:10.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Miura</td>
    </tr>
    <tr>
      <th>36683977</th>
      <td>115686</td>
      <td>None</td>
      <td>-356510659</td>
      <td>3240</td>
      <td>2018-03-30T07:02:44.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Miura</td>
    </tr>
    <tr>
      <th>23536993</th>
      <td>94065</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>364</td>
      <td>2018-03-27T12:00:22.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23536994</th>
      <td>94060</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>357</td>
      <td>2018-03-27T10:45:04.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23536996</th>
      <td>94055</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>364</td>
      <td>2018-03-27T13:02:35.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>14504407</th>
      <td>185711</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T15:12:09.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>23536997</th>
      <td>94056</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>360</td>
      <td>2018-03-27T13:15:08.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>1348195</th>
      <td>130457</td>
      <td>None</td>
      <td>1865470273</td>
      <td>281</td>
      <td>2018-03-25T08:43:04.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Tatebayashi</td>
    </tr>
    <tr>
      <th>1348196</th>
      <td>130457</td>
      <td>None</td>
      <td>1865470273</td>
      <td>219</td>
      <td>2018-03-25T08:49:59.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Tatebayashi</td>
    </tr>
    <tr>
      <th>23536998</th>
      <td>94053</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>359</td>
      <td>2018-03-27T13:21:24.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23536999</th>
      <td>94054</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>363</td>
      <td>2018-03-27T13:08:50.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537000</th>
      <td>94046</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>18141</td>
      <td>2018-03-27T13:34:02.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537001</th>
      <td>94052</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>362</td>
      <td>2018-03-27T13:27:44.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537002</th>
      <td>94058</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>358</td>
      <td>2018-03-27T12:50:12.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537003</th>
      <td>94061</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>357</td>
      <td>2018-03-27T12:37:48.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537004</th>
      <td>94062</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>361</td>
      <td>2018-03-27T10:38:47.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537005</th>
      <td>94057</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>359</td>
      <td>2018-03-27T11:10:01.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>23537006</th>
      <td>94069</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>357</td>
      <td>2018-03-27T09:54:58.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
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
    </tr>
    <tr>
      <th>7229152</th>
      <td>122627</td>
      <td>None</td>
      <td>-564124954</td>
      <td>4095</td>
      <td>2018-03-25T16:39:40.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>2702000</th>
      <td>133538</td>
      <td>None</td>
      <td>524833058</td>
      <td>1800</td>
      <td>2018-03-25T14:49:47.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kyoto</td>
    </tr>
    <tr>
      <th>209377</th>
      <td>203507</td>
      <td>11253</td>
      <td>1052460214</td>
      <td>2761</td>
      <td>2018-03-29T16:32:49.000+03:00</td>
      <td>Web</td>
      <td>Япония</td>
      <td>Osaka</td>
    </tr>
    <tr>
      <th>2701999</th>
      <td>127422</td>
      <td>9572</td>
      <td>-568388210</td>
      <td>360</td>
      <td>2018-03-27T00:51:06.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Kyoto</td>
    </tr>
    <tr>
      <th>2701998</th>
      <td>212394</td>
      <td>11556</td>
      <td>-568388210</td>
      <td>3049</td>
      <td>2018-03-30T03:18:36.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Kyoto</td>
    </tr>
    <tr>
      <th>2701997</th>
      <td>212392</td>
      <td>11556</td>
      <td>-568388210</td>
      <td>2109</td>
      <td>2018-03-29T14:25:53.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Kyoto</td>
    </tr>
    <tr>
      <th>2701996</th>
      <td>212393</td>
      <td>11556</td>
      <td>-568388210</td>
      <td>3021</td>
      <td>2018-03-29T15:01:24.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Kyoto</td>
    </tr>
    <tr>
      <th>24804861</th>
      <td>161826</td>
      <td>None</td>
      <td>719945288</td>
      <td>3844</td>
      <td>2018-03-28T16:18:34.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Toyama</td>
    </tr>
    <tr>
      <th>24804860</th>
      <td>176658</td>
      <td>None</td>
      <td>719945288</td>
      <td>213</td>
      <td>2018-03-27T16:26:14.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Toyama</td>
    </tr>
    <tr>
      <th>7229144</th>
      <td>211539</td>
      <td>11529</td>
      <td>659025730</td>
      <td>2995</td>
      <td>2018-03-31T13:36:18.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>7229146</th>
      <td>211538</td>
      <td>11529</td>
      <td>659025730</td>
      <td>2877</td>
      <td>2018-03-31T12:46:37.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>7229147</th>
      <td>155014</td>
      <td>None</td>
      <td>659025730</td>
      <td>1589</td>
      <td>2018-03-31T15:38:20.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>7229148</th>
      <td>211537</td>
      <td>11529</td>
      <td>659025730</td>
      <td>3077</td>
      <td>2018-03-31T11:50:47.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>7229149</th>
      <td>45788</td>
      <td>None</td>
      <td>-564124954</td>
      <td>4250</td>
      <td>2018-03-25T18:54:41.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>7229150</th>
      <td>107203</td>
      <td>None</td>
      <td>-564124954</td>
      <td>3815</td>
      <td>2018-03-25T17:50:15.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>9859730</th>
      <td>2538</td>
      <td>7305</td>
      <td>816946130</td>
      <td>660</td>
      <td>2018-03-24T10:05:37.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Tokyo</td>
    </tr>
    <tr>
      <th>24804858</th>
      <td>59441</td>
      <td>8127</td>
      <td>-40071551</td>
      <td>2940</td>
      <td>2018-03-24T02:04:10.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Toyama</td>
    </tr>
    <tr>
      <th>7229151</th>
      <td>33529</td>
      <td>None</td>
      <td>-564124954</td>
      <td>4395</td>
      <td>2018-03-25T21:48:08.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>14504398</th>
      <td>174454</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:54:42.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504397</th>
      <td>172382</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:48:51.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504402</th>
      <td>174456</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T15:06:20.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>7229153</th>
      <td>33558</td>
      <td>None</td>
      <td>-564124954</td>
      <td>4405</td>
      <td>2018-03-25T20:06:28.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Takarazuka</td>
    </tr>
    <tr>
      <th>24804859</th>
      <td>59440</td>
      <td>8127</td>
      <td>-40071551</td>
      <td>480</td>
      <td>2018-03-24T02:53:41.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Toyama</td>
    </tr>
    <tr>
      <th>14504403</th>
      <td>157383</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:13:43.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>59986247</th>
      <td>116794</td>
      <td>7312</td>
      <td>1846567800</td>
      <td>397</td>
      <td>2018-03-27T03:46:37.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kobe</td>
    </tr>
    <tr>
      <th>59986248</th>
      <td>43853</td>
      <td>7312</td>
      <td>1846567800</td>
      <td>413</td>
      <td>2018-03-27T03:38:04.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kobe</td>
    </tr>
    <tr>
      <th>55473085</th>
      <td>99774</td>
      <td>None</td>
      <td>-261496287</td>
      <td>1243</td>
      <td>2018-03-30T16:35:20.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Otsu</td>
    </tr>
    <tr>
      <th>55473084</th>
      <td>74864</td>
      <td>None</td>
      <td>-261496287</td>
      <td>1260</td>
      <td>2018-03-30T16:57:41.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Otsu</td>
    </tr>
    <tr>
      <th>21619671</th>
      <td>170530</td>
      <td>10367</td>
      <td>-21786224</td>
      <td>340</td>
      <td>2018-03-30T14:02:38.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Fukuoka</td>
    </tr>
    <tr>
      <th>14504399</th>
      <td>157387</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:31:17.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
  </tbody>
</table>
<p>133 rows × 8 columns</p>
</div>




```python
country11['Duration'].value_counts().reset_index().to_csv('Japan.csv')
```


```python
country11.head(n=10)
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>9859753</th>
      <td>197731</td>
      <td>11086</td>
      <td>816946130</td>
      <td>1346</td>
      <td>2018-03-25T04:35:58.000+03:00</td>
      <td>Mobile</td>
      <td>Япония</td>
      <td>Tokyo</td>
    </tr>
    <tr>
      <th>23536995</th>
      <td>94068</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>363</td>
      <td>2018-03-27T11:47:48.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
    <tr>
      <th>14504408</th>
      <td>157376</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>325</td>
      <td>2018-03-31T13:33:07.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504410</th>
      <td>186040</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T15:18:01.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504411</th>
      <td>157378</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T13:44:36.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504412</th>
      <td>157385</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:25:23.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504413</th>
      <td>174455</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>320</td>
      <td>2018-03-31T15:00:30.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504414</th>
      <td>157388</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:43:00.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>14504415</th>
      <td>157386</td>
      <td>10117</td>
      <td>1601937250</td>
      <td>340</td>
      <td>2018-03-31T14:37:09.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Yokohama</td>
    </tr>
    <tr>
      <th>23537007</th>
      <td>94059</td>
      <td>9092</td>
      <td>-1954159900</td>
      <td>360</td>
      <td>2018-03-27T10:57:30.000+03:00</td>
      <td>STB</td>
      <td>Япония</td>
      <td>Kanazawa</td>
    </tr>
  </tbody>
</table>
</div>




```python
country11['platform'].value_counts().reset_index().to_csv('platformTopJapan.csv')
```


```python
countryRus = country1[3151013:55815916]
```


```python
countryRus.head()
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3575497</th>
      <td>157267</td>
      <td>10115</td>
      <td>42</td>
      <td>23820</td>
      <td>2018-03-24T00:53:39.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Kursk</td>
    </tr>
    <tr>
      <th>3575516</th>
      <td>205922</td>
      <td>10274</td>
      <td>148967003</td>
      <td>302</td>
      <td>2018-03-24T20:09:55.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
    </tr>
    <tr>
      <th>3575509</th>
      <td>203503</td>
      <td>11251</td>
      <td>1976986390</td>
      <td>3075</td>
      <td>2018-03-24T00:02:58.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Kursk</td>
    </tr>
    <tr>
      <th>3575474</th>
      <td>65895</td>
      <td>8295</td>
      <td>633681963</td>
      <td>296</td>
      <td>2018-03-24T20:07:33.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Kursk</td>
    </tr>
    <tr>
      <th>3575510</th>
      <td>133822</td>
      <td>None</td>
      <td>1574207885</td>
      <td>1065</td>
      <td>2018-03-24T11:19:10.000+03:00</td>
      <td>STB</td>
      <td>Россия</td>
      <td>Kursk</td>
    </tr>
  </tbody>
</table>
</div>




```python
countryRus.loc['sum'] = countryRus.Duration.sum()
```

    /anaconda3/lib/python3.6/site-packages/ipykernel_launcher.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame
    
    See the caveats in the documentation: http://pandas.pydata.org/pandas-docs/stable/indexing.html#indexing-view-versus-copy
      """Entry point for launching an IPython kernel.



```python
countryRus['platform'].value_counts().reset_index().to_csv('platformTopRus.csv')
```


```python
countryRus['place'].value_counts().reset_index().to_csv('cityTopRus.csv')
```


```python
countryRus['Comp_id'].value_counts().reset_index().to_csv('contentTopRus.csv')
```


```python
DurationRus = countryRus.sort_values(by='Duration', ascending=False)
```


```python
DarationRus15 = DurationRus.head(n=15)
```


```python
DarationRus15.to_csv('DarationRus15.csv')
```


```python
countryRus["Duration"].mean()
```




    2700.2015349349163




```python
countryRus["Duration"].sum()
```




    142205854618




```python
filteredRusMob = countryRus[countryRus.platform == 'Mobile']
```


```python
filteredRusMob.head()
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
      <th>Content_id</th>
      <th>Comp_id</th>
      <th>User_id</th>
      <th>Duration</th>
      <th>time</th>
      <th>platform</th>
      <th>country</th>
      <th>place</th>
      <th>sum</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3575516</th>
      <td>205922</td>
      <td>10274</td>
      <td>148967003</td>
      <td>302</td>
      <td>2018-03-24T20:09:55.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
      <td>71102927309</td>
    </tr>
    <tr>
      <th>3575475</th>
      <td>161675</td>
      <td>10209</td>
      <td>42</td>
      <td>1380</td>
      <td>2018-03-24T19:47:07.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
      <td>71102927309</td>
    </tr>
    <tr>
      <th>3575350</th>
      <td>206937</td>
      <td>11389</td>
      <td>-975580002</td>
      <td>1260</td>
      <td>2018-03-24T11:17:03.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
      <td>71102927309</td>
    </tr>
    <tr>
      <th>3575340</th>
      <td>158759</td>
      <td>None</td>
      <td>-1981369534</td>
      <td>1260</td>
      <td>2018-03-24T19:59:49.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
      <td>71102927309</td>
    </tr>
    <tr>
      <th>3575339</th>
      <td>140433</td>
      <td>9794</td>
      <td>966869975</td>
      <td>1279</td>
      <td>2018-03-24T04:52:01.000+03:00</td>
      <td>Mobile</td>
      <td>Россия</td>
      <td>Kursk</td>
      <td>71102927309</td>
    </tr>
  </tbody>
</table>
</div>




```python
filteredRusMob["Duration"].sum()
```




    7542640585




```python
filteredRusSTB = countryRus[countryRus.platform == 'STB']
```


```python
filteredRusSTB["Duration"].sum()
```




    38743094593




```python
filteredRusWeb = countryRus[countryRus.platform == 'Web']
```


```python
filteredRusWeb["Duration"].sum()
```




    20396879511




```python
filteredRusWebmob = countryRus[countryRus.platform == 'Web-Mobile']
```


```python
filteredRusWebmob["Duration"].sum()
```




    4420312620


