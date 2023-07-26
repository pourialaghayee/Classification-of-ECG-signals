# Classification-of-ECG-signals
In this project we aim to classify a bunch of recorded ECG signals. To this end, you will implement two models with different architectures: 1- LSTM neural network and 2- Convolutional neural network.

The electrocardiogram (ECG) is a tool used in cardiology to record the heart's electrical activity. At every beat, the heart is depolarized to trigger its contraction. This electrical activity is transmitted throughout the body and can be picked up on the skin. An ECG machine records this activity via electrodes on the skin and displays it graphically. The machine processes the signals picked up from the skin by electrodes and produces a graphic representation of the patient's heart's electrical activity.

In the results, it is shown that LSTM has achieved a higher accuracy in the ROC_AUC criterion. But the number of epochs is two and a half times the CNN model. The reason is that CNN converges much faster in fewer epochs and achieves high accuracy. In general, we can say that LSTM tries to find long relationships between sequences, while convolution tries to find local relationships.

The convolution model has more parameters and the reason is that in the LSTM model we have the conditions to share parameters. However, in the convolution model the parameters are shared only in each layer, but in LSTM all parameters are the same in all layers. It is a weight matrix and is updated during different executions.

To be more specific, the convolution model is appropriate for the problem when the relationships between the fields are local. This is to the extent that the convolution model can understand them and achieve high accuracy. We said above that in the given sample, convolution had reached high accuracy. The reason is that the relationships between the fields are such that a convolution model with the appropriate kernel size can fully understand them and train an accurate model. So, in general, CNN is also suitable for some sequence problems, but if the relationships between the disciplines are such that the parts with a long distance have many relationships with each other, LSTM and RNN models will do this better. 


## LSTM Performance

- ROC_AUC Score: 0.9403510564367388
- Parameters for lstm classifier: 19397

| Metrics | 0 | 1 | 2 | 3 | 4 | Accuracy | Macro Avg | Weighted Avg |
|---------|---|---|---|---|---|----------|-----------|--------------|
| Precision | 0.98 | 0.25 | 0.73 | 0.21 | 0.92 | - | 0.62 | 0.94 |
| Recall | 0.88 | 0.70 | 0.89 | 0.88 | 0.89 | - | 0.85 | 0.88 |
| F1-Score | 0.93 | 0.36 | 0.80 | 0.34 | 0.90 | - | 0.67 | 0.90 |
| Support | 18118 | 556 | 1448 | 162 | 1608 | 21892 | 21892 | 21892 |

## CNN Performance

- ROC_AUC Score: 0.9188220972594315
- Parameters for conv classifier: 384453

| Metrics | 0 | 1 | 2 | 3 | 4 | Accuracy | Macro Avg | Weighted Avg |
|---------|---|---|---|---|---|----------|-----------|--------------|
| Precision | 0.99 | 0.53 | 0.70 | 0.16 | 0.83 | - | 0.64 | 0.94 |
| Recall | 0.90 | 0.67 | 0.91 | 0.85 | 0.95 | - | 0.86 | 0.90 |
| F1-Score | 0.94 | 0.59 | 0.79 | 0.27 | 0.88 | - | 0.70 | 0.91 |
| Support | 18118 | 556 | 1448 | 162 | 1608 | 21892 | 21892 | 21892 |

