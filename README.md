Marine Riser VIV Prediction Neural Network
This project demonstrates the use of a simple feedforward neural network, built with PyTorch, to predict Vortex-Induced Vibration (VIV) characteristics of a marine riser.

📝 Overview
The notebook trains a neural network on a dataset of marine riser parameters to predict the RMS amplitude of vibration. It includes the following key steps:

Definition of a simple feedforward neural network using torch.nn.

A training loop to optimize the model using the Adam optimizer and Mean Squared Error loss.

Evaluation of the model using R-squared and Root Mean Squared Error (RMSE) metrics.

Visualization of the training process and prediction accuracy.

A function to make predictions based on new user input.

🛠️ Technology Stack
Python: The core programming language.

PyTorch: For building and training the neural network.

Pandas: For data manipulation and loading from the Excel file.

Scikit-learn: For model evaluation metrics (R-squared, RMSE) and data splitting.

Matplotlib: For plotting and visualizing the results.

Google Colab: The notebook is designed to run in a Colab environment, leveraging its GPU capabilities and integration with Google Drive.

🚀 Getting Started
To run this project, you can open the Riser_Prediction_Neural_Network.ipynb notebook in Google Colab.

Prerequisites
A Google account to access Google Colab and Google Drive.

The dataset file (software_dataset.xlsx) uploaded to your Google Drive.

Installation & Setup
Open in Colab: Open the .ipynb file in Google Colab.

Mount Google Drive: Run the second code cell to mount your Google Drive. You'll be prompted to authorize access.

Update File Path: In the cell where file_path is defined, make sure the path correctly points to the location of your software_dataset.xlsx file in Google Drive.

Python

file_path = '/content/gdrive/My Drive/path/to/your/software_dataset.xlsx'
Run All Cells: You can now run all the cells in the notebook to train the model, evaluate its performance, and make new predictions.

📈 Results
The model is evaluated based on its ability to predict the RMS amplitude. The performance is quantified by:

R-squared (R²): Indicates the proportion of the variance in the dependent variable that is predictable from the independent variables. A value closer to 1 indicates a better fit.

Root Mean Squared Error (RMSE): Measures the standard deviation of the residuals (prediction errors). A lower value indicates a better fit.

The notebook generates several plots to visualize the model's performance, including an epoch vs. loss graph and a scatter plot of predicted vs. actual values.

🔮 Making Predictions
The final section of the notebook provides an interactive function where you can input new riser parameters (Cylinder Length, f_s, f_n, and ζ) and get an instant prediction for the RMS amplitude.
