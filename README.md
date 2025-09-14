# Real-Time-Data-Pipeline-using-AWS-Kinesis-and-Snowflake
Analyze global market data in real-time. This project uses AWS Kinesis Firehose to ingest and transform CSV datasets, Snowflake for data warehousing and analytics, and Power BI for visualization.



## Business Overview

This project implements a real-time data pipeline, a critical data engineering practice for integrating live data from diverse sources like IoT devices, APIs, and web servers. The pipeline transforms this raw data into actionable insights for analytics and loads it into destination systems in real-time. This capability is essential for organizations that need to process and analyze large volumes of data instantly.

## Key Features

* **Complex Workflow Handling:** Seamlessly manages intricate data workflows.
* **Data Quality Assurance:** Ensures data accuracy and completeness, with robust handling of upserts during transformations.
* **Unified Data Integration:** Consolidates data from various sources into a cohesive format.
* **Cost Efficiency:** Optimizes computational resources by updating destination systems with only new records.

## Technology Stack

This pipeline is built using a combination of **AWS services** and **Snowflake**. We chose Snowflake for its ability to efficiently handle semi-structured data in real-time. This automated solution leverages the in-house tools of AWS and Snowflake to ensure reliability, availability, and durability.

* Languages : Python, SQL

* Services : AWS Kinesis, AWS App Runner, AWS Kinesis Firehose, AWS S3, AWS Lambda, Snowflake, Power BI

  <img width="945" height="494" alt="image" src="https://github.com/user-attachments/assets/2f27c57b-1067-4412-8fd4-3a6e8f4e9aa1" />




  
## Dataset Overview

This project utilizes a comprehensive dataset of the global food market. Spanning from January 2007 to May 2023, the data covers 36 countries and 2,200 markets, providing detailed information on various food items. Key data points include country and market specifics, price points (**low, high, open, close**), inflation rates, and trust indicators for each item.

To efficiently manage and access this large volume of data, it is stored in **AWS S3**. Real-time AWS services are used to establish a seamless workflow, allowing for on-demand data retrieval via **FastAPI** to support real-time analysis and decision-making.



## Approach

This project implemented a real-time data pipeline with the following steps:

1.  **Data Ingestion:**
    * A **FastAPI** application was developed to securely access the raw dataset stored in an **AWS S3 bucket**.
    * **AWS Kinesis Data Streams** captured real-time data from this API.

2.  **Data Transformation:**
    * **AWS Kinesis Firehose** processed the streaming data.
    * An **AWS Lambda** function was integrated with Firehose to transform the data into a standardized CSV format before loading it into a new S3 bucket.

3.  **Data Loading and Processing:**
    * **Snowpipe** was configured in **Snowflake** to automatically ingest the new CSV files from the S3 bucket.
    * **Snowpark** Python sessions, scheduled as stored procedures, were used to cleanse and transform the raw data within Snowflake.

4.  **Visualization:**
    * The cleaned and structured data was then loaded into **Power BI**.
    * Multiple reports were created to visualize key metrics, providing diverse and strategic insights into global market trends.
  


   
  
   <img width="1877" height="781" alt="image" src="https://github.com/user-attachments/assets/244aeb42-a09a-4354-80ce-383ed79beda9" /> <br> </br>
   
   



   ## Visualization Result:
   <p>
<img width="1597" height="836" hspace= "10" alt="Screenshot 2025-09-15 at 12 45 57 AM" style= "padding-bottom:20 px;border:none;" src="https://github.com/user-attachments/assets/cc755f64-bbf4-4d82-b47d-5bd6afbc2283" />
<p>  
<img width="1617" height="834" hspace="10" alt="Screenshot 2025-09-15 at 12 46 16 AM" src="https://github.com/user-attachments/assets/a53ff587-dd22-45cd-9e2c-735ac9068544" />
<p>

<img width="1607" height="834" hspace="10" alt="Screenshot 2025-09-15 at 12 46 55 AM" src="https://github.com/user-attachments/assets/0926ae7b-9e2e-4462-aa88-9d2cfa1d6422" />
<p>
<img width="1617" height="834" hspace="10" alt="Screenshot 2025-09-15 at 12 46 41 AM" src="https://github.com/user-attachments/assets/1c1175f8-9a7d-4afa-b62f-e65acc01200e" />





</p>






   
   

  
      
