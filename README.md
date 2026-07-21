# EAISI Smart Buildings

## A data science case study on occupancy prediction and sensor optimization in office environments
This case study was developed for the EAISI Applications of Data & AI programme in collaboration with DataBuilt.

Participants will work on a real-world smart building challenge using environmental sensor data collected in an office environment. The objective is to investigate how accurately room occupancy can be predicted from sensor measurements while minimizing the number of sensors required and optimizing their placement.

Project participants are welcome to visit the office space where the sensors were installed and the data was collected, providing valuable context for understanding the dataset and the sensor placement strategy.

## Background
Modern buildings increasingly rely on sensor networks to improve indoor environmental quality, occupant comfort and energy efficiency. Occupancy information plays an important role in these applications. If building systems know how many people are present in a space, heating, cooling, and ventilation can be adjusted accordingly.

[DataBuilt](https://databuilt.nl/) has developed the [Sensi sensor platform](https://www.sensi-sensoren.nl/) for indoor environmental monitoring. In an experimental office environment, multiple sensors were deployed to measure environmental conditions while the number of occupants in the space was logged separately.

The central question in this case is:
> Can we accurately predict room occupancy using environmental sensor measurements, and what is the minimum sensor configuration required to do so?

This challenge combines building performance, sensor analytics and machine learning.

## Case Assignment
### Business Objective
Develop a predictive model that estimates occupancy in an office space using environmental sensor data.

The ultimate goal is to identify:
- Which sensor measurements contribute most to occupancy prediction.
- Which sensor locations are most informative.
- How many sensors are actually required.
- Whether comparable performance can be achieved with fewer sensors.
- How sensor placement influences model performance.

### Additional Objectives
Participants are encouraged to explore different problem formulations. 

Possible approaches include:
- Predicting the exact number of occupants (regression).
- Predicting occupancy categories (classification).
- Comparing the performance of both approaches.
- Investigating the trade-off between model complexity, prediction performance and number of sensors.
- Improving trust in the model by developing inherently interpretable machine learning models or applying post-hoc explainability methods like SHAP.
- [LOES - Deployment / dashboard]

Participants are free to choose the approach that best addresses the business question and to justify their choices.


## User Guide
This project follows the CRISP-DM methodology:
1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modelling
5. Evaluation
6. Deployment
   
Participants are expected to perform their own data exploration, cleaning, feature engineering and model development.

The focus is not only on predictive performance but also on generating actionable recommendations for future sensor deployments.

## Repository Structure

```text

application-project-smart-buildings/

│

├── Code/

│   ├── main.py

│   ├── hassebassie.py

│   └── utils_project/

│

├── Data/

│   ├── Raw/

│   │   └── WorkroomData_RAW.csv

│   │

│   ├── Clean_nomerge/

│   │   ├── CEIL1.csv

│   │   ├── CEIL2.csv

│   │   ├── IEQ1WR.csv

│   │   ├── IEQ2WR.csv

│   │   ├── IEQ3WR.csv

│   │   ├── IEQ4WR.csv

│   │   ├── WR1.csv ... WR8.csv

│   │   ├── WR_responses.csv

│   │   └── workroom_F.ipynb

│   │

│   ├── Clean_merged_to_use/

│   │   └── WorkroomData_clean.csv

│   │

│   └── WorkroomData_clean.xlsx

│

├── Documents/

│   ├── Sensor/

│   │   ├── sensor_placement_WorkroomSTUDY.pdf

│   │   └── sensor manuals/

│   │

│   ├── Space/

│   │   └── floor plans and room drawings

│   │

│   ├── HIA occuSensi_case study.pptx

│   └── 2026 05 08 - Brightlands-Campus-map.pdf

│

└── README.md

```

## Dataset
### Sensor Data
The repository contains measurements collected from multiple sensors placed throughout an office environment.

Available variables include:
- Temperature
- CO₂ concentration
- Relative humidity
- Motion
- Light intensity
- Timestamp information
  
The `Clean_nomerge` folder contains individual sensor exports and should be considered the primary data source for most analyses.

### Occupancy Data
The occupancy measurements represent the target variable for the project.
Raw occupancy observations are available in:

```text

Data/Raw/WorkroomData_RAW.csv

```

A cleaned occupancy dataset is also provided.

### Data Preparation
Data cleaning and preparation are intentionally included as part of the assignment.
Participants are encouraged to:
- Investigate data quality.
- Align timestamps across datasets.
- Handle missing values.
- Justify cleaning decisions.
- Document all preparation steps.
  
There is no prescribed workflow.

## Supporting Documents
Several documents are included to help understand the case context:

### Sensor Documentation
Located in:

```text

Documents/Sensor/

```

Including:
- Sensor placement information
- Sensor manuals
- Technical datasheets

### Space Documentation
Located in:

```text

Documents/Space/

```

Including:
- Floor plans
- Room layouts
- Spatial context of the measurement environment

### Previous Pilot Study
The presentation:

```text

Documents/HIA occuSensi_case study.pptx

```

contains background information about earlier experiments, sensor placement decisions and lessons learned.

Note that this presentation describes previous pilot study and should be considered supporting context rather than the assignment itself.

## Expected Deliverables
At the end of the project participants should be able to:
- Develop a predictive occupancy model.
- Compare alternative modelling approaches.
- Evaluate the influence of sensor location and sensor type.
- Identify opportunities for sensor reduction.
- Provide recommendations for future sensor deployments.
- Translate analytical findings into practical business insights.

## Getting Started
Recommended starting steps:
1. Review the supporting documents in the `Documents` folder.
2. Explore the occupancy data in the `Raw` folder.
3. Inspect the individual sensor datasets in `Clean_nomerge`.
4. Understand the relationship between sensors, locations and occupancy measurements.
5. Build a baseline model before experimenting with more advanced approaches.

## Copyright and License
© DataBuilt / EAISI

This case study was developed for educational purposes as part of the EAISI Applications of Data & AI programme.
