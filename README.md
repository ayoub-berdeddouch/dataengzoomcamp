# Data Engineering Zoomcamp

<img src="https://github.com/ayoub-berdeddouch/dataengzoomcamp/blob/main/images/dataenge.jpg"/>


---

## Homeworks Progress:
| Week | Module Session                            | Progress | Dead line    | Link               |
|------|-------------------------------------------|----------|--------------|--------------------|
|01    | Introduction & Prerequisites              | ⌛ ✔️    | 17/01/2022   | [Intro](https://github.com/ayoub-berdeddouch/dataengzoomcamp/blob/main/Intro/)  |
|02    | Data ingestion                            | ⏳ ✖️    | --/01/2022   | [Data ingestion]()|
|03    | Data Warehouse                            | ⏳ ✖️    | --/--/2022   | [Data Warehouse]()|
|04    | Analytics engineering                     | ⏳ ✖️    | --/--/2022   | [Analytics engineering]()|
|05    | Batch processing                          | ⏳ ✖️    | --/--/2022   | [Batch processing]()|
|06    | Streaming                                 | ⏳ ✖️    | --/--/2022   | [Streaming]()|
|07    | Project                                   | ⏳ ✖️    | --/--/2022   | [Project]()|
|08    | Project                                   | ⏳ ✖️    | --/--/2022   | [Project]()|
|09    | Project                                   | ⏳ ✖️    | --/--/2022   | [Project]()|

 


**Hint**

---

__⌛ ✔️= Done__ ||  __⏳ ✖️= Not_DONE__


#### Made with 💟 by [Ayoub Berdeddouch](https://github.com/ayoub-berdeddouch)

---
# About the Course



- **Start**: 17 January 2022
- **Registration link**: https://airtable.com/shr6oVXeQvSI5HuWD
- Register in [DataTalks.Club's Slack](https://datatalks.club/slack.html)
- Join the [`#course-data-engineering`](https://app.slack.com/client/T01ATQK62F8/C01FABYF2RG) channel
- Subscribe to our [public Google Calendar](https://calendar.google.com/calendar/?cid=ZXIxcjA1M3ZlYjJpcXU0dTFmaG02MzVxMG9AZ3JvdXAuY2FsZW5kYXIuZ29vZ2xlLmNvbQ) (it works from Desktop only)
- The videos will be published to [DataTalks.Club's YouTube channel](https://www.youtube.com/c/DataTalksClub) in [the course playlist](https://www.youtube.com/playlist?list=PL3MmuxUbc_hJed7dXYoJw8DoCuVHhGEQb) 


## Syllabus

> **Note**: This is preliminary and may change

### [Week 1: Introduction & Prerequisites](week_1_basics_n_setup)

* Big Picture
   * [x] Introduction to all instructors
   * [x] What to expect in this course
   * [x] Architecture / Data Flow
   * [x] What do we want to build
* GCP (5 mins)
   * [x] Intro to GCP - Concepts: IAM, Cloud Storage, BigQuery (relevant components)
   * [x] What is GCP, why we need it
* [Docker (45 mins)](week_1_basics_n_setup/2_docker_sql)
   * [x] What is Docker
   * [x] Running Postgres locally with Docker
   * [x] Putting some data for testing to local postres with Python
   * [x] Packaging this script in docker
   * [x] Running postgres and the script in one network
   * [x] Docker compose and running pgadmin and postres together with docker-compose
* [Data and SQL (15 mins)](week_1_basics_n_setup/2_docker_sql)
   * [x] [Dataset: Taxi Rides NY dataset](dataset.md)
   * [x] Experimentation: Taking a first look at the data 
   * [x] Relevant SQL Queries (Refresher): group by, joins, window function, union
* [Terraform (45-60 mins)](week_1_basics_n_setup/1_terraform_gcp)
   * [x] Intro to Terraform - Concepts
   * [x] Setting up GCP with TF: Storage, BigQuery
* [Homework](week_1_basics_n_setup/homework.md)

Duration: 2-2.5h


### [Week 2: Data ingestion](week_2_data_ingestion)

Goal: Orchestrating a job to ingest web data to a Data Lake in its raw form.

Instructor: Sejal & Alexey

* Data Lake (GCS) -- 10 mins
  * Basics, What is a Data Lake
  * ELT vs. ETL
  * Alternatives to components (S3/HDFS, Redshift, Snowflake etc.)
* Orchestration (Airflow) -- 15 mins
  * Basics
    * What is an Orchestration Pipeline?
    * What is a DAG?

* Demo:
  * Setup: (15 mins)
    * [ ] Docker pre-reqs (refresher)
    * [x] Airflow env with Docker
  * Data ingestion DAG - Demo (30 mins): 
    * [x] Extraction: Download and unpack the data
    * [ ] Pre-processing: Convert this raw data to parquet, partition (raw/yy/mm/dd)
    * [x] Load: Raw data to GCS
    * [x] Exploration: External Table for BigQuery -- Taking a look at the data
    * [ ] Further Enhancements: Transfer Service (AWS -> GCP)
   
Duration: 1.5h


### [Week 3: Data Warehouse](week_3_data_warehouse)

Goal: Structuring data into a Data Warehouse

Instructor: Ankush

* Data warehouse (BigQuery) (25 minutes)
    * What is a data warehouse solution
    * What is big query, why is it so fast, Cost of BQ,  (5 min)
    * Partitoning and clustering, Automatic re-clustering (10 min)
    * Pointing to a location in google storage (5 min)
    * Loading data to big query & PG (10 min) -- using Airflow operator?
    * BQ best practices
    * Misc: BQ Geo location, BQ ML 
    * Alternatives (Snowflake/Redshift)

Duration: 1-1.5h


### [Week 4: Analytics engineering](week_4_analytics_engineering/taxi_rides_ny/)

Goal: Transforming Data in DWH to Analytical Views

Instructor: Victoria

* Basics (15 mins)
    * What is DBT?
    * ETL vs ELT 
    * Data modeling
    * DBT fit of the tool in the tech stack
* Usage (Combination of coding + theory) (1:30-1:45 mins)
    * Anatomy of a dbt model: written code vs compiled Sources
    * Materialisations: table, view, incremental, ephemeral  
    * Seeds 
    * Sources and ref  
    * Jinja and Macros 
    * Tests  
    * Documentation 
    * Packages 
    * Deployment: local development vs production 
    * DBT cloud: scheduler, sources and data catalog (Airflow)
* Google data studio -> Dashboard
* Extra knowledge:
    * DBT cli (local)

Duration: 2h    


### [Week 5: Batch processing](week_5_batch_processing)

Goal: 

Instructor: Alexey

* Distributed processing (Spark) (40 + ? minutes)
    * What is Spark, spark cluster (5 mins)
    * Explaining potential of Spark (10 mins)
    * What is broadcast variables, partitioning, shuffle (10 mins)
    * Pre-joining data (10 mins)
    * use-case
    * What else is out there (Flink) (5 mins)
* Extending Orchestration env (airflow) (30 minutes)
    * Big query on airflow (10 mins)
    * Spark on airflow (10 mins)

Duration: 1-1.5h

### [Week 6: Streaming](week_6_stream_processing)

Goal: 

Instructor: Ankush

* Basics
    * What is Kafka
    * Internals of Kafka, broker
    * Partitoning of Kafka topic
    * Replication of Kafka topic
* Consumer-producer
* Schemas (avro)
* Streaming
    * Kafka streams
* Kafka connect
* Alternatives (PubSub/Pulsar)

Duration: 1.5h



### [Week 7, 8 & 9: Project](project)

* Putting everything we learned to practice

Duration: 2-3 weeks

* Upcoming buzzwords
  *  Delta Lake/Lakehouse
    * Databricks
    * Apache iceberg
    * Apache hudi
  * Data mesh
  * KSQLDB
  * Streaming analytics
  * Mlops
  
Duration: 30 mins

## Overview

### Architecture diagram
<img src="https://github.com/DataTalksClub/data-engineering-zoomcamp/raw/main/images/architecture/arch_1.jpg"/>

### Technologies
* *Google Cloud Platform (GCP)*: Cloud-based auto-scaling platform by Google
  * *Google Cloud Storage (GCS)*: Data Lake
  * *BigQuery*: Data Warehouse
* *Terraform*: Infrastructure-as-Code (IaC)
* *Docker*: Containerization
* *SQL*: Data Analysis & Exploration
* *Airflow*: Pipeline Orchestration
* *DBT*: Data Transformation
* *Spark*: Distributed Processing
* *Kafka*: Streaming


### Prerequisites

To get most out of this course, you should feel comfortable with coding and command line,
and know the basics of SQL. Prior experience with Python will be helpful, but you can pick 
Python relatively fast if you have experience with other programming languages.

Prior experience with data engineering is not required.



## Instructors

- Ankush Khanna (https://linkedin.com/in/ankushkhanna2)
- Sejal Vaidya (https://linkedin.com/in/vaidyasejal)
- Victoria Perez Mola (https://www.linkedin.com/in/victoriaperezmola/)
- Alexey Grigorev (https://linkedin.com/in/agrigorev)

