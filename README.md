# Change Log for Cyclistic Bike Study

## Process for Cleaning Data

### Step 1: Access

* Downloaded data from Cyclistic Website
* License for usage found here

### Step 2: Upload to Google Cloud

* Uploaded 12 csv files to Google Cloud for storage
* Created tables in BigQuery
* Data Loss Check - Spot Checked 3 datasets and confirmed row #s were the same - 202306, 202312, 202406
* Data Aggregation - Combined all data

CREATE OR REPLACE TABLE  bike-429016.bike_share_chicago.bike_share_analysis AS
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202306`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202307`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202308`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202309`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202310`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202311`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202312`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202401`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202402`
UNION ALL
SELECT * FROM `bike-429016.bike_share_chicago.bike_share_202403`
UNION ALL


### Step 3: Cleaning Process
