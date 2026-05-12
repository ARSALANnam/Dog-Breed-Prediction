# Dog-Breed-Predict



## Dataset

The final dataset consists of images from the **Stanford Dogs dataset**, covering approximately **120 dog breeds** with high inter-class visual similarity. This dataset represents a realistic and challenging fine-grained image classification problem.

All images were:
- Resized to a fixed input resolution compatible with the model
- Preprocessed using the **MobileNetV2-specific preprocessing function**
- Split into training, validation, and test sets using **stratified sampling** to preserve class balance
- Augmented during training to improve diversity and reduce overfitting

The final dataset configuration ensures fair evaluation, balanced learning across classes, and reliable performance estimation. Combined with transfer learning and fine-tuning, this dataset setup enables the model to achieve strong results while remaining computationally efficient.

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
