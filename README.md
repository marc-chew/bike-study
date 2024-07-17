# Change Log for Cyclistic Bike Study

## Process for Cleaning Data

### Step 1: Access

* Downloaded data from Cyclistic Website
* License for usage found [here](https://divvybikes.com/data-license-agreement)

### Step 2: Upload to Google Cloud

* Uploaded 12 months of data to Google Cloud for storage
* Data Loss Check - Spot Checked 3 datasets and confirmed row #s were the same - 202306, 202312, 202406
* Data Aggregation: Aggregated all data into a single table in BigQuery - see **prepare_aggregation**

### Step 3: Cleaning Process
I used the following checklist for confirming data was accurate, usable, and clean:

1. Removed Duplicates - see **remove_duplicates**
2. Remove Extra Spaces & Blanks see **trimming**
3. Remove Extremely low outliers - see **see rides < 1 sec** (220 records)
4. Identify unformatted data
    1. Transform Date to usable Format see **datetime_formatting**
5. Dataset Overview
    1. Time Frame: 2023-06 to 2024-06
    2. Total Records: 6,451,762
6. General Analysis

   Ride Length by minutes split by Rider Type:

|          | Avg  | Max     | Min |
|----------|------|---------|-----|
| Casual   | 28.09| 98489   | 0.02|
| Member   | 13.02| 1559.8  | 0.02|
| Combined | 18.5 | 98489   | 0.02|

7. **Average Ride Length by Day**

 | Day of Week | Avg Ride Length (seconds) | Avg Ride Length (minutes) |
|-------------|---------------------------|---------------------------|
| Sunday      |                      1371 | 22.85                     |
| Saturday    |                      1345 | 22.42                     |
| Friday      |                      1094 | 18.23                     |
| Monday      |                      1040 | 17.33                     |
| Wednesday   |                       970 | 16.16                     |
| Tuesday     |                       969 | 16.14                     |
| Thursday    |                       969 | 16.15                     |

6. **Average Ride Length by Day**

### STEP 4: Analyze

Data has been saved in table: bike_share_analyze

We will test the following hypotheses:

- Do Members/Casuals prefer a certain bike type?
- Do Members/Casuals ride on a certain day? month?
- Do Members/Casuals tend to rent at a specific location or end at a specific location?
- Do Members/Casuals ride for a longer or shorter duration? 
