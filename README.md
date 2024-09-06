# Basket-Analyzer

This is a project of Basket analyzer where we used This Python script performs market basket analysis using the Apriori algorithm and customer segmentation using the K-means clustering algorithm on synthetic transaction data.

(CODE EXPLANATION)

Libraries Import:
Imports essential libraries for data manipulation (numpy, pandas), synthetic data generation (faker), clustering (scikit-learn), visualization (plotly), and progress tracking (tqdm).

Data Generation (generate_data):
Generates synthetic transaction data for a given number of products, customers, and transactions. The transactions are randomly generated with customers buying random sets of products.
The data is then transformed into a binary-encoded format (customers vs. products) where 1 indicates a product was purchased by a customer.

Apriori Algorithm Implementation (simple_apriori):
Identifies frequent item sets and association rules from the transaction data based on minimum support and confidence thresholds.
Generates rules that provide insights into which products are often bought together and calculates metrics such as support, confidence, and lift to evaluate the strength of the rules.

K-means Clustering (perform_kmeans):
Performs K-means clustering on the customer-product matrix to segment customers into different clusters based on their purchasing behavior.
Uses the tqdm library to provide a progress bar during the clustering iterations and yields intermediate clustering results after a specified number of iterations (update_intervals).

Data Visualization (visualize_apriori, visualize_kmeans):
Uses Plotly to create 3D scatter plots to visualize the top association rules (visualize_apriori) and the customer clusters (visualize_kmeans).

Main Function (main):
Generates synthetic data. Applies the Apriori algorithm to discover association rules. Performs K-means clustering to segment customers.Saves visualizations of the Apriori rules and K-means clustering results as HTML files for interactive exploration.
