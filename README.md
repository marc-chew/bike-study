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
5. General Analysis
    1. Time Frame: 2023-06 to 2024-06
    2. Total Records: 6,451,762
    3. **Average Ride Length:** 1110 seconds
    4. **Max Ride Length:** 5909344 seconds  
    5. **Minimum Ride Length:** 1 second
    6. **Average Ride Length Members:** 781 seconds
    7. **Average Ride Length Casual:** 1685 seconds

  
### STEP 4: Analyze

Data has been saved in table: bike_share_analyze

We will test the following hypotheses:

- Do Members/Casuals prefer a certain bike type?
- Do Members/Casuals ride on a certain day? month?
- Do Members/Casuals tend to rent at a specific location or end at a specific location?
- Do Members/Casuals ride for a longer or shorter duration? 
