# CIFAR-10 

The CIFAR-10 dataset consists 60,000 color images, each with a resolution of 32x32 pixels, distributed across 10 classes. There are 6,000 images per class, making it a well-known and commonly used benchmark in the field of computer vision.

## Requirements
* Python v3
* numpy==1.23.5
* torch==2.1.0
* torchmetrics==1.3.0.post0
* torchvision==0.16.0
* tqdm==4.66.1


## Model Building and Evaluation Report 

### Model Architecture
The technique adopted is a straightforward approach of creating a model using convolution layer. The first is 2 convolution layers followed by maxpooling layer of size 3x3, followed by two fully-connected layers (CNN1). The second is by using three convolutional layers, two max-pooling layer of size 3x3, finishing with a single fully-connected layer for prediciton (CNN2). In order to perserve the input size of the images, padding was used.

### Loss Function
As working with a multi-class classification task, Cross Entropy loss function was selected.

### Optimizer Comparison
Two optimizers were evaluated and compared: Mini-Batch Gradient Descent and Adam optimizers. 

For the first, 5 fold cross-validation was applied during training with batch size of 32 . After running it on 3 epochs and using the CNN1, the final validation accuracy was 57.65%.

For Adam, using CNN2, the K-Fold cross validation approach was removed and replaced by simply dividing the training dataset into 80% and 20% of training and validation datasets, respectively. After running it for 80 epochs, the validation accuracy resulted in 74.56%.


### Model Performance on Test
Apply the model on the testing set, the results on the evaluation metrics are:
* Accuracy: 77.34
* Precision: 77.27
* Recall: 77.34
* F1-score: 77.11


## Issues:
**Computational resource limitation**:  model training and validation process consumed a considerable amount of time during the cross-validation due to limited computational power. This would result in avoiding applying hyperparameter tuning using searching.


## Future Enhancements:
1. **Model enhancement**: adjust the model architecture by adding more layers and add complexity to better capture data features.
2. **Hyperparamters optimization**: continue the hyperparameter tuning process, focusing on the Adam optimizer, to identify the best combination that can lead to the best possible performance.


