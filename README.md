# Tremor-Activity-Analysts

**Tremor-Activity-Analysts** is a repository developed as part of the ABC Challenge, "Understanding Normal vs. Unusual Activities Related to Parkinson's Disease with Multimodal Data." The objective of this project is to recognize 10 different activities, including normal and unusual activities such as tremors, based on multimodal sensor data, with a particular focus on Parkinson's disease-related motor symptoms.



---

## Overview

Parkinson's disease (PD) is characterized by symptoms such as tremors, muscle stiffness, and difficulty in walking. Recognizing these symptoms through sensor data plays a vital role in early diagnosis, treatment personalization, and ongoing patient care. This repository leverages data from wearables and mobile devices to detect both normal and PD-related unusual activities, including various types of tremors and gait abnormalities.

This project aims to:
- Link multimodal sensor data with corresponding activities and subjects
- Develop machine learning models to classify 10 distinct activity classes
- Understand and analyze tremor patterns as a key indicator of PD progression
- Comply with data usage policies and challenge guidelines

---

## Dataset Structure

### Sensor Data
- **Main Directory**: `users_timeXYZ/users/`
- **Subdirectories**: Multiple subdirectories named with random numerical values (e.g., `38`, `1716`)
- **Data Files**: Each subdirectory contains one or more CSV files with accelerometer data.
  - **File Naming Pattern**: `user-acc_[DIR-NUMBER]_[TIMESTAMP]_[RANDOM-NUMBER].csv`
  - **File Example**:
    ```
    user-acc_38_2024-09-08T23_31_01.510+0100_97016.csv
    user-acc_38_2024-09-08T23_31_16.519+0100_15638.csv
    ```

### Sensor Data File Format
Each CSV file contains 5 columns:
1. Random identifier (to be ignored)
2. Timestamp
3. x-axis accelerometer data
4. y-axis accelerometer data
5. z-axis accelerometer data

### Activity Labels
- **File**: `TrainActivities.csv`
- **Columns**:
  - ID (random identifier)
  - Activity Type ID
  - Activity Type (e.g., 1: (FACING camera) Sit and stand)
  - Start Time
  - End Time
  - Update Time
  - Subject ID (e.g., U1, U2, ..., U22)


**Activities:**
1. (FACING camera) Sit and stand
2. (FACING camera) both hands SHAKING (sitting position)
3. Stand up from chair - both hands with SHAKING
4. (Sideway) Sit & stand
5. (Sideway) both hands SHAKING (sitting)
6. (Sideway) STAND up with - both hands SHAKING
7. Cool down - sitting/relax
8. Walk (LEFT --> Right --> Left)
9. Walk & STOP/frozen, full body shaking, rotate then return back
10. Slow walk (SHAKING hands/body, tiny step, head forward)

---

## Challenge Description

**Objective:** Develop a robust model to classify 10 distinct activities from accelerometer and other multimodal sensor data, particularly focusing on recognizing tremor-related unusual activities due to Parkinson's disease.

**Training Data:**
- Data from 9 subjects: U1, U2, U3, U4, U5, U6, U7, U21, and U22.
- Each subject performs all 10 activities, with possible data gaps.

**Key Tasks:**
- Link sensor data files with their corresponding activity labels and subjects
- Explore various train/test splitting strategies
- Document methodology, experiments, results, and insights for paper submission

---

## Activity Classes in Parkinson's Data

The dataset captures a range of activity classes, both normal and unusual. Some relevant classes include:
- **Relax Time**: Periods of rest or minimal physical activity.
- **Normal Sit and Stand**: Routine sit-to-stand movements without abnormalities.
- **Tremor While Seated**: Involuntary shaking of body parts while sitting.
- **Tremor While Standing**: Involuntary shaking while standing.
- **Normal Walking**: Baseline walking pattern without irregularities.
- **Freezing and Festinating Gait**: Episodes of freezing and rapid, short steps.
- **Shuffling Gait**: Walking with dragging feet or short steps.

By analyzing these activities using multimodal sensor data (smartwatch, mobile accelerometer, pose estimation, etc.), the project aims to identify patterns indicative of Parkinson’s disease progression.

---



