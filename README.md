# Digit Classification using SVD (Mini-project)

This repository contains a mini-project for classifying handwritten digits using linear algebra and Singular Value Decomposition (SVD).
The model creates a basis (a subspace) for each digit based on the training data and then classifies test images based on which subspace the image can best be approximated by (i.e., the lowest residual error).

The Jupyter Notebook (`Miniproject_2.ipynb`) performs the following steps:
1. **Data Handling:** Loads training data in numpy format.
2. **Training (SVD):** Sorts images by digit (0-9) and computes the Singular Value Decomposition (SVD) to extract the most important features (singular vectors/singular images).
4. **Visualization:** Plots the singular values and the dominant singular images to understand the data structure (demonstrated for digits 3 and 8, for example).
6. **Testing and Classification:** Loads test data. Each test image is projected onto the first $k$ singular vectors for each digit. The image is classified as the digit that yields the smallest residual error.
8. **Evaluation:** Calculates and prints the model's accuracy (success rate) for different numbers of basis vectors ($k=5$ to $15$) across all ten digits, compiled in a clean table.

## Training and Test Data
The data files (`.npy`) are too large to be hosted directly on GitHub and are therefore hosted externally. Please download them via my Google Drive and place them in the same directory as the notebook before running the code.

## Data
Download the files from here: https://drive.google.com/drive/folders/1MfnZ8BIPRGVEOGl2SpmAR2ZLmV0MneCz?usp=sharing

Files that should be in the root directory:
* `TrainDigits.npy`
* `TrainLabels.npy`
* `TestDigits.npy`
* `TestLabels.npy`

## Requirements and Dependencies
To run this project, you need Python installed along with the following libraries:
* `numpy`
* `matplotlib`
* `pandas`

You can easily install the dependencies via your terminal:
```bash
pip install numpy matplotlib pandas
