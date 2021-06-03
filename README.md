# Network-Science-Project-Spring-2021

This repo houses the code for our term project for the course 'Network Science', given in the University of Tartu in spring 2021. We would like to present brief information about the notebooks & data files here, for more details please feel free to check them.

  'Berlin_EDA' stands for our efforts in combining the road network datasets provided by OpenStreetMap(OSM) and Uber for the city of Berlin. In order to run this notebook successfully, you need to unzip the 'berlin.csv.zip' file which includes the Uber Movement data for Berlin. OSM data can be accessed directly by using the OSMnx library, you can install it by following the instructions here: https://osmnx.readthedocs.io/en/stable/ .
  
  We saved the nodes and edges of our Berlin road network as csv files to simplify the running of the notebooks we describe below.
  
  In the 'Baseline' notebook, we used the features from the dataset we created in Berlin_EDA and fitted linear regression and random forest regression models on them to predict the mean speeds of the roads in Berlin.
  
  In the notebook called as 'First Approach', we used the features from the baseline model but also added some features that purely depended on our graph's structure(number of common neighbors, katz score etc), which are extracted in an unsupervised manner. We fed these combined set of features to the same models we used in the baseline.
  
  In 'Berlin_Node2Vec-Final', we only used Node2Vec embeddings for our LR and RF models to predict the mean speeds of the roads. We tried several values for the Node2Vec parameters p and q, to see if the results change according to the type of search we use. There wasn't a significant difference in the mean square errors between the embeddings created by breadth-first search and the ones created by depth-first search.
