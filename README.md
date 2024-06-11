
## Welcome to the 2nd IEEE ITSS Student Competition on Pedestrian Behavior Prediction!

## Video Demo
[Placeholder for a video]

## Background
Pedestrian behavior prediction is one of the most critical challenges for fully automated driving in urban settings. It requires autonomous vehicles to interact safely and efficiently with pedestrians in diverse and dynamic environments. Accurate and robust pedestrian behavior prediction is crucial to ensure the safety of both pedestrians and autonomous vehicles.

## Competition Tasks
- **Short-Term Pedestrian Trajectory Prediction (ST-PTP)**
- **Long-Term Pedestrian Trajectory Prediction (LT-PTP)**

PTP forecasts a pedestrian's future trajectory from a bird's-eye view, using observed data from six surrounding cameras and lidar. The Short-Term Prediction (ST) targets a 3-second future path, while the Long-Term Prediction (LT) extends to 7 seconds.

## Eligibility
We invite competitors from all around the world. Each team's leader must be a current undergraduate or graduate student. Teams are limited to entering one track only.

## Prizes
![Placeholder for a prize image](file-Sy85iu64zALlDTEwthTUWH9p)

## Important Dates
- **Competition Begins:** June 15th
- **Dry Run: ** August 10th
- **Submission Deadline:** August 15th
## Get Started

### Sample Data
[Instructions or link to sample data]

### Train and Validation Data
[Instructions or link to train and validation data]
## Evaluation Guidelines
## Evaluation Guidelines for IEEE ITSS Student Competition on Pedestrian Behavior Prediction

To ensure the accuracy and robustness of the pedestrian behavior prediction models, the following evaluation metrics will be used:

### Metrics for Evaluation

1. **Average Displacement Error (ADE)**
   - **Definition:** ADE measures the average Euclidean distance between the predicted trajectory and the ground truth trajectory over all annotated key points.
   - **Formula:** 
     ```markdown
     ADE = \frac{1}{K} \sum_{k=1}^{K} \sqrt{(x_k - \hat{x}_k)^2 + (y_k - \hat{y}_k)^2}
     ```
     where `K` is the total number of annotated key points, `(x_k, y_k)` is the ground truth position at key point `k`, and `(\hat{x}_k, \hat{y}_k)` is the predicted position at key point `k`.

2. **Final Displacement Error (FDE)**
   - **Definition:** FDE measures the Euclidean distance between the predicted final position and the ground truth final position at the last annotated key point.
   - **Formula:**
     ```markdown
     FDE = \sqrt{(x_K - \hat{x}_K)^2 + (y_K - \hat{y}_K)^2}
     ```
     where `K` is the final annotated key point, `(x_K, y_K)` is the ground truth final position, and `(\hat{x}_K, \hat{y}_K)` is the predicted final position.

3. **Miss Rate (MR)**
   - **Definition:** MR is the proportion of predicted trajectories that are further away from the ground truth trajectory by a certain threshold at the final annotated key point.
   - **Formula:**
     ```markdown
     MR = \frac{1}{N} \sum_{i=1}^{N} \mathbf{1}(\sqrt{(x_K^i - \hat{x}_K^i)^2 + (y_K^i - \hat{y}_K^i)^2} > \delta)
     ```
     where `N` is the total number of predicted trajectories, `\mathbf{1}` is the indicator function, and `\delta` is the distance threshold.

4. **Collision Rate (CR)**
   - **Definition:** CR measures the percentage of predicted trajectories that collide with static or dynamic obstacles in the environment, calculated based on all points of the trajectories.
   - **Formula:**
     ```markdown
     CR = \frac{1}{N} \sum_{i=1}^{N} \mathbf{1}(\text{collision}(i))
     ```
     where `\text{collision}(i)` indicates whether the `i`-th predicted trajectory collides with any obstacle.

### Evaluation Procedure

1. **Data Splitting**
   - The dataset will be divided into training, validation, and test sets. The training and validation sets will be provided to participants for model development and tuning, while the test set will be used for final evaluation.

2. **Prediction Horizon**
   - Short-Term Prediction (ST-PTP): Predicting the pedestrian trajectory for the next 3 seconds.
   - Long-Term Prediction (LT-PTP): Predicting the pedestrian trajectory for the next 7 seconds.

3. **Frame Rate Adjustment**
   - The annotated data are provided at 1 FPS, but the output trajectory needs to be at 5 FPS. Participants must ensure their predicted trajectories are interpolated to meet this requirement.

4. **Submission Format**
   - Participants must submit their predicted trajectories in a predefined format. Each submission should include the predicted coordinates for each pedestrian at each time step within the prediction horizon.

5. **Scoring**
   - Submissions will be evaluated based on the ADE and FDE metrics, calculated only on the annotated key points. Additional metrics such as MR and CR will be considered for assessing the safety and feasibility of the predicted trajectories. The CR will be calculated based on all the points of the trajectories.
   - The final ranking will be based on the average ranking of all metrics.

6. **Ranking**
   - Teams will be ranked based on their final scores. In the event of a tie, the team with the lower FDE will be ranked higher.



## Steering Committee
- **Professor 1**
  - ![Professor 1 Image](file-3oKWflsxpzSyO7G5D7W3GqDQ)
  - Affiliation
- **Professor 2**
  - ![Professor 2 Image](file-nDJKa77WK0Nq1GiMhwojjXtR)
  - Affiliation
- **Professor 3**
  - ![Professor 3 Image](file-KgQxuJ30J0DSRcgAXKZf88R5)
  - Affiliation

## Organizers
- **Organizer 1**
  - ![Organizer 1 Image](file-Sy85iu64zALlDTEwthTUWH9p)
  - Affiliation
- **Organizer 2**
  - ![Organizer 2 Image](file-3oKWflsxpzSyO7G5D7W3GqDQ)
  - Affiliation
- **Organizer 3**
  - ![Organizer 3 Image](file-nDJKa77WK0Nq1GiMhwojjXtR)
  - Affiliation
- **Organizer 4**
  - ![Organizer 4 Image](file-KgQxuJ30J0DSRcgAXKZf88R5)
  - Affiliation
- **Organizer 5**
  - ![Organizer 5 Image](file-Sy85iu64zALlDTEwthTUWH9p)
  - Affiliation
- **Organizer 6**
  - ![Organizer 6 Image](file-3oKWflsxpzSyO7G5D7W3GqDQ)
  - Affiliation

![Flyer](images/Flyer_3.png)

:bulb: This competition focuses on Short-Term Pedestrian Trajectory Prediction (ST-PTP) and Long-Term Pedestrian Trajectory Prediction (LT-PTP). PTP forecasts a pedestrian's future trajectory from a bird's-eye view, utilizing observed data from six surrounding cameras and lidar. The Short-Term Prediction (ST) targets a 3-second future path, while the Long-Term Prediction (LT) extends to 7 seconds.

<h1 align="center">Stay tuned for more information coming soon!</h1>


<p align="right">(<a href="#top">back to top</a>)</p>
