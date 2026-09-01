# Smart Buildings

## Occupancy prediction and sensor optimization in office environments

Participants will work on a real-world smart building challenge using environmental sensor data collected in an office environment. The objective is to investigate how accurately room occupancy can be predicted from sensor measurements while minimizing the number of sensors required and optimizing their placement in the office space. This challenge combines building performance, sensor analytics and machine learning.

Group project participants are welcome to visit the office space where the sensors were installed and the data was collected, providing valuable context for understanding the dataset and the sensor placement strategy.

## Background

Modern buildings increasingly rely on sensor networks to improve indoor environmental quality, occupant comfort and energy efficiency. Occupancy information plays an important role in these applications. If building systems know how many people are present in a space, heating, cooling, and ventilation can be adjusted accordingly.

[DataBuilt](https://databuilt.nl/) has developed the [Sensi sensor platform](https://www.sensi-sensoren.nl/) for indoor environmental monitoring. In an experimental office environment, multiple sensors were deployed to measure environmental conditions while the number of occupants in the space was logged separately.

The central question in this case is:
> Can we accurately predict room occupancy using environmental sensor measurements, and what is the minimum sensor configuration required to do so?

## Case Assignment

### Business Understanding

To guide model development and evaluation, the project addresses the following core questions:

* **Sensor Placement**: Which physical sensor locations are most informative for predicting room occupancy?

* **Feature Importance**: Which environmental variables (e.g., temperature, relative humidity, light, motion, or CO₂) contribute most to predictive accuracy?

* **Minimal Footprint**: What is the minimum number of sensors required to maintain an acceptable level of prediction performance?

* **Model Generalizability**: Can a model trained on one specific room generalize to a different room or building layout?

* **Model Performance Trade-off**: What performance drop occurs when transitioning from room-specific models to a single, generic model?

* **Sensor Deployment Insights**: What actionable guidelines can be derived for future Sensi sensor installations in smart buildings?

### Data Understanding

To lay a solid foundation for modeling, you must inspect and analyze the raw datasets with a focus on:

* **Data Quality Audit**: Identifying missing values, sensor dropouts, outliers, and irregular sampling intervals across different Sensi devices.

* **Temporal Discrepancies**: Inspecting timestamp formats, time zones, and sampling frequencies between continuous sensor streams and discrete occupancy logs.

* **Exploratory Data Analysis (EDA)**: Investigating multi-sensor correlations, spatial variations across sensor locations, and lag effects between sensor spikes (e.g., CO₂ buildup) and actual occupancy.

* **Time-Series Integrity Assessment**: Examining temporal boundaries and logging periods to plan leak-free validation strategies (e.g., temporal splitting vs. random k-fold).

### Data Preparation

You are expected to drive the entire end-to-end pipeline—from raw data processing to model-ready features. All custom preparation choices must be explicitly documented and justified in your interim and final reports.

There is no prescribed workflow, but your preparation pipeline should address:

* **Data Cleaning & Filtering**: Handling missing values, smoothing sensor noise, and resolving irregular sampling intervals identified during data understanding.

* **Time Synchronization & Resampling**: Converting raw, unaligned timestamps into unified, regularly sampled time windows matching the occupancy log frequency.

* **Feature Engineering**: Creating domain-specific features, such as rate-of-change indicators, moving averages, spatial aggregations across sensor locations, and lag features (e.g., CO2 accumulation trends).

* **Dataset Construction**: Formatting final feature matrices and establishing time-aware train/validation/test splits to strictly prevent data leakage.

### Modeling

Depending on your exploratory data analysis and target application, you may recommend that the case owner formulate the problem as either:

* **Regression**: Predicting the continuous or discrete exact count of occupants in the room (e.g., 0,1,2,3,…).

* **Classification**: Predicting broader occupancy states or capacity bands (e.g., Empty, Low, Medium, High).

Justify your choice between regression and classification, explaining how your selected task formulation aligns with both the data characteristics and the business requirements.

The focus extends beyond predictive performance to generating actionable recommendations for future sensor deployments.

## Repository Structure

```text

application-project-smart-buildings/
|
├── code/
│   ├── main.py
│   ├── hassebassie.py
│   └── utils_project/
├── documents/
│   ├── sensor/
│   │   ├── sensor_placement_WorkroomSTUDY.pdf
│   │   └── sensor manuals/
│   ├── space/
│   │   └── floor plans and room drawings
│   ├── 2026 05 08 - Brightlands-Campus-map.pdf
│   └── HIA occuSensi_case study.pptx
├── pyproject.toml
└── README.md

```

## Dataset

The data will be made available to the participants working on group project "Smart Buildings" through the private repo [Smart Buildings - Data](https://github.com/EAISI/application-project-smart-buildings-data/tree/main)

## Supporting Documents
Several supporting documents are provided to help you understand the context of the case.

### Sensor Documentation
Inside the `documents/sensor/` directory, you will find sensor documentation including placement details, user manuals, and technical datasheets.

### Space Documentation
The `documents/space/` directory contains space documentation such as floor plans, room layouts, and spatial context for the measurement environments.

### Previous Pilot Study
The presentation file `documents/HIA occuSensi_case study.pptx` provides background information from an earlier pilot study, outlining previous experiments, sensor placement decisions, and lessons learned. Please note that this presentation describes prior work and should be used as supporting context rather than the instructions for the assignment itself.

## Report
Your report and presentation should include:
- A clear description of the business problem and data mining formulation.
- An explanation of how the sensor and occupancy data were prepared.
- A comparison of different modelling approaches.
- An evaluation of model performance using appropriate metrics.
- An analysis of which sensors, locations and variables contribute most to prediction performance.
- A recommendation on the minimum number of sensors and their preferred placement.
- If applicable, a comparison between dedicated room-specific models and a generic model.
- Practical advice for DataBuilt on how to improve future sensor deployments and data collection.

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
1. Review the supporting documents in the `documents\` directory.
2. Explore the occupancy data in the `occupancy_log\` directory.
3. Inspect the individual sensor datasets in the `clean_nomerge\` directory.
4. Understand the relationship between sensors, locations and occupancy measurements.
5. Build a baseline model before experimenting with more advanced approaches.

## Copyright and License
© DataBuilt / EAISI

The 'Smart Buildings' group project was developed for educational purposes in close collaboration with DataBuilt as part of EAISI Academy's *Applications of Data & AI program*.
