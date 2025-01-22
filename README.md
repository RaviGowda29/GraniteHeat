# Heat Equation Fine-Tuning for Large Language Models

This repository contains the code and data pipelines for fine-tuning a Large Language Model (LLM) to solve problems related to the heat equation. Inspired by the Fine-Tuning LM for Physical Interpretation Hackathon on Kaggle, our goal is to enable the pre-trained Granite 3.1 model to predict temperatures based on the heat equation and boundary conditions.

The heat equation, a key partial differential equation (PDE), describes how heat diffuses through a region over time. Our model is trained on simulated data to predict temperatures at various points in space and time.

## Dataset Description

Overview

The dataset used for fine-tuning the Granite 3.1 model is based on heat equation simulations. The data is generated from VTK files (Visualization Toolkit) that model heat diffusion over time and space. The dataset contains temperature values at various spatial coordinates and time steps, simulating heat transfer in different materials.

Our model will be fine-tuned to interpret these data points and generate meaningful answers to questions related to the heat equation, such as predicting temperature at different points in space and time based on boundary conditions.

The dataset is processed and stored in CSV format, where each row corresponds to a specific simulation state, containing spatial coordinates, time, initial temperature, and the output temperature at a given time step.

Dataset Description

The dataset used for fine-tuning the Granite 3.1 model consists of heat diffusion simulations generated from VTK files. It includes temperature values at various spatial coordinates and time steps, simulating heat transfer in different materials.

The data is processed into CSV format, where each row represents a simulation state, containing:

 Spatial coordinates
 Time
 Initial temperature
 Output temperature at a given time step

This dataset enables the model to predict temperature distribution based on the heat equation and boundary conditions.

For more information on the dataset and the competition, please refer to the official Fine-Tuning LM for Physical Interpretation Hackathon page on Kaggle.

## Features

Fine-tune IBM's Granite 3.1 model using Hugging Face Transformers.
Generate synthetic data for training using PyVista and NumPy.
Perform evaluation with test datasets reflecting unseen scenarios.

heat-equation-llm-finetuning/
├── data/                # Contains VTK files and the processed dataset (CSV files)
│   ├── raw_vtk/         # Raw VTK files with temperature and simulation data
│   └── processed_csv/   # Processed CSV files ready for model training
│
├── scripted_data/       # Scripts for data processing (VTK to CSV conversion, etc.)
│   ├── convert_vtk_to_csv.py  # Script to convert raw VTK data to CSV format
│   └── preprocess_data.py     # Additional preprocessing steps, if any
│
├── scripts/             # Python scripts for model training and evaluation
│   ├── fine_tune.py     # Main script to fine-tune the model (Granite 3.1)
│   ├── evaluate_model.py  # Script to evaluate the fine-tuned model
│   └── visualize_results.py  # For plotting and visualizing model predictions
│
├── models/              # Model checkpoints and outputs
│   ├── granite3.1/      # Pre-trained Granite 3.1 model
│   ├── fine_tuned/      # Fine-tuned versions of Granite 3.1 for heat equation tasks
│   └── model_outputs/   # Directory to save model outputs (e.g., weights, predictions)
│
├── results/             # Evaluation metrics, performance logs, and visualizations
│   ├── metrics/         # Stores model evaluation metrics (e.g., MSE, RMSE, etc.)
│   └── plots/           # Visualizations (e.g., predictions vs. ground truth)
│
└── README.md            # Project overview, setup instructions, and usage guide


or additional resources and reference materials, the following links are useful:

- **Kaggle Competition: Fine-Tuning LM for Physical Interpretation Hackathon**  
  [Kaggle Competition Link](https://www.kaggle.com/competitions/fine-tuning-lm-physical-interpretation-hackathon)  
  This competition inspired the project, and the dataset and problem details can be found there.

- **IBM Granite 3.1 Model Documentation**  
  [Granite 3.1 Model Documentation](https://granite.ibm.com)  
  For detailed information on the pre-trained **Granite 3.1** model and how it works.

- **Build a Large Language Model (From Scratch) by Sebastian Raschka**  
  [Build LLM from Scratch](https://sebastianraschka.com/blog/2021/building-llm/)  
  This blog provides a detailed, step-by-step guide on building a large language model from scratch, which can be helpful for understanding the underlying mechanics of language models like Granite 3.1.


