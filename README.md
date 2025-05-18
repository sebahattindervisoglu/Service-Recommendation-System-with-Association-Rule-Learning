Service Recommendation System with Association Rule Learning
Project Overview
This project aims to build a recommendation system for Armut, Turkey’s largest online service platform that connects service providers with customers. By analyzing monthly user service purchase data, the project generates association rules to recommend related services based on past user behavior.

Problem Statement
In online service platforms like Armut, customers purchase various services (e.g., cleaning, repairs, moving). The goal is to enhance user experience and increase sales by recommending additional services that users are likely to purchase together, using historical purchase patterns.

Dataset
UserId: Customer identifier

ServiceId: Anonymized service identifier within categories

CategoryId: Anonymized service category identifier

CreateDate: Date and time when the service was purchased

Each service is uniquely identified by combining ServiceId and CategoryId.

Approach
Group purchases by user and month to create “baskets” representing monthly service purchases.

Use the Apriori algorithm to find frequent itemsets with minimum support.

Generate association rules with metrics like support, confidence, and lift.

Implement a recommendation function to suggest services based on association rules for a given service.
Usage
Load the dataset: armut_data.csv

Run the data preprocessing and basket creation.

Generate frequent itemsets and association rules using Apriori.

Use the arl_recommender function to get service recommendations for a given service.

recommended_services = arl_recommender(rules, "2_0", rec_count=5)
print("Recommended services:", recommended_services)

Technologies Used
Python

Pandas

mlxtend (Apriori and Association Rules)

License
MIT License

