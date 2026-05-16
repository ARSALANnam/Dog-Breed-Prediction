# Dog Breed Prediction

This project is a deep learning-based dog breed classification system developed using TensorFlow and Keras. The model is trained on the Kaggle Dog Breed Identification dataset containing 120 dog breeds and uses Transfer Learning with MobileNetV2 to achieve accurate multi-class image classification.

Techniques such as data augmentation, dropout regularization, and learning rate scheduling were applied to improve performance and reduce overfitting. The final model achieved approximately 68% test accuracy while remaining efficient enough to run on consumer-grade GPU hardware.


## Dataset
This project uses the Dog Breed Identification dataset from Kaggle.

The dataset contains thousands of dog images belonging to 120 different dog breeds.Each image is labeled with its corresponding breed, enabling supervised training for image classification.
The dataset includes:

- A train folder containing labeled dog images.
- A labels.csv file that maps each image ID to its corresponding dog breed.
- A test set used for prediction tasks.

The images vary in lighting conditions, backgrounds, and dog poses, which makes the classification task more challenging and realistic. This diversity helps the model learn robust visual features for distinguishing between many similar dog breeds.

## Model
The model is based on Transfer Learning using MobileNetV2, a lightweight convolutional neural network architecture pre-trained on ImageNet. Transfer learning allows the model to leverage previously learned visual features and adapt them to the task of dog breed classification.

The architecture consists of:

- MobileNetV2 as the feature extractor (pre-trained on ImageNet).
- A Global Average Pooling layer to reduce spatial dimensions.
- Fully connected Dense layers for classification.
- Dropout layers to reduce overfitting.

To improve generalization and performance, several techniques were applied:

- Data Augmentation (random flip, rotation, zoom, and translation) to increase dataset diversity.
- EarlyStopping to stabilize training.

The final model achieves around 68–69% accuracy on the test set when classifying among 120 dog breeds, which is a solid result for this multi-class image classification problem.

## Technologies Used

- Python
- MobileNetV2 (Transfer Learning)
- TensorFLow
- Keras
- Scikit-Learn
- Numpy
- Pandas
- Matplotlib
- Seaborn
- Plotly

## DataSet Source
LINK : https://www.kaggle.com/datasets/catherinehorng/dogbreedidfromcomp/data

## Working on a project............
