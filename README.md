# Network-Science-Project-Spring-2021

This repository houses the code for our Spring 2021 Network Science project at the University of Tartu. The following information summarizes the notebooks and raw data files located herein.

Berlin_EDA.ipynb performs exploratory data analysis as well as combines the road network dataset in Berlin, Germany provided by OpenStreetMap (OSM) with Uber movement data for rides in Berlin in Q1 2020. In order to run this notebook, unzip the 'berlin.csv.zip' file containing Uber movement data. OSM data can be accessed directly by using the OSMnx library, which can be installed by following the instructions located at https://osmnx.readthedocs.io/en/stable/.
  
Nodes and edges of the Berlin road network were saved as CSV files to simplify the running of the notebooks described below.
  
In Baseline.ipynb, features from the dataset created in Berlin_EDA.ipynb were fit using linear regression and random forest regression models to predict the mean speeds of roads in Berlin.
  
In First Approach.ipynb, we used the features from the baseline model but also added features that depend entirely on our graph's structure--similarity measures such as the number of common neighbors, Katz score, Jaccard index, Adamic/Adar index--which are extracted in an unsupervised manner. We fed this combined set of features into the linear regression and random forest regression models used in Baseline.ipynb.
  
In Berlin_Node2Vec-Final.ipynb, only Node2Vec embeddings were used for the linear regression and random forest models to predict the mean speeds of the roads. We tried several values for the Node2Vec parameters p and q to see if the results change according to the type of search used. There wasn't a significant difference in the mean squared errors between the embeddings created by breadth-first search and those created by depth-first search.
  
Lastly, the New York City Taxi GitHub folder encapsulates our earliest efforts in this project. We pivoted several times while working on this project, but still wanted to include the NYC taxi data for completeness. 
