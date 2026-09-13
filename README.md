# CNN-Based Eye Disease Diagnosis

### Deep Learning Approach on the ODIR-5K Dataset

## Project Overview

This project focuses on the detection of multiple eye diseases from retinal fundus images using deep learning.

A multi-label classification approach was developed using Convolutional Neural Networks (CNNs), allowing multiple disease categories to be identified from a single image.

## Dataset

The project uses the ODIR-5K dataset, which contains retinal fundus images annotated with eight diagnostic categories:

- Normal (N)
- Diabetic Retinopathy (D)
- Glaucoma (G)
- Cataract (C)
- Age-related Macular Degeneration (A)
- Hypertension (H)
- Myopia (M)
- Other (O)

The task is formulated as a multi-label classification problem, where an image can be associated with multiple disease labels.

## Methodology

The project follows a transfer learning-based deep learning pipeline:

**Preprocessing → Data Augmentation → EfficientNetB0 → Fine-Tuning → Threshold Tuning → Evaluation**

EfficientNetB0 with ImageNet pretrained weights was used as the backbone for multi-label classification. The model was trained in two stages, followed by class-specific threshold optimization on the validation set.

Weighted Binary Crossentropy was used to address class imbalance.

## Model Selection & Experiments

A total of 23 different model configurations were evaluated during the experimentation process. Based on their performance, the four most promising models were selected for detailed comparison.

The selected models were further evaluated using Macro F1, Macro Recall, Macro ROC-AUC, and Macro PR-AUC.

## Results

| Model | Macro F1 | Macro Recall | Macro ROC-AUC | Macro PR-AUC |
|---|---:|---:|---:|---:|
| Model 1 | 0.3912 | 0.5640 | 0.7739 | 0.4439 |
| Model 2 | 0.4449 | 0.5568 | 0.7877 | 0.4546 |
| **Model 3** | **0.4624** | **0.5840** | **0.8014** | **0.4734** |
| Model 4 | 0.4454 | 0.5836 | 0.7805 | 0.4583 |

Model 3 achieved the best overall performance among the four selected configurations.

## Project Structure

```text
├── notebooks/
│   ├── model_01_experiment.html
│   ├── model_02_experiment.html
│   ├── model_03_experiment.html
│   └── model_04_experiment.html
│
├── presentation/
│   ├── CNN_Eye_Disease_Diagnosis.pptx
│   └── CNN_Eye_Disease_Diagnosis.pdf
│
└── README.md
```
## Academic Team Project

This project was developed collaboratively as a university team project.

**Team Members:**

- Özcan Kocaman
- Betül Balcı
- Serra Demirel
- Sedef Birgül
- Zehra Yılmaz

## Presentation

The project presentation is included in the repository.
