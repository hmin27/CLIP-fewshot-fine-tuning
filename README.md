2023_Deep Learning Project

# Improve the Few shot learning Using CLIP
Fine-tuning the CLIP for few shot learning and fine the optimal hyperparameter configurations in terms of momentum.
- Used Datasets: Food, EuroSAT, Caltech, Flower102, Caltech101, Fgvc-aircraft, Standford Cars
- Split all the datasets into 4shot train/validation
- Evaluation of image classification is performed by top k accuracy in validation set
- Comparing the performance in FSL using different momentum methods 

# Improve Few-Shot Learning Using CLIP
## Project Overview
This project focuses on enhancing the performance of few-shot learning by fine-tuning the CLIP model and optimizing hyperparameter configurations, particularly momentum.

## Objectives
- Fine-tune CLIP for few-shot learning.
- Identify optimal hyperparameter settings, with a focus on momentum.
- Understand the mechanisms of how few-shot learning operates.
  
## Datasets Utilized
- Food
- EuroSAT
- Caltech
- Flower102
- Caltech101
- FGVC-Aircraft
- Stanford Cars

## Methodology
All datasets were split into 4-shot train/validation sets.
Image classification performance was evaluated using top-k accuracy on the validation set.
The performance of few-shot learning was compared using different momentum methods.

## Environmental Setup
- **Platform**: Google Colab Pro with T4 GPUs
- **Model**: CLIP ViT-B/32
- **Default Configuration**:
Learning rate: 1e-5
Batch size: 4
Momentum: 0.0
Weight decay: 0.0
Hyperparameter Variations:
Batch size: 2, 4, 8, 16, 32, 64
Learning rate: 1e-4, 1e-5, 5e-5, 1e-6, 1e-7
Momentum: 0.0, 0.8, 0.9, 0.95, 0.99
Weight decay: 0.0, 1e-5
</br>
- **Training**:
Early stopping if validation loss does not decrease for 5 consecutive epochs.
Average of 20 epochs per experiment.
- **Evaluation**:
Top-1 and top-3 accuracy on the validation set.
Results averaged over multiple runs.
