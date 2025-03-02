# CIFAR-10 Classification

## Dataset
- The CIFAR-10 dataset is automatically downloaded using `torchvision.datasets`.
- Preprocessed by normalizing pixel values and split into training, validation, and test sets.

## Model Architecture
- **Input layer**: 3072 neurons (Flattened 32x32x3 images)
- **Hidden layers**: Two fully connected layers (256, 128 neurons)
- **Dropout layer**: 0.3 probability after the first hidden layer to reduce overfitting
- **Output layer**: 10 neurons (handled in loss function)

## Hyperparameter Tuning
- **Hidden Layers**: 2
- **Neurons per Layer**: [256, 128]
- **Optimizer**: Adam
- **Learning Rate**: 1e-3
- **Batch Size**: 32
- **Activation Function**: ReLU
- **Regularization**: Dropout (0.3 probability)

## Training & Evaluation
- **Training**: 5 epochs using Adam optimizer and Cross-Entropy Loss
- **Evaluation**: Validation and test set accuracy computed
- **Confusion Matrix**: Plotted for classification performance

## Findings
- **Optimal Hyperparameters**: ReLU activation, Adam optimizer, and batch size of 32
- **Effect of Dropout**: 0.3 probability reduced overfitting
- **Accuracy**:
  - Validation Accuracy: ~70%
  - Test Accuracy: ~69%
