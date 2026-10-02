# PRODIGY_ML_04 – Hand Gesture Recognition

Task 4 of my Machine Learning internship at **Prodigy InfoTech**.

## Objective
Recognize and classify 10 hand gestures from infrared images to enable gesture-based human–computer interaction.

## Dataset
[LeapGestRecog (Kaggle)](https://www.kaggle.com/datasets/gti-upm/leapgestrecog) – 20,000 images, 10 gestures, 10 subjects

## Approach
- **Transfer learning** with MobileNetV2 (ImageNet weights) + data augmentation
- **Fine-tuning** of the last layers (low learning rate, early stopping)
- **Subject-wise split** to avoid data leakage: train on subjects 00–06, validate on 07, test on 08–09

## Results (unseen subjects)
| Metric | Value |
|---|---|
| Test accuracy | **94.2 %** |
| Perfect classes | down, index, palm_moved |
| Main confusion | fist ↔ fist_moved / thumb |

## Tools
Python, TensorFlow/Keras, Scikit-learn, Pandas, Matplotlib
