# Azure Data Factory Pipeline - NY Taxi Data

---

## Overview  
This Azure Data Factory (ADF) pipeline iterates 12 times, retrieving monthly parquet files from an external source and dynamically adjusting the file path based on the iteration index.

---

## Pipeline Architecture  
<div align="center">
    <img src="https://raw.githubusercontent.com/juancarlosierrac/NYTaxi-DataEngineeringProject/main/images/ADF_NYTaxi_Project.png" width="800px"/>
</div>

---

## Process Flow  
1. ForEach Activity: Iterates 12 times using `@range(1, 12)`, dynamically adjusting the file path to fetch data from January to December 2023.
2. If Condition Activity: Determines whether the iteration index is greater than 9.
   - If False (Months 1-9): The pipeline retrieves files with a leading zero in the month format (e.g., `green_tripdata_2023-01.parquet`).
   - If True (Months 10-12): The leading zero is omitted (e.g., `green_tripdata_2023-10.parquet`).
3. Copy Data Activity: Transfers the data from the source URL:
   ```
   https://d37ci6vzurychx.cloudfront.net/trip-data/green_tripdata_2023-XX.parquet
   ```
   to the designated storage in Azure Data Lake.