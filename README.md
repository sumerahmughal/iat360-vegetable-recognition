# Vegetable Recognition and Recipe Suggestions Using YOLO

**Course:** IAT 360 – Computer Vision Final Project · **Group 1**
**Members (student no.):** Alyssa Tao ([ ]), Antony Kumar ([ ]), Grace Jin ([ ]), Sumerah Mughal ([ ])

## Report
[report/Final_Report.pdf](report/Final_Report.pdf)

## Task
Image classification with a pretrained YOLO11n-cls model. Five classes: broccoli, capsicum, carrot, potato, tomato.

## Repository structure
| Path | Contents |
|---|---|
| `dataset/` | YOLO classification folders (train, val, test) and the 120 group photos |
| `notebooks/` | Baseline and hyperparameter experiment notebooks |
| `config.yaml` | Dataset paths and class names |
| `results/` | Metrics, classification reports, confusion matrices, example predictions |
| `screenshots/` | Training and evaluation screenshots |
| `report/` | Final report PDF |

## How to run
1. `pip install -r requirements.txt`
2. Check the paths in `config.yaml`.
3. Train the baseline in `notebooks/[name].ipynb`, then run the experiment notebooks.
4. Evaluate with `notebooks/[evaluation notebook].ipynb`.

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

![Example predictions](results/example_predictions.png)

## Dataset
- Online source: [Vegetable Image Dataset (Kaggle)](https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset). Licence: [status]
- Group photos: 30 per member, sorted into class folders. Labels come from the folder names.
- Initial bounding-box exploration used [Make Sense](https://makesense.ai). These boxes were not used for the final labels.

## Corrections to the PDF
- Table 11: per-class precision and F1 were recomputed from the confusion matrix. Broccoli precision is 0.774, not 1.000. Macro values are unchanged.
- Section 4.4: the 100-epoch model is 8.4 percentage points higher than the 25-epoch model, not 10.9.
- Baseline settings: [list the full settings from the run log].

## Citations
- Ultralytics. (n.d.). YOLO image classification documentation. https://docs.ultralytics.com/tasks/classify/
- Jocher, G., & Qiu, J. (2024). Ultralytics YOLO11 [Computer software]. https://github.com/ultralytics/ultralytics
- Ahmed, M. (n.d.). Vegetable image dataset [Data set]. Kaggle. https://www.kaggle.com/datasets/misrakahmed/vegetable-image-dataset
- Skalski, P. (n.d.). make-sense [Computer software]. https://github.com/SkalskiP/make-sense
- Keskar, N. S., et al. (2017). On large-batch training for deep learning. https://arxiv.org/abs/1609.04836
