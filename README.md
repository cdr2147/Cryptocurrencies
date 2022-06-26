# Cryptocurrencies

# Overview
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. You have been asked to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

# Purpose
Using data retrieved from CryptoCompare, we process the data to fit the machine learning models and decide to use unsupervised learning to advise Accountability Accounting as there is no known output for the analysis. We use a clustering alorith to group the cryptocurrencies and use data visualizations to share our findings.

# Results
First, we load our data from CryptoCompare:

![load data](https://user-images.githubusercontent.com/99205688/175836683-8ee96866-ecf9-4176-be71-07b675ce59db.PNG)

Then we transform our data to keep only cryptocurrencies that are being traded, have a working algorithm, coins are mined, and remove unnecessary columns and null values:

![cleaned data](https://user-images.githubusercontent.com/99205688/175836692-19063495-a2f5-41d2-9b36-8d963115968c.PNG)

Then we scale the data and used PCA to reduce dimension to three principal components and create a new dataframe:

![pca](https://user-images.githubusercontent.com/99205688/175836745-9fd8cbbd-8d3a-4093-bfed-8ab8fe333951.PNG)

Then we create an elbow curve to find the best value for K:

![elbow curve](https://user-images.githubusercontent.com/99205688/175836766-6510dd8e-ab68-4f18-a3c4-af037410a83e.PNG)

We create a new DataFrame including predicted clusters and cryptocurrencies features and make a 3D-Scatter with the PCA data and clusters:

![3d](https://user-images.githubusercontent.com/99205688/175836782-d865ced0-166b-4b94-a6e9-8cf57f68cb79.PNG)

Finally, we create a new dataframe with the scaled data and make a hvplot.scatter plot

![scatterplot](https://user-images.githubusercontent.com/99205688/175836810-f3e3bc40-3862-4f5e-b7e3-67a428cad15e.PNG)
