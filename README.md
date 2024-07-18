# Change Log for Cyclistic Bike Study: Data Processing & Analysis

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
6. **Average Ride Length by Day**

| Day of Week | Avg Ride Length (minutes) |
|:-----------:|:-------------------------:|
| Sunday      | 22.85                     |
| Saturday    | 22.42                     |
| Friday      | 18.23                     |
| Monday      | 17.33                     |
| Wednesday   | 16.16                     |
| Tuesday     | 16.14                     |
| Thursday    | 16.15                     |

7. **Average Ride Length by Month**

| Day of Week | Avg Ride Length (minutes) |
|:-----------:|:-------------------------:|
| Sunday      | 22.85                     |
| Saturday    | 22.42                     |
| Friday      | 18.23                     |
| Monday      | 17.33                     |
| Wednesday   | 16.16                     |
| Tuesday     | 16.14                     |
| Thursday    | 16.15                     |

