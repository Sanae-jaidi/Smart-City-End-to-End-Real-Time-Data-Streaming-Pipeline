# Smart-City-End-to-End-Real-Time-Data-Streaming-Pipeline

![Analysis-1](https://github.com/user-attachments/assets/a762594c-92e1-4dee-a0bd-0db682546b05)

## Project Overview

This project establishes a fully operational real-time data streaming pipeline tailored for Smart City applications. It captures and processes data from a vehicle journey between London and Birmingham, including metrics like vehicle performance, GPS locations, emergency events, weather conditions, and camera footage. Utilizing IoT devices, Apache Kafka, Apache Spark, Docker, and AWS services, this pipeline provides robust data ingestion, processing, storage, and visualization.

## System Architecture

![System Architecture](https://github.com/user-attachments/assets/4f1c54b5-732d-4482-a154-6478d17b070d)

## Key Technologies

- **IoT Devices**: Collects live data from the environment.
- **Apache Zookeeper**: anages Kafka brokers for reliable data coordination.
- **Apache Kafka**: Ingests and streams real-time data to various topics.
- **Apache Spark**: Processes and streams data in real-time.
- **Docker**: Facilitates containerized setup for Kafka and Spark.
- **Python**: Supports data processing and transformation scripts.
- **AWS Cloud Services**: 
  - **S3**: Stores processed data as Parquet files.
  - **Glue**: Extracts and catalogs data for accessibility.
  - **Athena**: Enables querying of processed data.
  - **IAM**: Manages user roles and access controls.
  - **Redshift**: Provides data warehousing and analytics.
- **Amazon QuickSight**: Creates interactive dashboards for data visualization.

## Pipeline Workflow

1. **Data Ingestion**:
   - IoT devices stream live data.
   - Data flows into Kafka topics, deployed using Docker and configured in docker-compose.yml.

2. **Data Processing**:
   - Apache Spark reads and processes data from Kafka.
   - Spark writes processed data to AWS S3 in Parquet format, utilizing Spark Streaming for continuous processing with checkpointing.

3. **Data Storage**:
   - Processed data is stored in AWS S3.
   - AWS Glue crawlers catalog data, making it accessible for querying.

4. **Data Querying**:
   - AWS Athena retrieves and queries cataloged data from Glue.

5. **Data Visualization**:
   - Amazon QuickSight visualizes the data with dynamic dashboards.

## Dashboard

The Amazon QuickSight dashboard includes:

- **Total Number of Entries in Each Table**: KPI widgets or bar charts.
- **Average Speed of Vehicles**: Displayed as a single KPI value.
- **Number of Emergency Incidents**: Displayed as a KPI.
- **Time Series Analysis**: Line charts for vehicle data, weather data, and emergency incidents over time.
- **Geographic Visualization**: Maps showcasing routes and vehicle locations.
- **Heat Maps**: Density maps for GPS data points.
- **Detailed Analysis**: Tables and pie charts offering in-depth insights.

## Conclusion

This Smart City project showcases the capability of modern data engineering to efficiently handle real-time data, producing actionable insights for urban management. The integration with AWS offers scalability and reliability, illustrating an effective end-to-end streaming data solution.

## Acknowledgments

Special thanks to the open-source community for the tools and libraries used in this project.
