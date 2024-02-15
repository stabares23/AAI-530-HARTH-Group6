# HARTH Human Activity Recognition Trondheim (HARTH) Dataset

The HARTH dataset is a professionally-annotated collection designed to facilitate research in human activity recognition (HAR) within free-living environments. It comprises data from 22 subjects equipped with two 3-axial accelerometers attached to their right thigh and lower back. These sensors record movement data at a sampling rate of 50Hz, providing a rich resource for training and evaluating machine learning models.

## Dataset Overview

- **Dataset Characteristics**: Multivariate, Time-Series
- **Subject Area**: Computer Science
- **Associated Tasks**: Classification
- **Feature Type**: Real
- **Instances**: 6,461,328
- **Features**: 8

## Dataset Creation

The HARTH dataset was created with the goal of training machine learning classifiers for human activity recognition in free-living scenarios. It was funded by NTNU Helse and features professional annotations of activities performed by participants.

## Dataset Content

Each participant's data is stored in a separate .csv file, containing the following columns:

1. `timestamp`: Date and time of recorded sample
2. `back_x`: Acceleration of back sensor in x-direction (down) in the unit g
3. `back_y`: Acceleration of back sensor in y-direction (left) in the unit g
4. `back_z`: Acceleration of back sensor in z-direction (forward) in the unit g
5. `thigh_x`: Acceleration of thigh sensor in x-direction (down) in the unit g
6. `thigh_y`: Acceleration of thigh sensor in y-direction (right) in the unit g
7. `thigh_z`: Acceleration of thigh sensor in z-direction (backward) in the unit g
8. `label`: Annotated activity code

The dataset includes activities such as walking, running, shuffling, standing, sitting, lying, and various cycling activities.

## Usage

### Requirements

To utilize the dataset in your project, you need:

- Python installed on your system
- The `ucimlrepo` package installed. You can install it using `pip install ucimlrepo`.

### Importing the Dataset

Import the dataset into your code using the provided package:

```python
from ucimlrepo import fetch_ucirepo

# Fetch dataset
harth = fetch_ucirepo(id=779)

# Access data
X = harth.data.features
y = harth.data.targets

# Additional metadata
print(harth.metadata)


## License
This dataset is licensed under a [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/), allowing for sharing and adaptation provided appropriate credit is given.
