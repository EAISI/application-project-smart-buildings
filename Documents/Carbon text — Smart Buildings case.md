**[ Video ]**

## The challenge
Smart buildings generate increasing amounts of sensor data. But how many sensors do we actually need to understand how a space is being used?

In this case, you will work with sensor data collected in an office environment by DataBuilt. Your challenge is to predict the number of coworkers present in a room based on indoor environmental sensing data, while minimizing the number of sensors and optimizing their position in the space.
  
Knowing how many people are present in a room is highly relevant for smart building control. It can support better use of resources such as energy and ventilation, while maintaining a comfortable indoor environment. In short: “air follows the coworker.” The fewer sensors needed to make a reliable prediction, the more scalable and cost-effective the solution becomes.

By the end of this project, you should be able to develop and evaluate machine learning models that estimate room occupancy from sensor data and provide practical recommendations on sensor placement, sensor selection and model generalizability.
  
## Background information
DataBuilt develops data-driven solutions for buildings, including Sensi: a compact sensor device that measures indoor environmental variables such as temperature, CO₂, relative humidity, motion and light intensity. These measurements help understand how spaces are used and how indoor climate systems can respond more intelligently.

In an experimental setting, DataBuilt collected data from multiple sensors installed in an office space. The sensors measured variables such as temperature, relative humidity, light and motion. During the same period, the actual number of coworkers present in the space was logged. This occupancy count is the response variable that you will try to predict.

The business relevance is clear: sensors and their operation cost money. Therefore, DataBuilt wants to understand how to use as few sensors as possible, while still predicting occupancy with acceptable accuracy. A single sensor in a well-chosen location may outperform multiple sensors in poor locations. Similarly, one type of measurement, such as CO₂, may be more predictive than another, such as motion, depending on where and how it is measured.

The first project focus is a larger office space. In addition, data is provided  from a smaller room, a meeting room, using fewer Sensi sensors. This allows you to compare dedicated models for different spaces and explore whether a more generic model can work across both.

In addition to the information provided: Project participants are welcome to visit the office space where the sensors were installed and the data was collected, providing valuable context for understanding the dataset and the sensor placement strategy.

## Project-based
This case is project-based. The business problem and data are provided, but there is room for exploration in how you define, prepare and model the data.

You will be working on a real smart-building challenge, with direct relevance for DataBuilt’s ambition to make building data more actionable, scalable and useful for energy-efficient and comfortable indoor environments.

## Several CRISP-DM cycle specifics and the objective
### Determine business objectives
The main business objective is to minimize the number of sensors and optimize their position in an office space, while still being able to predict the number of coworkers present in that space with acceptable accuracy.

More specifically, DataBuilt would like to know:
- Which sensor locations are most informative for predicting occupancy?
- Which measured variables, such as temperature, relative humidity, light, motion or CO₂, contribute most to prediction performance?
- What is the minimum number of sensors needed to achieve an acceptable prediction accuracy?
- Can a model trained for one room also be used for another room and/or other building?
- What accuracy is lost when moving from dedicated room-specific models to a more generic model?
- What practical lessons can be learned for future Sensi deployments in smart buildings?

### Determine data mining goals
Develop a machine learning model that can predict the number of coworkers present in a room using sensor data.

The project should address the following modelling goals:
- Build a dedicated occupancy prediction model for the larger office space.
- Build a dedicated occupancy prediction model for the smaller room.
- Investigate which sensor locations and sensor variables are most important for prediction.
- Explore whether comparable performance can be achieved with fewer sensors.
- Compare dedicated models with a more generic model that can be applied across both spaces.
- Quantify the trade-off between model simplicity, number of sensors and prediction performance.

Depending on the characteristics of the data, you may formulate this as a regression task, predicting the number of people in the room, or as a classification task, predicting occupancy categories.

### Data understanding
The available data consists of time-series sensor measurements and logged occupancy counts.

The sensor data  include variables such as:
- Temperature
- Relative humidity
- Light intensity
- Motion
- CO₂, if available for the relevant sensor set
- Timestamp information
- Sensor identifiers

The occupancy data contains logged counts of the number of coworkers present in the room during specific measurement periods. The available raw occupancy data covers several separate logging periods, including July, September and November. Participants should carefully inspect the timestamps, align sensor and occupancy data, and assess which periods can be used for modelling.

Important data understanding and preparation topics include:
- Checking timestamp formats and time zones
- Aligning sensor measurements with occupancy logs
- Handling missing values and irregular sampling intervals
- Understanding differences between raw, cleaned and non-merged datasets
- Deciding whether and how to aggregate sensor readings over time windows
- Investigating correlations between sensor variables, location and occupancy
- Avoiding data leakage when splitting time-series data into training and test sets

Participants are encouraged to perform their own data cleaning and preparation. Cleaned files are also provided as a starting point, but the data preparation choices should be made explicit and justified.

### Report
Your final report and presentation should include:
- A clear description of the business problem and data mining formulation.
- An explanation of how the sensor and occupancy data were prepared.
- A comparison of different modelling approaches.
- An evaluation of model performance using appropriate metrics.
- An analysis of which sensors, locations and variables contribute most to prediction performance.
- A recommendation on the minimum number of sensors and their preferred placement.
- If applicable, a comparison between dedicated room-specific models and a generic model.
- Practical advice for DataBuilt on how to improve future sensor deployments and data collection.

## Getting started
The data and supporting documents are available in the EAISI GitHub repository:
https://github.com/EAISI/application-project-smart-buildings

The repository contains sensor data, occupancy data and supporting documents such as background information about the Sensi sensor and a previous pilot study. These materials are intended to help you understand the experimental setup, the available variables and the practical context of this smart-building challenge.

## Attribution
© DataBuilt / EAISI. This case study was developed for educational purposes as part of the EAISI Applications of Data & AI programme.