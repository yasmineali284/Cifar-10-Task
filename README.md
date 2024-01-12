# CIFAR-10 

The CIFAR-10 dataset consists 60,000 color images, each with a resolution of 32x32 pixels, distributed across 10 classes. There are 6,000 images per class, making it a well-known and commonly used benchmark in the field of computer vision.

## Requirements
* Python v3
* numpy==1.23.5
* torch==2.1.0
* torcheval==0.0.7
* torchvision==0.16.0
* tqdm==4.66.1


## Model Building and Evaluation Report 

### Model Architecture
The technique adopted is a straightforward approach of creating a model of two convolutional layers, max-pooling layer, finishing with a fully-connected layer. In order to perserve the input size of the images, padding was used.

### Loss Function
As working with a classification task, Cross Entropy loss function was selected.

### Optimizer Comparison
Two optimizers were evaluated and compared. After 3 epochs, the Adam optimizer outperformed Mini-Batch Gradient Descent, resulting in 65.61% and 57.56% validation accuracy, respectively. 

### Model Performance on Test
The initial model using the Adam optimizer has resulted in 56% on the testsets.

### Hyperparameter Tuning
To optimize the Adam optimizer parameters, hyperparameter tuning was initiated. This was taken to achieve the best possible outcome on the validation/test result.


## Issues:
1. **Underfitting**: the model show signs of underfitting, suggesting a need for higher complexity and capacity to capture the underlying patterns in data.
2. **Computational resource limitation**: model training and validation process consumed a considerable amount of time due to limited computational power. 


## Future Enhancements:
1. **Model enhancement**: adjust the model architecture by adding more layers and add complexity to better capture data features.
2. **Extend number of epochs**: by increasing the number of epochs, it may leave room for better performance.
3. **Hyperparamters optimization**: continue the hyperparameter tuning process, focusing on the Adam optimizer, to identify the best combination that can lead to the best possible performance.


