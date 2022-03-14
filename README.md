# Analyse-Yelp-Dataset-with-Spark-Parquet-Format-on-Azure-Databricks
Analysis and Visualisation of Yelp Dataset using Apache Spark | Elastic Search | Kibana


Introduction

Most businesses seek to get reviews on their goods and services one way or another. It is a most basic way for the business to improve their efficiency and subsequently their bottom-line. Get the review is not only the issue, ability to extract and visualize analytics from review data is critical to business success.

In Apache Spark Project, we will use the yelp review dataset to analyze businesses and reviews over a period of time. Perhaps we will spot potential gaps in service delivery or see how business thrive in different scenarios.

Beyond processing this data, we will ingest the final output of our data processing in Elasticsearch and use the visualization tool in the ELK stack to visualize various kinds of ad-hoc reports from the data.


Goal

The goal of this Spark project is to analyze business reviews from Yelp dataset and ingest the final output of data processing in Elastic Search.Also, use the visualisation tool in the ELK stack to visualize various kinds of ad-hoc reports from the data.


Architecture

![image](https://user-images.githubusercontent.com/96236642/158189770-d2e4263b-c734-44b7-8f6d-9528d9ee8698.png)



![image](https://user-images.githubusercontent.com/96236642/158189813-4ea81a52-9891-4833-9117-c0126054d6ba.png)


• Import data from yelp dataset into relational database(MySQL)

please go through file(get_yelp_in_mysql_databaset.txt) for more information 
• Ingesting data from relational database (MySQL) using Sqoop into Hadoop HDFS

please go through file(yelp_mysql_sqoop_commands.txt) for more information 
• Ingesting data from relational database directly into Spark

• Processing relational data in Spark

• Ingesting processed data into Elasticsearch

• Visualizing review analytics using Kibana


Technology stack


![image](https://user-images.githubusercontent.com/96236642/158189857-c0db3fb9-7530-4bd2-a7fc-62d2e9a2752b.png)



Area	Technology
DataSet	Yelp
Relational Database	MySQL
Big Data Ingestion Tool	Hadoop (Sqoop)
Distributed File System	Hadoop (HDFS)
Cluster Computing Framework	Apache Spark (Scala)
Search and Analytics Engine	Elasticsearch

Yelp schema

![image](https://user-images.githubusercontent.com/96236642/158189934-b92195f4-a549-4e6a-9875-18c64f87f318.png)


Out of all attributes we will focus on some shown below

Business

category

hours

Review


Use Cases considered for Visualisation

Top 10 Business Categories

Yelp Business Map

Business distribution by state

Average rating of business over time

Top rated businesses

User sign up trend


Configuring Environment

Installation of Cloudera quickstart VM

Installation of Elk stack

Later Configuring Scala Runtime to Cloudera QuickStart VM

Watch the below video for more information

https://www.youtube.com/watch?v=SFJsuo2XISs


Execution Instructions
Launch the Spark Shell

spark-shell --packages org.elasticsearch:elasticsearch-spark-13_2.10:6.1.1 --conf spark.es.index.auto.create=true --conf spark.es.nodes= Ipaddress:port(Elastic search)


Visualisation Screen shots

After Ingesting processed data into Elasticsearch




Yelp User sign up trend



![image](https://user-images.githubusercontent.com/96236642/158190157-c091df5c-32f4-4f5a-a231-dcaa6e28c55b.png)


Business distribution by state


![image](https://user-images.githubusercontent.com/96236642/158190206-9df70f1e-66b2-414b-b731-0107e7e43ee7.png)


Yelp review


![image](https://user-images.githubusercontent.com/96236642/158190242-81005ac7-32cc-4315-8e77-c2bb18252f6e.png)


Top 10 Business Categories


![image](https://user-images.githubusercontent.com/96236642/158190296-6f3bcf7e-f8cf-4394-be57-b80b61e62e57.png)



![image](https://user-images.githubusercontent.com/96236642/158190322-e63a3d2f-25f1-4005-9bcc-3f46a37aaeff.png)


Dashboard


![image](https://user-images.githubusercontent.com/96236642/158190366-6de1267c-389e-43c5-befd-fad995e953c2.png)


