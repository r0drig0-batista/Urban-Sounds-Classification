# Urban Sound Classification Project (UrbanSound8K)  

## Project Description  
This project aims to develop **deep learning** classifiers for the **UrbanSound8K** dataset, which contains 8,732 urban sound excerpts classified into 10 categories:  
- Air Conditioner  
- Car Horn  
- Children Playing  
- Dog Bark  
- Drilling  
- Engine Idling  
- Gunshot  
- Jackhammer  
- Siren  
- Street Music  

The project was developed as part of the **Machine Learning II** course at **FCUP**.  

---  

## Implemented Models  
Two classifiers were implemented:  
1. **Multilayer Perceptron (MLP)**  
2. **Convolutional Neural Network (CNN) 2D**  

---  

## Project Steps  

### 1. Data Preprocessing and Preparation  
- **Libraries Used:** `librosa` for audio feature extraction.  
- **Steps:**  
  - Normalization and standardization of audio signals.  
  - Extraction of **Mel-frequency cepstral coefficients (MFCCs)** for 2D sound representation.  
  - Splitting data into training, validation, and test sets using **10-fold cross-validation**.  

### 2. Model Architecture Definition  
#### MLP  
- **Layers:**  
  - Input layer with dimensions corresponding to the number of extracted features.  
  - Hidden layers with **ReLU** activation.  
  - Output layer with **Softmax** activation for multi-class classification.  
- **Hyperparameters:**  
  - Number of neurons per layer.  
  - Dropout rate for regularization.  

#### CNN 2D  
- **Layers:**  
  - Convolutional layers with 2D filters.  
  - Pooling layers (MaxPooling2D).  
  - Fully connected (Dense) layers at the end.  
  - **ReLU** activation in hidden layers and **Softmax** in the output layer.  
- **Hyperparameters:**  
  - Number of filters and kernel sizes.  
  - Pooling size.  

### 3. Training Strategies  
- **Optimizer:** Adam.  
- **Hyperparameters:**  
  - Learning rate.  
  - Mini-batch size.  
  - Number of epochs.  
- **Regularization Techniques:**  
  - Dropout.  
  - Early stopping to prevent overfitting.  

## Conclusions  
- The **MLP** showed satisfactory performance, but the **CNN 2D** outperformed it in terms of accuracy, demonstrating the effectiveness of convolutional networks for audio classification tasks.  
- Feature extraction using MFCCs was crucial for the success of the CNN 2D.

## Authors
  - Francisco Tavares
  - Rodrigo Batista
  - Rodrigo Taveira
