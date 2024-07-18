### Cyclistic Bike Case Study: Analysis

*NOTE: Data has been saved in table bike_share_analyze*

To answer the business objective of:
*How do annual members and casual riders use Cyclistic bikes differently?*

We will test the following hypotheses:

- Do Members/Casuals prefer a certain bike type?
- Do Members/Casuals ride on a certain day? month?
- Do Members/Casuals tend to rent at a specific location or end at a specific location?
- Do Members/Casuals ride for a longer or shorter duration?


#### Do Members/Casuals prefer a certain bike type?

Findings: 
- Members rode Classic Bikes 50% of the time and Electric Bikes 50% of the time last year
- Casual Users used electric bikes slightly more (52%%) than classic bikes (46%) with a small usage of docked bikes
- The docked bikes could be attributed to accessibility users 

| **User** | **Bike Type** | **Rides** |
|----------|---------------|-----------|
| member   | classic_bike  |   2086240 |
| member   | electric_bike |   2015884 |
| casual   | electric_bike |   1219429 |
| casual   | classic_bike  |   1080854 |
| casual   | docked_bike   |     49355 |

#### Do Members/Casuals ride on a certain day? month?

Findings: 
- Members bike usage on average is 18% higher on **weekdays** than on **weekends**
- Casual users on average is 35% higher on **weekends** than on **weekdays**
- Members used bikes most frequently mid-week on Thursday, Wednesday, and Tuesday
- Casual users used bikes most frequently toward the end of the week on Friday, Saturday, and Sunday
- Summer has the highest volume of rides for both Members and Casual Users
- Winter has the lowest volume of rides for both Members and Casual Users

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

#### Do Members/Casuals tend to rent at a specific location or end at a specific location?

Findings:

- Steeter Dr & Grand Ave was the most frequented start station for Casual Users
- Clinton Streets two stations were both in the top five for Members

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

#### Do Members/Casuals ride for a longer or shorter duration?

Findings:

- Casual Users have a longer average riding duration than Members

|   User   | Avg  | Max     | Min |
|----------|------|---------|-----|
| Casual   | 28.09| 98489   | 0.02|
| Member   | 13.02| 1559.8  | 0.02|
| Combined | 18.5 | 98489   | 0.02|
