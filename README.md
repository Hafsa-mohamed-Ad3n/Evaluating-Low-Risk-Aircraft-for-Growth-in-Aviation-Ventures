# Evaluating Low-Risk Aircraft for Growth in Aviation Ventures

![Aircraft Image](Images/airplane.jpg)

## Business Problem
 As part of its strategy to diversify operations, the company is expanding into the aviation industry with plans to purchase and operate aircraft for both commercial and private purposes. However, the organization currently lacks domain knowledge about the risks associated with different aircraft types. To support the new aviation division, this project analyzes National Transportation Safety Board (NTSB) Aviation Accident data to identify aircraft models with the lowest risk profiles in terms of operational safety and performance.


## Data Understanding

### Data Source  
The dataset was sourced from the [National Transportation Safety Board](https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses) via Kaggle and contains historical aviation safety records of incidents and accidents involving various aircraft types, starting from 1962.

### Data Preparation
To ensure the data reflected modern aviation standards, records from **2012 to 2022** were selected. Given the significant evolution in aviation technology, safety practices, and regulations since 1962, older records may not accurately represent current industry realities.  

The dataset was also cleaned to remove:
- Inconsistencies  
- Incomplete entries (Dropped columns that had missing value >30%) 
- Irrelevant fields (such as `Latitude`, `Longitude`, `Airport Code`, and `Airport Name`)  

These fields were dropped because they were missing large amount of data and the analysis did not focus on location-based patterns. This cleaning process enhanced the overall quality and relevance of the dataset for assessing aircraft risk.

### Objectives
This project aims to:
- Determine aircraft models with the lowest operational risk
- Examine historical aviation incident data, including aircraft types and contributing operational factors
- Deliver clear, data-driven recommendations to support the aviation division in selecting aircraft for initial investment
- Reduce potential liabilities and support a safer, more informed entry into the aviation sector


### Key Variables Used in the Analysis

The following variables were identified as most relevant for assessing aircraft safety and operational risk:

- **Make and Model**: Specifies the manufacturer and model of the aircraft.
- **Injury Severity**: Indicates whether the accident resulted in fatal or non-fatal injuries.
- **Total Fatal Injuries**: The number of fatalities per accident.
- **Total Serious Injuries**: The number of serious injuries per accident.
- **Meteorological Conditions**: Specifies whether the accident occurred under Visual Meteorological Conditions (VMC) or Instrument Meteorological Conditions (IMC).
- **Engine Type**: Type of engine powering the aircraft (e.g., Reciprocating, Turbo Shaft, Turbo Prop, Turbo Fan).
- **Number of Engines**: The number of engines on the aircraft.
- **Registration Number**: A unique identifier for each aircraft which helps track individual incident records.
- **Purpose of Flight**: Describes the intended use of the aircraft during the incident (personal, business, instructional), offering insight into usage patterns and associated risk.
- **Year**: Extracted from the `Event_Date` column to facilitate time-based trend analysis.

### Relevance to Analysis
The selected variables provides valuable insights into accident trends, fatality rates, and aircraft damage levels. These insights are relevant to assessing the likelihood and severity of aviation incidents, as well as factors that influence aircraft performance and safety.

## Analysis Overview
To assess the **severity and patterns of aircraft accidents**, we performed the following:

- Created **additional derived columns** to classify the level of risk (*High Risk* or *Low Risk*) based on variables helped evaluate whether a specific aircraft model posed a greater operational risk.
- Conducted trend analyses of:
  - Injury severity (Fatal, Serious, Minor, None)
  - Accident frequency over time (2012–2022)
  - Trends in fatalities and uninjured passengers over the years

I also analyzed factors that influence aircraft safety:
- Engine reliability: by assessing the frequency and severity of accidents across different engine types (Turbo Prop vs. Turbo Fan).
- Aircraft configuration: including make, model, registration number, engine type, and number of engines.
- Purpose of flight: understanding whether certain flight types (business, personal) are associated with higher accident risks.

I also explored accident counts per Make & Model combinations to determine which aircraft were most frequently involved in accidents, especially those with fatal outcomes. This helped identify models associated with higher risk profiles.

For a detailed breakdown of the analysis, please refer to the full notebook: [Aviation.ipynb](https://github.com/Hafsa-mohamed-Ad3n/Evaluating-Low-Risk-Aircraft-for-Growth-in-Aviation-Ventures/blob/main/aviation.ipynb)






