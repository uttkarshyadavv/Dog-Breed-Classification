# 🐶 Dog Breed Identification — Multi-Class Image Classification
 
Identifying the breed of a dog from an image using Deep Learning and Transfer Learning.
 
> *"When I'm sitting at a cafe and take a photo of a dog, I want to know what breed it is."*
 
---
 
## Problem
 
Given an image of a dog, predict its breed from **120 possible breeds** — a multi-class image classification problem using unstructured data (images).
 
## Data
 
- Source: [Kaggle Dog Breed Identification Competition](https://www.kaggle.com/c/dog-breed-identification/data)
- ~10,000+ labeled training images
- ~10,000+ unlabeled test images
- 120 unique dog breeds
## Model
 
- **Architecture:** Transfer Learning with **MobileNetV2** (via TensorFlow Hub)
- **Framework:** TensorFlow 2.x + Keras
- **Input size:** 224 × 224 px (normalized to 0–1)
- **Output:** Prediction probabilities for each of 120 breeds
- **Callbacks:** EarlyStopping + TensorBoard
## Workflow
 
1. Load and explore data (labels + image file paths)
2. Preprocess images → Tensors (resize, normalize, batch)
3. Build transfer learning model using MobileNetV2
4. Train on 1,000 images first (experiment), then full dataset
5. Evaluate predictions with confidence visualization
6. Generate Kaggle submission CSV with prediction probabilities
## Results
 
- Trained on full dataset (~10,000 images)
- Model saved as `.h5` and reloaded successfully
- Predictions exported to CSV for Kaggle submission
- Visualized top-10 prediction confidences per image
## Key Libraries
 
- TensorFlow 2.x
- TensorFlow Hub
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
## How to Run
 
1. Clone the repo
2. Install dependencies: `pip install -r requirements.txt`
3. Open `dog_vision.ipynb` in Google Colab
4. Mount Google Drive and point paths to your dataset
5. Run all cells
## Evaluation
 
Submission format follows [Kaggle evaluation criteria](https://www.kaggle.com/c/dog-breed-identification/overview/evaluation) — prediction probability for each breed per test image.
 
---
 
*Part of my ML portfolio — built while learning from the Zero To Mastery ML course.*
