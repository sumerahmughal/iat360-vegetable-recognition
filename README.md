# Vegetable Recognition and Recipe Suggestions Using YOLO

**Course:** IAT 360 – Computer Vision Final Project · **Group 1**
**Members :** Alyssa Tao, Antony Kumar, Grace Jin, Sumerah Mughal

## Task
Image classification with a pretrained YOLO11n-cls model. Five classes: broccoli, capsicum, carrot, potato, tomato.

## Results
Accuracy on 120 independently collected group photos (24 per class). All models scored 98.3–100% on the online test set.

| Experiment | Setting | Accuracy |
|---|---|---|
| Baseline | 224 px, batch 16, 15 epochs, lr0 0.01 (auto optimizer) | 73.3% |
| Batch size | 8 | 79.2% |
| Image size | 320 px | 75.8% |
| Learning rate | 0.001 (AdamW) | 77.5% |
| Epochs | 100 | 79.2% |

**Selected model:** 100 epochs. Macro precision 0.794, recall 0.792, F1 0.788.

## Dataset
- Online source: [Vegetable Image Dataset (Kaggle)](https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset). Licence: [status]
- Group photos: 30 per member, sorted into class folders. Labels come from the folder names.

## Corrections to the PDF
- Table 11: per-class precision and F1 were recomputed from the confusion matrix. Broccoli precision is 0.774, not 1.000. Macro values are unchanged.
- Section 4.4: the 100-epoch model is 8.4 percentage points higher than the 25-epoch model, not 10.9.

## Citations
- Ultralytics. (n.d.). YOLO image classification documentation. https://docs.ultralytics.com/tasks/classify/
- Jocher, G., & Qiu, J. (2024). Ultralytics YOLO11 [Computer software]. https://github.com/ultralytics/ultralytics
- Ahmed, M. (n.d.). Vegetable image dataset [Data set]. Kaggle. https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset
- Skalski, P. (n.d.). make-sense [Computer software]. https://github.com/SkalskiP/make-sense
- Keskar, N. S., et al. (2017). On large-batch training for deep learning. https://arxiv.org/abs/1609.04836

## Google Drive (Shared Photo)
https://drive.google.com/drive/folders/13RmDr23rKxwQBszpCTxYbo_J7gasF5Ak?usp=sharing
