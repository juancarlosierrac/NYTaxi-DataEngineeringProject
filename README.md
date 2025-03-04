# **NYC Taxi Data Pipeline with Azure**  

## **Introduction**  
This project implements a data engineering pipeline on Microsoft Azure to process and analyze NYC Taxi trip data. The solution ingests raw data via an API, stores it in Azure Data Lake, transforms it using Delta Lake and Parquet format, and makes it available for reporting in Power BI.  

---

## **Project Overview**  
The project follows a modern data architecture approach, integrating Azure Data Factory for ingestion, Azure Data Lake Gen2 for storage, and Delta Lake for efficient data transformation. The final dataset is optimized for reporting and business intelligence.  

---

## **Architecture**  
<div align="center">
    <img src="https://raw.githubusercontent.com/juancarlosierrac/NYTaxi-DataEngineeringProject/main/images/NY_Taxi_Project.png" 
         alt="NYC Taxi Data Pipeline Architecture" 
         width="800px"/>
</div>  

---

## **Objective**  
Develop an end-to-end data pipeline that extracts taxi trip data from an external API, stores and processes it in Azure Data Lake using Delta Lake, and prepares it for analysis and visualization in Power BI.  

---

## **Technologies Used**  
- Azure Data Factory  
- Azure Data Lake Gen2  
- Parquet  
- Delta Lake  
- Power BI  
- Azure Security  

---

This project was developed as a hands-on learning experience in cloud data engineering, inspired by educational resources and best practices in the field by Ansh Lamba.
