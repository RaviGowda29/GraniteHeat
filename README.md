Heat Equation Fine-Tuning for Large Language Models

This repository contains the code and data pipelines for fine-tuning a Large Language Model (LLM) to solve problems related to the heat equation. Inspired by the Fine-Tuning LM for Physical Interpretation Hackathon on Kaggle, the goal is to fine-tune the pre-trained Granite 3.1 model to predict temperatures based on the heat equation and boundary conditions.

The heat equation is a key partial differential equation (PDE) that describes how heat diffuses through a region over time. We train the model using simulated data to predict temperatures at various points in space and time.
Dataset Description
Overview

The dataset used for fine-tuning the Granite 3.1 model is based on heat diffusion simulations generated from VTK files (Visualization Toolkit). The data represents temperature values at various spatial coordinates and time steps, simulating heat transfer in different materials.

Each data point consists of:

    Spatial coordinates
    Time
    Initial temperature
    Output temperature at a given time step

This data is processed and stored in CSV format for easier use in model fine-tuning. The model is trained to predict the temperature distribution based on the heat equation and boundary conditions.

For more information on the dataset and the competition, please visit the official Kaggle competition page.
Features

    Fine-tune IBM's Granite 3.1 model using Hugging Face Transformers.
    Generate synthetic data for training using PyVista and NumPy.
    Evaluate model performance with test datasets representing unseen scenarios.

Project Structure

The repository is organized as follows:

heat-equation-llm-finetuning/
├── data/                
│   ├── raw_vtk/         # Raw VTK files with temperature and simulation data
│   └── processed_csv/   # Processed CSV files ready for model training
│
├── scripted_data/       
│   ├── convert_vtk_to_csv.py  # Script to convert raw VTK data to CSV format
│   └── preprocess_data.py     # Additional preprocessing steps, if any
│
├── scripts/             
│   ├── fine_tune.py     # Main script to fine-tune the model (Granite 3.1)
│   ├── evaluate_model.py  # Script to evaluate the fine-tuned model
│   └── visualize_results.py  # For plotting and visualizing model predictions
│
├── models/              
│   ├── granite3.1/      # Pre-trained Granite 3.1 model
│   ├── fine_tuned/      # Fine-tuned versions of Granite 3.1 for heat equation tasks
│   └── model_outputs/   # Directory to save model outputs (e.g., weights, predictions)
│
├── results/             
│   ├── metrics/         # Stores model evaluation metrics (e.g., MSE, RMSE)
│   └── plots/           # Visualizations (e.g., predictions vs. ground truth)
│
└── README.md            # Project overview, setup instructions, and usage guide
