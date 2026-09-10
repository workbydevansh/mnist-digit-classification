# MNIST Digit Classification

A simple deep learning project for classifying handwritten digits from the **MNIST dataset** using a neural network built with **TensorFlow and Keras**.

## Overview

This project demonstrates the complete workflow of a basic image classification problem:

* Loading the MNIST handwritten digit dataset
* Visualizing sample images
* Normalizing pixel values
* Building a neural network using Keras
* Training the model for 10 epochs
* Evaluating predictions using accuracy
* Visualizing training and validation loss
* Visualizing training and validation accuracy
* Making predictions on individual test images

## Dataset

The project uses the built-in **MNIST dataset** provided by Keras.

* Training samples: 60,000
* Testing samples: 10,000
* Image size: 28 × 28 pixels
* Number of classes: 10
* Classes: digits `0` to `9`

## Model Architecture

The neural network consists of:

```text
Input Image (28 × 28)
        ↓
Flatten
        ↓
Dense (128 neurons, ReLU)
        ↓
Dense (32 neurons, ReLU)
        ↓
Dense (10 neurons, Softmax)
```

The model is compiled using:

* **Loss:** Sparse Categorical Crossentropy
* **Optimizer:** Adam
* **Metric:** Accuracy
* **Epochs:** 10
* **Validation Split:** 20%

## Preprocessing

The pixel values are normalized from the range `0–255` to `0–1`:

```python
X_train = X_train / 255
X_test = X_test / 255
```

## Results

The trained model is evaluated on the MNIST test set using classification accuracy. Training and validation curves are also plotted to observe the model's learning behavior.

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab / Jupyter Notebook

## Project Structure

```text
mnist-digit-classification/
│
├── mnist_classification.ipynb
└── README.md
```

## How to Run

1. Clone this repository:

```bash
git clone https://github.com/workbydevansh/mnist-digit-classification.git
```

2. Open `mnist_classification.ipynb` in Google Colab or Jupyter Notebook.

3. Run the notebook cells sequentially.

The MNIST dataset is automatically downloaded through Keras, so no manual dataset upload is required.

## Future Improvements

* Add a confusion matrix
* Compare different neural network architectures
* Experiment with dropout and regularization
* Compare the neural network with CNN-based classification
* Add prediction visualization for multiple test images

## Author

**Devansh Verma**

GitHub: [@workbydevansh](https://github.com/workbydevansh)
