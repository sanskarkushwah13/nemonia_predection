Medical Image Classification
This project uses deep learning to classify medical images into different categories. It includes image preprocessing, model training/evaluation notebooks, a saved trained model, and a dataset folder.

Project Structure
.
├── DS2/
│   └── Dataset files
├── imageprocessing.ipynb
├── MedicalImageClassification.ipynb
├── imageClassificationModel.h5
├── .gitignore
└── .gitattributes
Files
DS2/ contains the medical image dataset used for training and testing.
imageprocessing.ipynb contains image loading, resizing, cleaning, preprocessing, and dataset preparation steps.
MedicalImageClassification.ipynb contains the model building, training, evaluation, and prediction workflow.
imageClassificationModel.h5 is the saved trained model file.
Features
Medical image preprocessing
Image classification using a deep learning model
Model training and evaluation
Saved model for reuse without retraining
Notebook-based workflow for easy experimentation
Requirements
Install the required Python libraries before running the notebooks:

pip install numpy pandas matplotlib opencv-python tensorflow keras scikit-learn jupyter
Depending on the notebook contents, you may also need:

pip install pillow seaborn
How to Run
Open the project folder.
Make sure the dataset is available inside the DS2/ folder.
Start Jupyter Notebook:
jupyter notebook
Run imageprocessing.ipynb to preprocess the images.
Run MedicalImageClassification.ipynb to train, evaluate, or test the classification model.
Use imageClassificationModel.h5 to load the saved model for predictions.
Loading the Saved Model
Example:

from tensorflow.keras.models import load_model

model = load_model("imageClassificationModel.h5")
Model Workflow
Load medical image dataset
Preprocess images
Split data into training and testing sets
Build the image classification model
Train the model
Evaluate model performance
Save or load the trained model
Use the model for predictions
Notes
Keep the dataset folder structure consistent with the notebook code.
Large dataset files and trained model files may be excluded from Git depending on .gitignore.
If the saved model does not load, check that the TensorFlow/Keras version matches the version used during training.
Author
Medical Image Classification Project
