This folder contains all codes for our final project for EECS 549/SI 650 information retrieval.

Our project implemented a search engine for recipes, which allows users to input the search query with certain food name, 
certain ingredients, ingredients that users want to avoid, the number of searched recipes, the range of ratings for recipes, and the range of calories for recipes.

# Scrape dataset
To scrape the dataset, first run the /recipescrape to get the urls for recipes. The final dataset file is too large to upload.
(first run "pip install scrapy", then run "scrapy crawl recipes").
After obtaining the url files, run the dataset.ipynb to scrape the contents in urls, generate docno,
and save the scraped data to a csv file. We also provide our scraped dataset in the root folder whose name is recipes.csv

# Our search algorithm
We include our method in the evaluation.ipynb. You could run the notebook to conduct learning to rank with our features, evaluate and compare our method with pyterrier experiements. The queries and qrels can be found 
in root folder, whose names are all_queries.csv and all_qrel.csv

# Composition & negation (for search interface)
We include the demonstration of the code in Composition&Negation.ipynb. In this notebook, we use BM25 to demonstrate the effectiveness of the features for search interface.

# The final demo
Please run the code in search_demo.ipynb, where we integrate the composition & negation features with our search algorithm (which beats BM25 in MAP, NDCG, and NDCG@10!), and build a simple demo which allows the user 
to input queries with multiple fields. The demo will display a dataframe with titles, cook time, ratings, number of servings, ingredients, instructions, information of calories, sugar, fiber, fat, sodium and other nutrition contents.
