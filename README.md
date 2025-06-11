# CNN
## Trained a CNN on CIFAR-10, then use transfer learning/fine-tuning to adapt the model to new datasets (Caltech-101, Horse/Cat/Dog classification) and pretrained models.

### Frameworks: TensorFlow/Keras or PyTorch.

### Evaluation Metrics: Report Precision, Recall, F1-Score for test data in all models/phases.

### Phases:

#### Phase 1: Model Design (CIFAR-10)

Design & train a CNN (< 1 million parameters) on CIFAR-10.

Maximize accuracy (train & test sets).

Overfitting allowed in this phase only.

Dataset: CIFAR-10 (45k Train, 5k Val, 10k Test).

#### Phase 2: Prevent Overfitting (CIFAR-10)

Apply techniques (Data Augmentation + others) to the Phase 1 model to combat overfitting.

Achieve high final accuracy.

Perform hyperparameter tuning (e.g., optimizers).

Save the best model for Phase 3.

#### Phase 3: Transfer Learning

Use the saved best model from Phase 2.

Dataset A: Caltech-101 (101 classes)

Step 1: Freeze all layers, train only new last layer.

Step 2: Unfreeze one block, retrain.

Prevent overfitting, analyze results.

Dataset B: Horse/Cat/Dog (3 classes, smaller data)

Repeat steps 1 & 2 (Freeze all -> new last layer; Unfreeze one block -> retrain).

Prevent overfitting.

Pretrained Models (Fine-Tuning):

Fine-tune ResNet50, MobileNetV2, EfficientNetB0 on both Caltech-101 and Horse/Cat/Dog.

Hyperparameter tuning required.

Replace last layer. Limit trainable layers (< 10).

Prevent overfitting, achieve best accuracy.

Perform all required evaluations/visualizations.
