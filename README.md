This repository contains the code and data pipelines for fine-tuning a Large Language Model (LLM) to interpret and solve problems related to the heat equation in various scenarios. Inspired by the Fine-Tuning LM for Physical Interpretation Hackathon on Kaggle, the goal of this project is to enable a pre-trained LLM (Granite 3.1) to accurately predict temperatures in a given environment, based on the heat equation and associated boundary conditions.

The heat equation is a fundamental partial differential equation (PDE) that describes how heat diffuses through a given region over time. Our model is trained on data that simulates heat diffusion scenarios and learns to predict the temperature at different points in space and time.


Objective

The objective of this project is to:

   Fine-tune a pre-trained LLM on the heat equation dataset to enable it to predict temperature distribution in a given space over time.
    Use VTK-based data (which includes temperature, position, and time data) and convert it to a CSV format for easier use in model fine-tuning.
    Generate prompt-response pairs that translate physical properties (such as initial temperature and position) into readable, accurate model outputs (predicted temperatures).

Dataset Description

Overview

The dataset used for fine-tuning the Granite 3.1 model is based on heat equation simulations. The data is generated from VTK files (Visualization Toolkit) that model heat diffusion over time and space. The dataset contains temperature values at various spatial coordinates and time steps, simulating heat transfer in different materials. The model will be fine-tuned to interpret these data points and generate meaningful answers to questions related to the heat equation, such as predicting temperature at different points in space and time based on boundary conditions.

The dataset is processed and stored in CSV format, where each row corresponds to a specific simulation state, containing spatial coordinates, time, initial temperature, and the output temperature at a given time step.
