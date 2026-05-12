# Dog-Breed-Predict
Deep learning–based dog breed classification system built with MobileNetV2 and transfer learning on the Stanford Dogs dataset.  
The model classifies around 120 dog breeds and achieves 67.92% test accuracy using fine‑tuning and data augmentation.

## Dataset



This project uses the Dog Breed Identification dataset from Kaggle.

The dataset contains thousands of dog images belonging to 120 different dog breeds. Each image is labeled with its corresponding breed, enabling supervised training for image classification.

The dataset includes:

- A train folder containing labeled dog images.
- A labels.csv file that maps each image ID to its corresponding dog breed.
- A test set used for prediction tasks.

The images vary in lighting conditions, backgrounds, and dog poses, which makes the classification task more challenging and realistic. This diversity helps the model learn robust visual features for distinguishing between many similar dog breeds.

## Model

The final model is a **transfer learning–based image classification system** built on **MobileNetV2**, pretrained on the ImageNet dataset. MobileNetV2 was selected due to its strong performance–to–efficiency ratio, making it suitable for training and inference on limited GPU resources while still achieving high accuracy.

The model uses a custom classification head consisting of:
- Global Average Pooling
- Fully connected layer with ReLU activation
- Dropout for regularization
- Softmax output layer for multi-class classification

To improve generalization and robustness, **data augmentation** layers are integrated directly into the model. After an initial training phase with frozen backbone layers, **fine‑tuning** was applied by unfreezing the upper layers of MobileNetV2 and training with a low learning rate.

The final model achieves a **test accuracy of 67.92%** on a challenging multi-class dog breed classification task (~120 classes), demonstrating strong generalization and stability. The model is suitable for deployment and further extension, such as ensemble learning or higher-resolution inputs.


## Technologies Used
- Python
- MobileNetV2 (Transfer Learning)
- TensorFLow
- Keras
- Numpy
- Pandas
- Matplotlib
- Scikit-Learn

## DataSet Source
https://www.kaggle.com/datasets/catherinehorng/dogbreedidfromcomp/data
