# nasa-neo-R

# The Great Space Race to Save the Earth

[Check Out The Notebook Here!](https://brandontnavarrete.github.io/Brandons-R-Markdown/)

A Near Earth Object Classification project by Brandon Navarrete

  # :earth_americas: Goal

Humanity has forgotten how fragile we live. It would be wise to keep an eye to the stary abyss and determine if a near earth object has the potential to be hazardous.
With world climate becoming ever changing, we have lost sight on protecting the one resource we all share. EARTH.

* Here I will develop a model that can classify hazardous asteroids given their respective features of `diameter`, `magnitude`, and `velocity`

* This will be encompassed in a report that is easy to read and interpret to any viewers.


## :world_map: Data Overview

* This data was pulled from kaggle(2023) which has been pulled from NASA's API

* 90836 rows, each it's own object or asteroids with 10 columns of its features


# Initial Questions
* How Many of our Objects Are Inert?

* Will Diameter play a Big Difference in Determining Hazard Status

* Will Relative Velocity play a Big Difference in Determining Hazard Status

* Will Absolute Magnitude play a Big Difference in Determining Hazard Status

# Data Dictionary

## :open_file_folder:   Data Dictionary
**Variable** |    **Value**    | **Meaning**
---|---|---
*ID* | numerical | Unique Identifier for each Asteroid
*Name* | string | Name given by NASA
*est_diameter_min* | Float | Minimum Estimated Diameter in Kilometeres.
*est_diameter_max* | Float | Maximum Estimated Diameter in Kilometeres.
*relative_velocity* | Float | Velocity Relative to Earth
*orbiting_body* | string | Earth
*sentry_object* | False | Included in sentry - an automated collision monitoring system
*absolute_magnitude* | Float | Describes intrinsic luminosity
*Hazardous* | Boolean |  Feature that shows whether asteroid is harmful or not


## Project Plan / Process
#### :one:   Data Acquisition

<details>
<summary> Gather data from kaggle database</summary>

- Import csv in local files

- Read/ Creat data dictionary and extract meaningful columns 

</details>

<details>
<summary> acquire.py</summary>

- Create acquire.py and user-defined function to import data from csv

</details>

#### :two:   Data Preparation

<details>
<summary> Data Cleaning</summary>

- **Missing values:**
    - No missing values in kaggle dataset


- **Outliers**
    - Outliers were kept

- **Droppeds**
     - `id`,`name`,`orbiting_body, `sentry` columns were dropped,no useful information.
      
   
<details>
<summary> Data Splitting</summary>

- Create function to split data into **train, validate, test**

- Call the function, and store the 3 data samples separately in the form of dataframe
  
</details>

#### :three:   Exploratory Analysis
- Ask questions to find what are the key features that are associated with hazard status

- Explore each feature's correlation with status

- Using visualizations to better understand the relationship between features

#### :four:    Statistical Testing & Modeling
- 


- Conclude hypothesis and address the initial questions
#### :five:    Modeling Evaluation

- Find the amount of features that can gerenate the highest performance (Recall)

- 

- Pick the model with highest accuracy and evaluate on test dataset




# :medal_sports:  Key Findings
* About 10 % of data was classified as `hazardous`
* All 3 features above shows promise in determing hazard status
* The best performing model was the `XGboost` and was able to detect 98% of hazardous asteroids




# Recommendation
This model has a high percentage of finding the hazardous asteroids at the cost of a low accuracy, due to the false postitives

* This model should be used UNTIL a better model is developed

:electron: # Next Steps
* Use the API to gather more relevant features, try to increase hazardous object capture rate.

* Combine with image recogonition, try to automate process to have 24/7 observation / protection



# Steps To Clone:
1. Clone this repo
2. Import NASA's csv
3. Run Notebook
     # some dependencies may need to be installed such as 'xgboost'
