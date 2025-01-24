# Heat Equation Fine-Tuning for Large Language Models


## OverView

This repository contains the code and data pipelines for fine-tuning a Large Language Model (LLM) to solve problems related to the heat equation. Inspired by the Fine-Tuning LM for Physical Interpretation Hackathon on Kaggle, the goal is to fine-tune the pre-trained Granite 3.1 model to predict temperatures based on the heat equation and boundary conditions.

The heat equation is a key partial differential equation (PDE) that describes how heat diffuses through a region over time. We train the model using simulated data to predict temperatures at various points in space and time.

## Dataset Description:

- Dataset Source: The dataset used for fine-tuning the Granite 3.1 model is based on heat diffusion simulations generated from VTK files (Visualization Toolkit).

- Data Representation: The data represents temperature values at various spatial coordinates and time steps, simulating heat transfer in different materials.

- Data Format: The data is processed and stored in CSV format for easier use in model fine-tuning.

- Training Goal: The model is trained to predict the temperature distribution based on the heat equation and boundary conditions.

- Additional Information: For more details on the dataset and the competition, visit the official Kaggle competition page.[Here](https://www.kaggle.com/competitions/fine-tuning-lm-physical-interpretation-hackathon/data)

## Features:

- Fine-tune IBM's Granite 3.1 model using Hugging Face Transformers.
  
- Generate synthetic data for training using PyVista and NumPy.
  
- Evaluate model performance with test datasets representing unseen scenarios.
  
- Experiment with instruction fine-tuning to improve model adaptability to specific tasks and enhance its performance in real-world applications.

## Project Structure
```
heat-equation-llm-finetuning/
├── dataset/              
│   ├── raw_vtk/              # Raw VTK files with temperature and simulation data
│   ├── convert_vtk_to_csv.py # Script to convert raw VTK data to CSV format
│   └── preprocess_data.py    # Additional preprocessing steps, if any
│
├── scripts/                
│   ├── fine_tune.py          # Main script to fine-tune the model (Granite 3.1)
│   ├── evaluate_model.py     # Script to evaluate the fine-tuned model
│   └── visualize_results.py  # Script for plotting and visualizing model predictions
│
├── models/                 
│   ├── granite3.1/           # Pre-trained Granite 3.1 model
│   ├── fine_tuned/           # Fine-tuned models for heat equation tasks
│   └── model_outputs/        # Directory to save model outputs (e.g., weights, predictions)
│
├── results/                 
│   ├── metrics/              # Model evaluation metrics (e.g., MSE, RMSE)
│   └── plots/                # Visualizations (e.g., predictions vs. ground truth)
│
└── README.md                 # Project overview, setup instructions, and usage guide

```
## References

- [Kaggle Competition: Fine-Tuning LM for Physical Interpretation Hackathon](https://www.kaggle.com/competitions/fine-tuning-lm-physical-interpretation-hackathon/overview)

- [IBM Granite 3.1 Model Documentation](https://www.ibm.com/granite/docs/models/granite/)

- [Build a Large Language Model (From Scratch)](https://www.google.co.in/books/edition/Build_a_Large_Language_Model_From_Scratc/scIgEQAAQBAJ?hl=en&gbpv=1&pg=PA1&printsec=frontcover)

- [LLM-Engineers-Handbook](https://github.com/PacktPublishing/LLM-Engineers-Handbook)

