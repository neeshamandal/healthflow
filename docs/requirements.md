A. Problem Statement:
healthcare organizations receives raw dataset from different healthcare system in different format such as xml, csv, json. These datasets needs to be validated, cleaned, transformed and organized into a standarized format for downstream use. HealthFlow provides a platform to upload these datasets and process them through configurable processing workflows.

B. Users:
data engineers, data analysts

C. Functional Requirements:
   
    
    Dataset Management

1. User can upload CSV, JSON and XML datasets.

2. System stores the uploaded file.

3. System stores metadata about the dataset.

4. User can view uploaded datasets.

5. User can view details of a dataset.


   Processing

6. User can create a processing job for a dataset.

7. System validates the input dataset.

8. System parses the dataset according to its format.

9. System cleans and transforms the data.

10. System stores the processed result.

11. System tracks processing status.

12. User can view processing job details.

    
D. Non-Functional Requirements:
   1. Extensibility
   New dataset formats should be easy to add.

2. Maintainability
   Uploading, processing and persistence logic
   should be separated.

3. Reliability
   Processing failures should not corrupt data.

4. Data Integrity
   Invalid data should be detected before
   being stored as processed data.

5. Observability
   Processing failures should be traceable
   through logs and job information.

6. Performance
   Large datasets should eventually be processed
   without blocking the user's request.
   
D. Version 1 Scope: 

React
   ↓
Spring Boot
   ↓
PostgreSQL + Local File Storage

Supported:
CSV
JSON
XML

Features:
Upload
Metadata
Dataset listing
Create processing job
Basic synchronous processing
Job status
Results

E. Future Features: 

V2
S3
 ↓
Async processing
 ↓
SQS
 ↓
Workers

V3
Spark
 ↓
EMR
 ↓
Hudi

V4
Configurable pipelines
 ↓
Multiple processing engines
