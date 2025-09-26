
# Traffic Accident Analysis Project

## Project Description
This project analyzes traffic accident data spanning approximately 10 years from an unspecified location. Traffic accidents are a significant cause of preventable deaths and losses globally. The goal of this analysis is to understand the primary factors contributing to accidents—such as road defects, weather conditions, or driver behavior—in order to identify key areas for improving public safety and reducing fatalities.

The dataset for this analysis was sourced from Kaggle: https://www.kaggle.com/datasets/oktayrdeki/traffic-accidents 


## Data Dictionary
The analysis is based on several interconnected data tables:

CRASHES TABLE:
* `SERIALNO/CASEID`: Unique ID for each recorded incident.
* `DAMAGERANGE`: The extent of damage caused by the accident.
* `INJURYTYPE`: The type of injury sustained (e.g., Incapacitating, Non-Incapacitating).
* `PRIMARYCONTRIBUTORYCAUSE`: The main cause of the crash.
* `TOTALINJURIES`: Total number of injuries reported in the incident.
* `NUMBEROFVEHICLES`: The number of vehicles involved.

ROADTYPES TABLE:
* `ALIGNMENT`: The alignment of the road where the accident happened (e.g., straight, curved).
* `CRASHTYPE`: The type of crash (e.g., head-on, rear-end).
* `TRAFFICWAYTYPE`: The type of roadway involved (e.g., highway, local road).

WEATHERROADCONDITIONS TABLE:
* `WEATHERCONDITION`: Weather conditions at the time of the crash.
* `LIGHTINGCONDITION`: Lighting conditions at the time of the crash.
* `ROADWAYSURFACE`: The condition of the road surface (e.g., dry, wet).
* `ROADDEFECT`: Any defects present on the road.

YEARTIMEMΟNΤΗ ΤABLE:
* `CRASHHOUR`: The hour when the accident took place.
* `CRASHDAY`: The day of the week the accident occurred .
* `CRASHMONTHNumber`: The month in which the accident happened .

*
## Data Cleaning and Preparation
Several steps were taken to clean and prepare the data for analysis:
* An index column was added to serve as a primary key.
* Multiple columns containing redundant data were removed. For example, injury types were consolidated from five separate columns.
* Multi-valued categorical names were simplified . For instance, 'DARKNESS, LIGHTED ROAD' in the `LIGHTINGCONDITION` column was changed to 'LIGHTED' to facilitate easier analysis .
* Unclear column names with underscore characters were renamed for clarity.
* Unnecessary columns, such as separate date and time columns with repeated information, were removed. Time details were classified into 'AM'/'PM' to make the data more intuitive.

*
## Key Analyses and Insights

### 1. Pedestrian Crashes
* Timing and Danger: Injuries involving pedestrians spike between 3 p.m. and 7 p.m.
* Severity: From 2017 to 2024, pedestrian-related accidents caused damage to over 17,000 vehicles, with nearly one injury recorded per incident (0.96), indicating their severity .
* Primary Cause: The leading cause of pedestrian injuries is drivers "Failing to Yield Right-of-Way" (49.93%) .
* Hotspots: Most pedestrian injuries occur at T-intersections, one-way streets, and divided roads .

### 2. The Surprising Risk of "Good" Road Conditions
* Counterintuitive Findings: Over an 8-year span, more injuries occurred under "GOOD" road conditions compared to "BAD" ones. This suggests that good conditions may lead to riskier driving behaviors .
* Injury Trends: While accident rates stabilized after 2021, injuries have continued to rise by about 1,000 per year, indicating more severe consequences.
* Severity: The average number of injuries per crash is slightly higher on "GOOD" roads (0.40) than on "BAD" roads (0.39).

### 3. Head-On Collisions
* High Severity: Head-on collisions result in double the percentage of fatal and incapacitating injuries compared to other crash types. The injury rate is 0.71, twice that of non-head-on crashes.
* Financial Impact: These collisions are associated with heavier expenses, with 84% falling into the "heavy expense" category compared to 70% for other crashes.
* Timing: Injuries from head-on collisions peak around 3 p.m. and decline into the night.

### 4. Severe Injuries: Weekdays vs. Weekends
* Increased Weekend Risk: Weekends are approximately 20.5% riskier than weekdays for severe injuries. Weekends account for 3.8% of severe injuries, while weekdays account for 3.14%.
* Timing: The rate of severe injuries is highest between 12 a.m. and 5 a.m., and rises again after 6 p.m.
* Top Causes on Weekends: Leading causes for severe injuries on weekends include speeding, alcohol/drug influence, and incidents related to bus stops .

### 5. "Sensitive Roads" (Junctions and Dividers)
* Higher Risk: "Sensitive roads" like intersections and four-way junctions are considered higher-risk due to complex vehicle movements.
* Injury Rate: These roads have 10% more crashes than other roads, but the injuries are 41% higher, resulting in approximately 43 injuries for every 100 crashes .
* Cost: Crashes on sensitive roads are more likely to result in heavy expenses (74%) compared to non-sensitive roads (67%).

### 6. Monthly and Seasonal Trends
* Peak Crash Times: Crash volumes are consistently higher in the second half of the year, with October being the riskiest month.
* Weather Impact: Adverse weather is a major contributor, with rain dominating the last quarter of the year and snow leading in the first two months . About 70% of injuries in the top 6 injury-heavy months occurred during rainy conditions.

*
## Overall Conclusions and Recommendations
The analysis reveals that traffic accidents and resulting injuries have not shown a positive downward trend over the years, suggesting that current transportation safety measures may be insufficient. Reckless driver behavior appears to be a primary factor in most accident scenarios.

Based on the findings, the following recommendations are proposed:
* Infrastructure Improvements: Design smarter barriers, signals, and speed breakers, especially on curved roads, to mitigate risks in adverse weather.
* Enhanced Visibility: During rainy conditions, invest in illuminated road borders and consider reducing speed limits significantly.
* Combat Overconfidence: Launch awareness campaigns to address the higher injury rates in good weather and enforce laws against reckless driving, signal violations, and drunk driving.
* Pedestrian Safety: Increase the frequency of crosswalk signals between 3 p.m. and 7 p.m. at intersections and four-way roads to reduce pedestrian-related injuries.
* Driver Accountability: Enhance the vetting process for obtaining a driver's license and shorten renewal intervals to ensure ongoing driver competence.
* Increased Enforcement: Increase night-time police checks to address the late-night spikes in severe injuries.
