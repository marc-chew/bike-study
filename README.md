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
3. Transform Date to usable Format see **datetime_formatting**
