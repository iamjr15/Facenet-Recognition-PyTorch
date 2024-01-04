Here is a comprehensive README for the face recognition code:

# Face Recognition using Facenet, SVM, and PCA

This project implements a facial recognition system for identifying faces from a custom dataset. The system uses MTCNN for face detection, Facenet for facial feature extraction, SVM for classification, and PCA for dimensionality reduction and visualization.

## How it Works

The overall pipeline follows these key steps:

1. Face Detection: MTCNN detects and extracts face regions from input images
2. Feature Extraction: The detected face regions are passed through the Facenet model to generate 128-d facial embeddings
3. Training: An SVM model is trained on the embeddings and labels from the training set 
4. Classification: For any new image, the face embedding is extracted and fed to the SVM model for prediction
5. Visualization: PCA is used to reduce embeddings to 2d for visualization

## Key Components

**Models:**

- **MTCNN:** Face detector model
- **Facenet:** Inception ResNet V1 model pretrained on VGGFace2 dataset for facial feature extraction  
- **SVM:** Support Vector Machine model for classification

**Libraries:**

- facenet-pytorch: Provides MTCNN and Facenet models
- sklearn: SVM, PCA, metrics
- Matplotlib: Visualization plots

**Functions:**

- `extract_features()`: Face detection and embedding extraction
- `dataset_to_embeddings()`: Extract embeddings and labels for a dataset
- `train()`: Train classification SVM model
- `visualize()`: Generate 2D visualization plots

**Evaluation:** 

The model is evaluated using accuracy metric and classification report.

**Usage:**

Check the notebook for sample usage including training, evaluation and predictions.

## Requirements

Python 3.8+

See `requirements.txt` file for all package dependencies.

## References

Facenet PyTorch: https://github.com/timesler/facenet-pytorch

## Author
@Jigyansu Rout