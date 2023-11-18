# Spotify Film Score Data Engineering ETL Pipeline

### Description
Explore my GitHub repository featuring an ETL pipeline project that harmoniously blends Spotify API integration with the collection of film score data. Witness the seamless extraction, transformation, and loading of musical insights from Spotify, coupled with the cinematic touch of film score data. Immerse yourself in the intersection of music and film through this unique project, offering a concise yet powerful demonstration of ETL processes in action.
### Note: 
Spotify client secret has been rotated for privacy.

### Architecture

![Architecture Diagram](https://github.com/brandonjensengit/spotify_etl_pipeline/assets/3952764/1b9283fd-5a72-4357-a8dd-97b1cd8a2cb2)

### About Dataset/API
This [API](https://developer.spotify.com/documentation/) contains information about the top film score soundtracks and album information from Spotify.

### Services Used
1. **S3 (Simple Storage Service):** Amazon S3 is a scalable and secure object storage service offered by AWS. It allows you to store and retrieve any amount of data from anywhere on the web.
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without provisioning or managing servers. It automatically scales and manages the infrastructure needed to run your applications.
3. **Cloud Watch:** Amazon CloudWatch is a monitoring service that provides real-time insights into your AWS resources and applications. It collects and tracks metrics, monitors log files, and sets alarms.
4. **Glue Crawler:** AWS Glue Crawler is part of the AWS Glue service, designed for data integration. The Crawler connects to your source or target data store, progresses through a defined path, and extracts metadata to populate the AWS Glue Data Catalog.
5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover, manage, and organize your data. It stores metadata from various sources, enabling a unified view for efficient data governance and discovery.
6. **Amazon Athena:** Amazon Athena is a serverless, interactive query service that makes it easy to analyze data directly in Amazon S3 using SQL. It requires no infrastructure setup, and you only pay for the queries you run.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract Data from API -> Lambda Trigger (Every Day) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Tranform Data and Load it -> Query Using Athena
