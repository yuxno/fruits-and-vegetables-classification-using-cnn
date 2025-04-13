# 🥦 Fruits & Vegetables Classifier using Transfer Learning (PyTorch)

This project is a deep learning model that classifies images of 14 different fruits and vegetables using a pre-trained CNN (VGG16). It was created as part of a step-by-step educational workshop to demonstrate image classification, transfer learning, data loading, and fine-tuning in PyTorch.

## 🧠 Classes
- Artichoke
- Beet
- Carrot
- Cucumber
- Egg Plant
- HotPeeper
- Lemon
- Onion
- Oranges
- Pepper
- Potato
- Squach
- Tomato
- Turnip

## 🚀 Features
- Custom PyTorch `Dataset` class for loading images
- Data augmentation for training using `torchvision.transforms`
- Uses **VGG16** pre-trained on ImageNet for feature extraction
- Fine-tunes only selected layers of the model for faster, more efficient training
- Supports training and validation phases
- Visualizes preprocessed input and transformed outputs

## 🧾 Steps
1. **Prepare Dataset**  
   - Images are organized in folders by class names.
   - Split into training and validation sets.

2. **Custom Dataset & Dataloader**  
   - Built using `FruitsDataset` class and `torch.utils.data.DataLoader`.

3. **Image Preprocessing**  
   - Resize, color convert, data augment (for training), normalize.

4. **Model Setup**  
   - Load VGG16 from `torchvision.models`
   - Replace final layer to classify 14 classes
   - Selective fine-tuning (only certain layers are trained)

5. **Training & Validation**  
   - Uses `CrossEntropyLoss`
   - Optimizer is SGD with different learning rates for different layers

6. **Testing a Single Image**  
   - Load and visualize original and preprocessed image
   - Predict the class using the trained model

## 🔧 Requirements
- Python 3.7+
- PyTorch
- torchvision
- PIL
- matplotlib
- numpy

You can install requirements using:

```bash
pip install torch torchvision matplotlib pillow
