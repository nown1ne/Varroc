# Battery Capacity Prediction for Low-Resource Environments
https://github-production-user-asset-6210df.s3.amazonaws.com/25835195/320318759-9448119c-44dc-4288-ba85-ec3326c88da9.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240409%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240409T135104Z&X-Amz-Expires=300&X-Amz-Signature=bdccd6b73634c76b58af17d6b7ed7615361088485d290ad9507da0f85b01bd27&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=783439280
## Table of Contents
- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Current Solutions and Limitations](#current-solutions-and-limitations)
- [Our Approach](#our-approach)
- [Critical Points and Model Selection](#critical-points-and-model-selection)
- [File Structure](#file-structure)
- [Contributing Guidelines](#contributing-guidelines)

## Introduction
This project aims to develop a battery capacity prediction model suitable for low-resource environments, such as TI C2000 microcontrollers. The model predicts battery capacity based on discharge cycle data, enabling efficient resource utilization and real-time implementation.

## Problem Statement
Traditional battery capacity prediction models, such as LSTMs, GRUs, and time series models, require significant computational resources, making them unsuitable for low-power microcontrollers like TI C2000. These models often involve complex architectures and large memory footprints, hindering real-time deployment and efficient resource utilization.

## Current Solutions and Limitations
Existing approaches for battery capacity prediction, such as LSTMs and GRUs, rely on recurrent neural networks (RNNs) and time series analysis. While effective, these models demand high computational resources and memory, making them impractical for deployment on low-power microcontrollers like TI C2000.

## Our Approach
We propose a lightweight battery capacity prediction model suitable for low-resource environments. Our model utilizes simple regression algorithms trained on discharge cycle data to predict battery capacity. By prioritizing efficiency and simplicity, our approach enables real-time deployment on low-power microcontrollers while maintaining accuracy.

## Critical Points and Model Selection
To ensure efficient resource utilization and accurate battery capacity prediction, we identified four critical points in the discharge cycle data:
1. **Time of Maximum Temperature:** The time at which the battery reaches its maximum temperature during the discharge cycle. This critical point reflects the thermal stress experienced by the battery, which is indicative of its health and capacity degradation.
2. **Maximum Temperature:** The highest temperature recorded during the discharge cycle. High temperatures accelerate battery degradation, making it an essential factor in capacity prediction.
3. **Time after 1500s when Voltage Drops Below 1V:** This critical point signifies the time duration after 1500 seconds when the battery voltage drops below 1 volt. It represents the end-of-life behavior of the battery, indicating imminent capacity depletion.
4. **Time of Minimum Voltage:** The time at which the battery voltage reaches its minimum value during the discharge cycle. Low voltage levels suggest reduced battery capacity and imminent failure.

We chose these critical points based on their significance in battery health monitoring and capacity estimation. By incorporating these points into our model, we capture key indicators of battery degradation and predict capacity accurately. Furthermore, the selection of these critical points aligns with the low-resource requirement of our model, enabling efficient implementation on microcontrollers like TI C2000.


## File Structure
- `B0005.mat`: Data file containing discharge cycle data for battery B0005.
- `B0006.mat`: Data file containing discharge cycle data for battery B0006.
- `B0007.mat`: Data file containing discharge cycle data for battery B0007.
- `B0018.mat`: Data file containing discharge cycle data for battery B0018.
- `battery_capacity_prediction.ipynb`: Jupyter notebook containing Python code for battery capacity prediction.
- `README.md`: Documentation providing an overview of the project, problem statement, solution, and code explanation.

## Contributing Guidelines
We welcome contributions to this project. If you would like to contribute, please follow these guidelines:
1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and ensure all tests pass.
4. Commit your changes with clear commit messages.
5. Push your changes to your fork.
6. Submit a pull request to the main repository's `main` branch.

Thank you for your interest in contributing to our project!

