```markdown
# Medicine Recommendation System

## Overview

This is a **Medicine Recommendation System** built using Python, Flask, and a machine learning model. The system suggests alternative medicines based on the selected medicine by the user. It uses a similarity-based recommendation approach to find medicines with similar properties or functions.

## Project Structure

- **`app.py`**: This file contains the Flask web application that serves the recommendation system. Users can input a medicine, and the app will recommend similar medicines.
- **`Medicine recommendation System.ipynb`**: A Jupyter Notebook that contains the data processing and model development pipeline for generating the medicine similarity matrix.
- **`medicine.csv`**: The dataset containing information about various medicines, which is used to train the recommendation model.
- **Pickle Files**:
  - `medicine_dict.pkl`: Contains the processed medicine data.
  - `similarity.pkl`: Stores the similarity matrix used to recommend medicines.

## Features

1. **Medicine Recommendation**:
   - Users can input the name of a medicine, and the system will recommend 5 similar medicines.
   
2. **Similarity Model**:
   - A pre-trained machine learning model calculates the similarity between medicines based on their features.

## Setup and Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd medicine-recommendation-system
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the dataset and pre-trained models:
   - Ensure `medicine.csv`, `medicine_dict.pkl`, and `similarity.pkl` are placed in the root directory.

4. Run the Flask application:
   ```bash
   python app.py
   ```

## How It Works

1. The **Jupyter Notebook** processes the dataset, computes medicine similarities, and saves the similarity matrix.
2. The **Flask App** serves an HTML page where users can select a medicine.
3. Once a medicine is selected, the app uses the pre-trained similarity matrix to recommend the top 5 most similar medicines.

## Dataset

The dataset (`medicine.csv`) contains the following columns:
- `Drug_Name`: The name of the medicine.
- Other features relevant to the medicine (e.g., type, use-case, ingredients).
