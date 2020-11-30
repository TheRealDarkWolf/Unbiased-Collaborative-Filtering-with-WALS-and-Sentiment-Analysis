# Building Recommender Systems on the Yelp Open Dataset

Since the dataset is too large to be uploaded, the drive link to the dataset is :https://drive.google.com/drive/folders/1pWMpf4OBkSXnaPEFBmO_k1KX4t1eSv6n?usp=sharing
The notebook can be executed sequentially if the data folder is in the same directory as the notebook
There are 2 ways to load the data, since the notebook was written on colaboratory, the dataset links are drive links. Everytime data is loaded, there 2 lines of code. 
1.The first line of code loads the data using google drive links. You can run this line if you have the data folder and the notebook in the same directory on drive. Minor changes might be required depending on the name of your directory. 
2. The second line of code is a relative path to the data if you're running the notebook locally. As long as the data folder and the notebook are in the same directory, the code will run. This line of code is commented out by default and will need to be uncommented every time you want to load the data using this method.
The notebook is divided into 8 sections
## EDA and Visualizations
This section of the uses the all_restaurants.csv dataset to perform some EDA and visualisations, all cells can be run in any order as long as the data has been loaded. Additional directions if necessary are documented in the notebook.

## Content Based Recommender System
The code here needs to be run sequentially. Data from Scottsdale Arizona is loaded by default. This can be changed to the dataset of your choice. Scottsdale is chosen because its size was just enough to let it run on colab without crashing when generating the cosine similarity matrix. The last 2 cells accept a restaurant of your choice and output recommendations based on your input

## Collaborative Filtering with PCC
The code here needs to be run sequentially. Data from Scottsdale Arizona is loaded by default. Either pearson correlation or cosine similarity can be used to generate item similarity matrix. A generalized test cell exists with a dummy user and his ratings to demonstrate the recommender system's working

## Collaborative Filtering with cosine similarity and evaluation metrics
The code here needs to be run sequentially. Data from Cleveland Ohio is loaded by default. Both MSE and Precision@k are used as metrics. Loss is calculated for user-user and item-item collaborative filtering and loss is compared before and after bias subtraction

## Word Clouds and some nlp
The code here can be run sequentially. Data from Cleveland Ohio is loaded and document term matrix of the reviews are generated. Extracting only the adjectives from reviews, we can plot word clouds for restaurants of our choice, the 2 options included by default are the 10 most popular restaurants in Cleveland and 10 most infamous (high review count but low rating) restaurants.

## Sentiment Analysis
This section focuses on extracting the review rating or converting the review into an unbiased rating using its polarity and subjectivity. The code in this section can be run sequentially. The dataset created during this section is used in the WALS model if you want to generate unbiased recommendations.

## Collaborative Filtering with WALS

## Extracting Recommendations

