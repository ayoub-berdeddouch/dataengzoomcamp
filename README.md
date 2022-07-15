# Data Engineering @DPHI BootCamp ~~ Zoomcamp 

[Data Engineering Bootcamp](https://dphi.tech/bootcamps/data-engineering?itm_source=website&itm_medium=header&itm_campaign=maybootcamps)

<img src="https://github.com/ayoub-berdeddouch/dataengzoomcamp/blob/main/images/dataenge.jpg"/>


---

## Homeworks Progress:
| Week | Module Session                            | Progress | Dead line    | Link               |
|------|-------------------------------------------|----------|--------------|--------------------|
|01    | Introduction & Prerequisites              | ⌛ ✔️    | 15/07/2022   | [Intro]()  |
|02    | Data ingestion                            | ⌛ ✔️    | 15/07/2022   | [Data ingestion]()|
|03    | Data Warehouse                            | ⌛ ✔️    | 15/07/2022   | [Data Warehouse]()|
|04    | Analytics engineering                     | ⌛ ✔️    | 15/07/2022   | [Analytics engineering]()|
|05    | Batch processing                          | ⌛ ✔️    | 15/07/2022   | [Batch processing]()|
|06    | Streaming                                 | ⌛ ✔️    | 15/07/2022   | [Streaming]()|
|07    | Project                                   | ⏳ ✖️    | 21/07/2022   | [Project]()|
|08    | Project                                   | ⏳ ✖️    | 21/07/2022   | [Project]()|
|09    | Project                                   | ⏳ ✖️    | 21/07/2022   | [Project]()|

 


**Hint**

---

__⌛ ✔️= Done__ ||  __⏳ ✖️= Not_DONE__


#### Made with 💟 by [Ayoub Berdeddouch](https://github.com/ayoub-berdeddouch)

---
# About the Course

## Welcome to Data Engineering Bootcamp :)

We are doing this bootcamp with the support of DataTalks.Club. The content is created by some of the renowned data leaders. Many thanks to DataTalks.Club and the instructors for creating and allowing us to put this bootcamp together. Check them out:

## Instructors

- Ankush Khanna (https://linkedin.com/in/ankushkhanna2)
- Sejal Vaidya (https://linkedin.com/in/vaidyasejal)
- Victoria Perez Mola (https://www.linkedin.com/in/victoriaperezmola/)
- Alexey Grigorev (https://linkedin.com/in/agrigorev)
- @DataTalks.Club

## In this bootcamp, there will be:

- 6 Weeks of Learning Content - release every Friday (detailed schedule here)
- Home works for practice
- 1 Graded Hands-on Assignment

## Self-paced mode

* All the materials of the course are freely available, so you can take the course at your own pace
* Follow the suggested syllabus (see below) week by week

## Learning Modules:

* Learning modules will be released every Friday, starting from 13th May, 7:00 PM CET/ 10:30 PM IST.
* Please keep checking this space for regular learning module additions we make.
* To accommodate learners from across the globe, we are putting the learning modules in offline format instead of having live sessions. This will allow you to learn at your own time.
* If you face any issues while learning, feel free to drop a message on #help channel on Discord.

## Assignment Guidelines
* There will be 1 Final Assignment, mandatory to attempt for the bootcamp completion.
* Howeworks are for practice and we recommend you to work on them. However, they don't carry weightage while issuing certificate.
* Certificate: In order to be eligible for the certificate, you should submit the assignment with a total score of minimum 60%.

`Happy Learning :)`


## Syllabus

> **Note**: This is preliminary and may change

### [Week 1: Introduction & Prerequisites](week_1_basics_n_setup)

* Big Picture
   * [x] Introduction to all instructors
   * [x] What to expect in this course
   * [x] Architecture / Data Flow
   * [x] What do we want to build
* GCP
   * [x] Intro to GCP - Concepts: IAM, Cloud Storage, BigQuery (relevant components)
   * [x] What is GCP, why we need it
* [Docker ](week_1_basics_n_setup/2_docker_sql)
   * [x] What is Docker
   * [x] Running Postgres locally with Docker
   * [x] Putting some data for testing to local postres with Python
   * [x] Packaging this script in docker
   * [x] Running postgres and the script in one network
   * [x] Docker compose and running pgadmin and postres together with docker-compose
* [Data and SQL ](week_1_basics_n_setup/2_docker_sql)
   * [x] [Dataset: Taxi Rides NY dataset](dataset.md)
   * [x] Experimentation: Taking a first look at the data 
   * [x] Relevant SQL Queries (Refresher): group by, joins, window function, union
* [Terraform ](week_1_basics_n_setup/1_terraform_gcp)
   * [x] Intro to Terraform - Concepts
   * [x] Setting up GCP with TF: Storage, BigQuery




### [Week 2: Data ingestion](week_2_data_ingestion)

Goal: Orchestrating a job to ingest web data to a Data Lake in its raw form.

Instructor: Sejal Vaidya (https://linkedin.com/in/vaidyasejal) & Alexey Grigorev (https://linkedin.com/in/agrigorev)

* Data Lake (GCS)
  * [x] Basics, What is a Data Lake
  * [x] ELT vs. ETL
  * [x] Alternatives to components (S3/HDFS, Redshift, Snowflake etc.)
* Orchestration (Airflow)
  * Basics
    * [x] What is an Orchestration Pipeline?
    * [x] What is a DAG?

* Demo:
  * Setup:
    * [x] Docker pre-reqs (refresher)
    * [x] Airflow env with Docker
  * Data ingestion DAG - Demo (30 mins): 
    * [x] Extraction: Download and unpack the data
    * [x] Pre-processing: Convert this raw data to parquet, partition (raw/yy/mm/dd)
    * [x] Load: Raw data to GCS
    * [x] Exploration: External Table for BigQuery -- Taking a look at the data
    * [x] Further Enhancements: Transfer Service (AWS -> GCP)
   



### [Week 3: Data Warehouse](week_3_data_warehouse)

Goal: Structuring data into a Data Warehouse

Instructor: Ankush Khanna (https://linkedin.com/in/ankushkhanna2)

* Data warehouse (BigQuery) (25 minutes)
    * [x] What is a data warehouse solution
    * [x] What is big query, why is it so fast, Cost of BQ,  (5 min)
    * [x] Partitoning and clustering, Automatic re-clustering (10 min)
    * [x] Pointing to a location in google storage (5 min)
    * [x] Loading data to big query & PG (10 min) -- using Airflow operator?
    * [x] BQ best practices
    * [x] Misc: BQ Geo location, BQ ML 
    * [x] Alternatives (Snowflake/Redshift)




### [Week 4: Analytics engineering](week_4_analytics_engineering/taxi_rides_ny/)

Goal: Transforming Data in DWH to Analytical Views

Instructor: Victoria Perez Mola (https://www.linkedin.com/in/victoriaperezmola/)

* Basics 
    * [x] What is DBT?
    * [x] ETL vs ELT 
    * [x] Data modeling
    * [x] DBT fit of the tool in the tech stack
* Usage (Combination of coding + theory) (1:30-1:45 mins)
    * [x] Anatomy of a dbt model: written code vs compiled Sources
    * [x] Materialisations: table, view, incremental, ephemeral  
    * [x] Seeds 
    * [x] Sources and ref  
    * [x] Jinja and Macros 
    * [x]Tests  
    * [x] Documentation 
    * [x] Packages 
    * [x] Deployment: local development vs production 
    * [x] DBT cloud: scheduler, sources and data catalog (Airflow)
* Google data studio -> Dashboard
* Extra knowledge:
    * [x] DBT cli (local)

### [Week 5: Batch processing](week_5_batch_processing)

Goal: 

Instructor: Alexey Grigorev (https://linkedin.com/in/agrigorev)

* Distributed processing (Spark) 
    * [x] What is Spark, spark cluster 
    * [x] Explaining potential of Spark 
    * [x] What is broadcast variables, partitioning, shuffle
    * [x] Pre-joining data 
    * [x] use-case
    * [x] What else is out there (Flink)
* Extending Orchestration env (airflow) 
    * [x] Big query on airflow 
    * [x] Spark on airflow 



### [Week 6: Streaming](week_6_stream_processing)

Goal: 

Instructor: Ankush

* Basics
    * [x] hat is Kafka
    * [x] nternals of Kafka, broker
    * [x] artitoning of Kafka topic
    * [x] eplication of Kafka topic
* Consumer-producer
* Schemas (avro)
* Streaming
    * [x] Kafka streams
* Kafka connect
* Alternatives (PubSub/Pulsar)


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
