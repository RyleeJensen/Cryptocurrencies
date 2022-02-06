# Cryptocurrencies
## Overview
The purpose of this project is to analyze Cryptocurrency data with the help of Unsupervised Machine Learning. We wanted to be able to show what cryptocurrenices are on the market and figure out how they could be grouped to create a classification system in order to create a cryptocurrency investment portfolio for our client. We had to process the data to fit the machine learning model, we reduced dimensions using PCA, we clustered the data using K-means, and then used hvPlot to visualize the data.

## Resources
- Data Source: crypto_data.csv
- Tools: Python 3.8.8, scikit-learn, hvPlot, Pandas, plotly, Jupyter Notebook

## Results
After we cleaned up the data (i.e dropped null rows, only kept cryptocurrencies that were being traded, etc.) and reduced the dimensions to three principal components using PCA, we were able to cluster the data using K-means. In order to figure out the best value for K, we created an elbow curve. As seen in the image below, we were able to determine that 4 was the optimal number of clusters to use.

![ElbowCurve](https://github.com/RyleeJensen/Cryptocurrencies/blob/main/Images/ElbowCurve.png)

We were then able to initialize the K-means model, fit the model, and predict clusters. With this new data, we created a 3D scatter plot in order to visually see where the clusters sat in comparison of one-another

![3DPlot](https://github.com/RyleeJensen/Cryptocurrencies/blob/main/Images/3DPlot.png)

From there, we could create a table useing hvplot.table(). This allowed us to easily see all the tradable cryptocurrencies, of which there is a total of 532.

![Table](https://github.com/RyleeJensen/Cryptocurrencies/blob/main/Images/hvTable.png)

Finally, we made a scatter plot that was grouped by "Class" and in Jupyter Notebook, when you hover over a plot on the chart, you will be able to see the Coin Name and all of the data that follows (such as the total amount of coins mined and the total coin supply).

![ScatterPlot](https://github.com/RyleeJensen/Cryptocurrencies/blob/main/Images/ScatterPlot.png)
