# Disease Outbreak Prediction

## Abstract

This project implements deep learning algorithms and LLMs to predict the severity of infectious disease outbreaks in India. By utilizing historical disease data and climatic data from the past decade, we aim to create a robust predictive system for future outbreaks.

## Introduction

Following the COVID-19 pandemic, the need for accurate and reliable predictive systems for disease outbreaks has become paramount. This research leverages historical data on disease spread and climatic conditions in India to develop a predictive model for future outbreaks.

## Methodology

### Dataset Creation

1. **Disease Dataset**: Collected from official sources, covering nine diseases including COVID-19, Influenza, Typhoid, etc.
2. **Weather Dataset**: Curated using the Weather.com API, spanning from January 1, 2009, to February 23, 2024.
3. **Demographics Dataset**: Merged with the symptoms dataset, including attributes like disease descriptions, test procedures, and risk factors.

### Text Embeddings

We used the pre-trained 'distilbert-base-uncased' model to generate embeddings for text data (Disease, Symptoms, and Most Repeated Weather Phrase).

### Deep Learning Model

Our final approach involves a hybrid model integrating both numerical features and text embeddings:

1. Concatenation of numerical features and text embeddings
2. Deep learning architecture with 5 dense layers using ReLU activation
3. L2 regularization to prevent overfitting
4. Adam optimizer for model training

## Results

The model was tested on an Influenza dataset, achieving the following metrics:

| Metric | Value |
|--------|-------|
| Mean Absolute Error | 1846.39 |
| Mean Squared Error | 13367089.49 |
| Root Mean Squared Error | 3656.10 |
| R-Squared | 0.95 |

## Conclusion

This research demonstrates the potential of predictive modeling in public health, focusing on infectious disease outbreaks. The developed model can assist public health officials and policymakers in proactively preparing for potential disease outbreaks, allocating resources, and implementing preventive measures.

## How to Use the Project
1. Clone the repository:
   ```
   git clone https://github.com/your-username/disease-outbreak-prediction.git
   ```

2. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Prepare your data:
   - Ensure your disease, weather, and demographic data are in the correct format
   - Place the datasets in the `datasets` folder

4. Run the main script:
   ```
   python main.py
   ```

5. View the results and predictions in the output folder
