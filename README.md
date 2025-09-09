# Marine Riser VIV Prediction using a Neural Network

This project uses a feedforward neural network built with **PyTorch** to predict the Vortex-Induced Vibration (VIV) characteristics, specifically the RMS Amplitude, of a marine riser based on its physical and environmental parameters.

-----

## 📝 Overview

Vortex-Induced Vibration is a critical phenomenon in offshore engineering, and accurately predicting its amplitude is essential for ensuring the structural integrity of marine risers. This notebook demonstrates a data-driven approach to solving this problem by:

  * Loading and preprocessing riser data from an Excel file.
  * Defining and training a simple but effective neural network.
  * Evaluating the model's performance using standard regression metrics.
  * Visualizing the results to provide clear insights.
  * Offering an interactive function to make predictions on new, user-defined data.

-----

## ✨ Key Features

  * **Data-Driven Prediction**: Leverages a dataset of riser parameters to learn complex, non-linear relationships.
  * **PyTorch Implementation**: A clean and modern implementation using one of the leading deep learning frameworks.
  * **Comprehensive Evaluation**: The model's accuracy is assessed using both **R-squared (R²)** and **Root Mean Squared Error (RMSE)**.
  * **Rich Visualizations**: Includes plots for epoch vs. loss, predicted vs. actual values, and feature-specific performance graphs.
  * **Interactive Prediction**: Allows users to input their own riser parameters and receive an immediate prediction for the RMS amplitude.

-----

## 🛠️ Technology Stack

  * **Core Language**: Python 3
  * **Deep Learning**: PyTorch
  * **Data Handling**: Pandas, NumPy
  * **Evaluation & Preprocessing**: Scikit-learn
  * **Visualization**: Matplotlib
  * **Environment**: Google Colab (recommended for GPU support)

-----

## 🧠 Model Architecture

The neural network is a simple feedforward model with the following structure:

  * **Input Layer**: 4 neurons (corresponding to `Cylinder Length`, `f_s`, `f_n`, and `ζ`)
  * **Hidden Layer 1**: 64 neurons with a ReLU activation function.
  * **Hidden Layer 2**: 32 neurons with a ReLU activation function.
  * **Output Layer**: 1 neuron (predicting the `RMS Amplitude`)

The model is trained using the **Adam optimizer** and the **Mean Squared Error (MSE)** loss function.

-----

## 🚀 Getting Started

To run this project, open the `.ipynb` notebook in Google Colab.

### **Prerequisites**

  * A Google account to use Google Colab and Google Drive.
  * The project dataset (`software_dataset.xlsx`) must be uploaded to your Google Drive.

### **Installation & Setup**

1.  **Open in Colab**: Launch the `.ipynb` file in your Google Colab environment.
2.  **Mount Google Drive**: Run the second code cell in the notebook. You will be prompted to authorize access to your Google Drive.
3.  **Update File Path**: Locate the cell where the `file_path` is defined and ensure it points to the correct location of your `software_dataset.xlsx` in your Google Drive.
    ```python
    file_path = '/content/gdrive/My Drive/path/to/your/software_dataset.xlsx'
    ```
4.  **Run the Notebook**: You can now execute all cells sequentially (`Runtime > Run all`) to load the data, train the model, and see the results.
