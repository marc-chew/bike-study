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

### STEP 4: Analyze

Data has been saved in table: bike_share_analyze

We will test the following hypotheses:

- Do Members/Casuals prefer a certain bike type?

| **User** | **Bike Type** | **Rides** |
|----------|---------------|-----------|
| member   | classic_bike  |   2086240 |
| member   | electric_bike |   2015884 |
| casual   | electric_bike |   1219429 |
| casual   | classic_bike  |   1080854 |
| casual   | docked_bike   |     49355 |

- Do Members/Casuals ride on a certain day? month?

| **Day**   | **User** | **Rides** | **Percent of Total** |
|-----------|----------|-----------|----------------------|
| Thursday  | member   |    658218 |                 10.2 |
| Wednesday | member   |    652783 |                 10.1 |
| Tuesday   | member   |    623693 |                  9.7 |
| Friday    | member   |    593879 |                  9.2 |
| Monday    | member   |    564499 |                  8.7 |
| Saturday  | member   |    542445 |                  8.4 |
| Saturday  | casual   |    487042 |                  7.5 |
| Sunday    | member   |    466607 |                  7.2 |
| Sunday    | casual   |    399790 |                  6.2 |
| Friday    | casual   |    351531 |                  5.4 |
| Thursday  | casual   |    296412 |                  4.6 |
| Wednesday | casual   |    281544 |                  4.4 |
| Monday    | casual   |    269307 |                  4.2 |
| Tuesday   | casual   |    264012 |                  4.1 |


| **Month** | **User** | **Rides** | **Percent of Total** |
|-----------|----------|-----------|----------------------|
| June      | member   |    827748 |                 12.8 |
| June      | casual   |    602087 |                  9.3 |
| August    | member   |    460430 |                  7.1 |
| July      | member   |    436185 |                  6.8 |
| September | member   |    404617 |                  6.3 |
| May       | member   |    378317 |                  5.9 |
| October   | member   |    359947 |                  5.6 |
| July      | casual   |    331252 |                  5.1 |
| August    | casual   |    311006 |                  4.8 |
| April     | member   |    283092 |                  4.4 |
| November  | member   |    264042 |                  4.1 |
| September | casual   |    261534 |                  4.1 |
| May       | casual   |    230915 |                  3.6 |
| March     | member   |    219081 |                  3.4 |
| October   | casual   |    177007 |                  2.7 |
| February  | member   |    175979 |                  2.7 |
| December  | member   |    172356 |                  2.7 |
| April     | casual   |    131745 |                    2 |
| January   | member   |    120330 |                  1.9 |
| November  | casual   |     98327 |                  1.5 |
| March     | casual   |     82500 |                  1.3 |
| December  | casual   |     51662 |                  0.8 |
| February  | casual   |     47157 |                  0.7 |
| January   | casual   |     24446 |                  0.4 |

- Do Members/Casuals tend to rent at a specific location or end at a specific location?

| **User** | **Start Station Name**             | **Rides** |
|----------|------------------------------------|-----------|
| casual   | Streeter Dr & Grand Ave            | 54406     |
| casual   | DuSable Lake Shore Dr & Monroe St  | 36703     |
| member   | Clinton St & Washington Blvd       | 30331     |
| member   | Kingsbury St & Kinzie St           | 29730     |
| member   | Clark St & Elm St                  | 27544     |
| casual   | Michigan Ave & Oak St              | 27285     |
| casual   | DuSable Lake Shore Dr & North Blvd | 25207     |
| member   | Clinton St & Madison St            | 24688     |
| member   | Wells St & Concord Ln              | 23412     |
| casual   | Millennium Park                    | 23326     |

- Do Members/Casuals ride for a longer or shorter duration?

|   User   | Avg  | Max     | Min |
|----------|------|---------|-----|
| Casual   | 28.09| 98489   | 0.02|
| Member   | 13.02| 1559.8  | 0.02|
| Combined | 18.5 | 98489   | 0.02|
