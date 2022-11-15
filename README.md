# WeRateDogs-Wrangling_Project
### by Amen T. Ajamu

### Introduction:

The project required me to work on three datasets in different formats. These datasets were a twitter archive file in the csv format, an image prediction file in the tsv format and an additional json file gotten from twitter api in the txt format. 

These datasets contain bits an pieces of data to make up the whole required to derive insights from the tweets of a twitter handle @handle, we rate dogs. We rate dogs is renown for using a numerator/denominator rating system to rate dogs. This page has large following and is internationally recognised.

Upon importing the relevant libraries, using aliases where applicable, I proceeded to wrangle the datasets with the aim of deriving intelligible insights.
### Gathering the Data

To gather both the twitter archive and the image prediction files, I used the popular `pandas.read_csv()` method. Only that I specified the specified the separator for the image prediction file to be `\t` upon getting it from the supplied url using the get method and the request library.

To import the datasets gotten from the twitter API, I used the request library to fetch it from the supplied url and then used `pandas.read_json()` to read it into a dataframe
### Assessing the data

To assess the data, I firstly merged all the three datasets on the 'tweet_id' column upon realising that they had it in common. This also meant that tidines issue had been resolved before anything else. Afterwards, I converted the dataframe into a single csv file and then carried out visual assessment on it using microsoft excel. It was while doing this that I realised that a good number of columns were either empty or contained an insignificant number of entries. I noted these quality issues down in the space provided.

Furthermore, I did some programmatic assessment to pick up other quality issues that had to do with incorrect data types and extra characters. These quality  issues were all noted down to make up the total sum of 8 quality issues required for me to complete the project. Using the `df.describe()` method, rating denominator and numerator values that were outliers were determined and noted for futher action.
### Cleaning the Data

The data was cleaned for quality and tidiness issues using methods such as the `df.melt()` method, the `df.drop()` method among others. The data was then stored in a csv format upon completing the cleaning.
### Visualization and Conclusion

Univariate and bivariate visualizations were carried out on the dataset and the following insights were derived:
 
 - The major proportion of the dogs were either "pupper" or "doggo". This distribution was also observed in the dog specie with the most number of favorites and retweets. As such, it is unclear whether the audience had any particular liking for any of the dog stages.
 
 - The rating numerator of value 12 was found to be most prominent in the dataset. It is unclear why that is, but studies have shown that humans tend to have a bias for even numbers.
 
 - Finally, the majority of the languages were english and a very little propotion of the dogs in the dataset were hairy
