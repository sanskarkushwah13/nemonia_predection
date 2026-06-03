# Medical Image Classification

This repository contains a deep learning project for classifying chest X-ray images as Normal or Pneumonia. The implementation is based on TensorFlow/Keras and uses notebook-driven preprocessing, training, evaluation, and visualization.

## Project Structure

- `DS2/` - dataset folder containing chest X-ray images for training, validation, and testing
- `imageprocessing.ipynb` - image loading, resizing, preprocessing, and dataset preparation steps
- `MedicalImageClassification.ipynb` - model building, training, validation, evaluation, and prediction workflow
- `imageClassificationModel.h5` - saved trained model file
- `.gitignore` - ignored files and folders
- `.gitattributes` - Git attributes configuration

## Key Features

- Image preprocessing and augmentation
- CNN model architecture for binary classification
- Training with callbacks: `ModelCheckpoint` and `EarlyStopping`
- Evaluation with accuracy and confusion matrix metrics
- Visualization of training history and sample images
- Saved model for reuse without retraining

## Requirements

Install the required Python libraries before running the notebooks:

```bash
pip install numpy pandas matplotlib opencv-python tensorflow keras scikit-learn jupyter pillow seaborn
```

> Note: Depending on your environment, `tensorflow` may already include Keras.

## How to Run

1. Open the project folder in VS Code or Jupyter.
2. Confirm the dataset is present under `DS2/` with the expected `train`, `validation`, and `test` subfolders.
3. Start Jupyter Notebook:

```bash
jupyter notebook
```

4. Open and run `imageprocessing.ipynb` to prepare the image dataset.
5. Open and run `MedicalImageClassification.ipynb` to build, train, and evaluate the model.
6. Optionally load the saved model from `imageClassificationModel.h5` for inference.

## Loading the Saved Model

Example:

```python
from tensorflow.keras.models import load_model

model = load_model("imageClassificationModel.h5")
```

## Recommended Workflow

- Preprocess the images and verify the dataset structure
- Build the model architecture
- Train with `train_generator` and validate with `validation_generator`
- Plot training accuracy and loss curves
- Run model predictions on the test set
- Display sample images from train/validation folders

## Notes

- Keep the dataset folder structure consistent with notebook paths.
- If you move the dataset, update the path variables in the notebooks.
- If model loading fails, verify the installed TensorFlow/Keras version matches the version used during training.

## Author
Medical Image Classification Project
