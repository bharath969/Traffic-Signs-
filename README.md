# Traffic Signs Labelling

## Overview
This project focuses on building a deep learning model to classify traffic signs into one of 43 different categories. The dataset used is the German Traffic Sign Recognition Benchmark (GTSRB), and onvolutional neural network architectures such Lenet etc are implemented for the classification task.

![Traffic Sign Example](https://upload.wikimedia.org/wikipedia/commons/b/b6/UK_traffic_sign_543.svg)

### Problem Statement
The aim is to develop a machine learning model capable of identifying and classifying various traffic signs from images. Such a model can assist autonomous driving systems in recognizing and responding to traffic signs in real-time.

The dataset will be trained don Lenet CNN and a regular CNN

### Dataset
The dataset contains 43 classes, including but not limited to:
- Speed limit signs (e.g., 20km/h, 30km/h, 50km/h)
- Warning signs (e.g., Dangerous curves, Slippery road)
- Mandatory signs (e.g., Keep right, Roundabout mandatory)
- Prohibitory signs (e.g., No passing, No entry)

The data is too large to be uploaded here.`Do find the dataset at this link:`

A complete list of classes is provided within the project notebook.

## Project Features
- **Deep Learning Architecture**: Implementation of LeNet, a convolutional neural network originally developed by Yann LeCun for handwritten digit recognition.
- **Preprocessing**: Image resizing, normalization, image augumentation,coverted the image from rgb to gray as LeNet generally work on gray images
- **Data Augumentation:** The dataset is imabalanced and using datagenerator from sklear,generated thrice thedataset fro the classes which have less than 500 samples in the datset
- **Training & Evaluation**: Models training on a labeled dataset with performance evaluation metrics like accuracy.
- - Trained 4 models on this data
  - - `Model 1:` Letnet Cnn
    - `Model 2:` Lenet CNN + Data Augumentation
    - `Model 3:` Regualr cnn + Hyperp parameter tuning
    - `Model 4:` Regular cnn + Hyperp parameter tuning + Data Augumentation
## Summary
| Model         | Loss | Accuracy |
|---------------|------|----------|
| Lenet         | 0.78 | 0.87     |
| Lenet+Aug     | 0.81 | 0.84     |
| CNN+hyp       | 0.41 | 0.97     |
| CNN+hyp+Aug   | 0.50 | 0.96     |

## Inference
- Trained both the normal data and augumented data  on the above models and We will be reading the traffic signs using model 3 which as an accuracy of 97%
- The model 3 omly performs poorly on the pedestrain signs (Refer below classification reports) and heatmap for the confusion matrix provided in the files
| Class                                        | Precision | Recall | F1-score | Support |
|----------------------------------------------|-----------|--------|----------|---------|
| Speed limit (20km/h)                         | 0.92      | 1.00   | 0.96     | 55      |
| Speed limit (30km/h)                         | 0.99      | 0.98   | 0.98     | 727     |
| Speed limit (50km/h)                         | 0.99      | 0.99   | 0.99     | 747     |
| Speed limit (60km/h)                         | 0.96      | 0.99   | 0.97     | 433     |
| Speed limit (70km/h)                         | 0.98      | 0.99   | 0.98     | 652     |
| Speed limit (80km/h)                         | 1.00      | 0.90   | 0.94     | 697     |
| End of speed limit (80km/h)                  | 0.92      | 0.99   | 0.96     | 139     |
| Speed limit (100km/h)                        | 0.98      | 1.00   | 0.99     | 443     |
| Speed limit (120km/h)                        | 0.94      | 0.97   | 0.96     | 437     |
| No passing                                   | 1.00      | 0.98   | 0.99     | 489     |
| No passing for vehicles over 3.5 metric tons | 0.99      | 1.00   | 0.99     | 656     |
| Right-of-way at the next intersection        | 0.99      | 0.91   | 0.95     | 460     |
| Priority road                                | 0.93      | 1.00   | 0.97     | 644     |
| Yield                                        | 0.99      | 1.00   | 0.99     | 710     |
| Stop                                         | 1.00      | 0.94   | 0.97     | 287     |
| No vehicles                                  | 1.00      | 0.85   | 0.92     | 247     |
| Vehicles over 3.5 metric tons prohibited     | 1.00      | 0.97   | 0.98     | 155     |
| No entry                                     | 1.00      | 1.00   | 1.00     | 360     |
| General caution                              | 0.93      | 0.99   | 0.96     | 366     |
| Dangerous curve to the left                  | 1.00      | 0.88   | 0.94     | 68      |
| Dangerous curve to the right                 | 0.94      | 0.86   | 0.90     | 99      |
| Double curve                                 | 0.83      | 0.85   | 0.84     | 88      |
| Bumpy road                                   | 0.82      | 0.97   | 0.89     | 101     |
| Slippery road                                | 1.00      | 0.82   | 0.90     | 183     |
| Road narrows on the right                    | 0.88      | 1.00   | 0.93     | 79      |
| Road work                                    | 0.96      | 0.95   | 0.96     | 487     |
| Traffic signals                              | 0.97      | 0.97   | 0.97     | 179     |
| Pedestrians                                  | 0.50      | 0.91   | 0.65     | 33      |
| Children crossing                            | 0.99      | 0.98   | 0.98     | 151     |
| Bicycles crossing                            | 0.93      | 1.00   | 0.97     | 84      |
| Beware of ice/snow                           | 0.77      | 0.94   | 0.85     | 122     |
| Wild animals crossing                        | 0.96      | 0.97   | 0.96     | 267     |
| End of all speed and passing limits          | 1.00      | 1.00   | 1.00     | 60      |
| Turn right ahead                             | 1.00      | 0.98   | 0.99     | 215     |
| Turn left ahead                              | 1.00      | 0.98   | 0.99     | 122     |
| Ahead only                                   | 0.97      | 1.00   | 0.99     | 379     |
| Go straight or right                         | 1.00      | 0.99   | 1.00     | 121     |
| Go straight or left                          | 1.00      | 0.98   | 0.99     | 61      |
| Keep right                                   | 1.00      | 0.98   | 0.99     | 702     |
| Keep left                                    | 0.97      | 0.96   | 0.96     | 91      |
| Roundabout mandatory                         | 0.96      | 0.85   | 0.90     | 101     |
| End of no passing                            | 0.73      | 1.00   | 0.85     | 44      |
| End of no passing by vehicles over 3.5 metric tons | 0.99 | 1.00   | 0.99     | 89      |
| **Accuracy**                                 | **0.97**  |        |          | **12630** |
| **Macro avg**                                | **0.95**  | **0.96**| **0.95** | 12630   |
| **Weighted avg**                             | **0.97**  | **0.97**| **0.97** | 12630   |



- The mislabelling of the pedestrian class might be because of the following reasons (less sample data,Low quality of the image,similarities with other classes such as yiled)
- Apart from that this model performs very well on all classes and you can see the same from the macro avg and weighted average in the classsification report
- **Overall Performance of the Model 3:**
- - Accuracy: 0.97
  - Macro Avg Precision: 0.95
  - Macro Avg Recall: 0.96
  - Weighted Avg Precision: 0.97
  - Weighted Avg Recall: 0.97

**So we can conlude that Model 3 is the best for reading traffic signs**
  



