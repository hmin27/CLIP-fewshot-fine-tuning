2023_Deep Learning Project

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
- **Default Configuration**: <br>
Learning rate: 1e-5 <br>
Batch size: 4 <br>
Momentum: 0.0 <br>
Weight decay: 0.0 <br>

- **Hyperparameter Variations**: <br>
Batch size: 2, 4, 8, 16, 32, 64 <br>
Learning rate: 1e-4 ~ 1e-7 <br>
Momentum: 0.0, 0.8, 0.9, 0.95, 0.99 <br>
Weight decay: 0.0, 1e-5 <br>

<br>
<br>

- **Training**:
Early stopping if validation loss does not decrease for 5 consecutive epochs.
Average of 20 epochs per experiment.

- **Evaluation**:
Top-1 and top-3 accuracy on the validation set.
Results averaged over multiple runs.

## Results
### Variation in momentum coefficient
<p align="left">
  <img src="https://github.com/user-attachments/assets/951682c1-9879-4533-8d90-b8ddd73e23ad", width="60%">
</p>

### Variation in learning rate with or without momentum
<p align="left">
  <img src="https://github.com/user-attachments/assets/42f56afe-e588-4aa6-87f5-f6cb59e2c49c", width="60%">
</p>

### Effect of weight decay according to different datasets
<p align="left">
  <img src="https://github.com/user-attachments/assets/233f1924-501e-422d-bb07-e0038722213e", width="60%">
</p>
