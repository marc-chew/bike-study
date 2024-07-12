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
3. Identify unformatted data
    1. Transform Date to usable Format see **datetime_formatting**
4. General Analysis
    1. Time Frame: 2023-06 to 2024-06
    2. Total Records: 6,451,982
    3. **Average Ride Length**
    4. **Max Ride Length**
    5. **Minimum Ride Length**
  
### STEP 4: Analyze

We will test the following hypotheses:

- Do Members/Casuals prefer a certain bike type?
- Do Members/Casuals ride on a certain day? month?
- Do Members/Casuals tend to rent at a specific location or end at a specific location?
- Do Members/Casuals ride for a longer or shorter duration? 
