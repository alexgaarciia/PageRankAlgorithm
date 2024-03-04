# PageRankAlgorithm
- Final grade: 10/10.
- In collaboration with [mariamagro](https://github.com/mariamagro).

## Overview
This project involves the implementation of the original PageRank algorithm, as proposed by Sergey Brin and Larry Page in 1998, which laid the groundwork for the Google Search Engine. The algorithm aims to assign a weight to each webpage on the internet, primarily based on the number of external links pointing to the page. The algorithm's specifications can be found in the original paper: http://ilpubs.stanford.edu:8090/422/1/1999-66.pdf.

## Objective
The primary goal is to apply the PageRank algorithm to set weights for each page within the English version of Wikipedia, utilizing the dataset available in the Databricks Databases Set at the URI: dbfs:/databricks-datasets/wikipedia-datasets/data-001/en_wikipedia/articles-only-parquet. This involves working with a database containing 5,823,210 entries stored in a parquet file format.

## Dataset Analysis
The dataset comprises seven columns: title, id, revisionId, revisionTimestamp, revisionUsername, revisionUsernameId, and text. The essential data for this project is located in the title, id, and text columns. The project involves creating a forward link matrix by identifying outgoing links (noted with double "[[]]") and mapping these to the respective ids. Subsequently, a backward links matrix will be constructed to apply the PageRank algorithm effectively.

## Implementation Details
- Apache Spark DataFrames will be used to manage the Wikipedia database and intermediate results.
- A smaller version of the dataset, approximately 0.01% of the records (around 582 records), is recommended for initial analysis.
- Implementation of a User Defined Function (UDF) to parse the text field from each record and extract the outgoing links is suggested.
- The final output should be a Pandas DataFrame including the columns: title, id, and pagerank, representing the PageRank value for each Wikipedia page.

## Expected Results
The project's culmination is a scalable and optimized implementation of the PageRank algorithm, capable of processing extensive datasets with efficiency and accuracy.

## Evaluation Criteria
The project will be evaluated based on the following criteria:
1. Code Execution: Your code must run without errors (20%).
2. Scalability: Your implementation should be scalable, tested with datasets ten times larger on a cluster with 80 execution workers (20%).
3. Optimization: Code optimization is crucial (20%).
4. Documentation: Adequate code documentation is required (10%).
5. Conclusions: Insightful conclusions based on the project findings (30%).
