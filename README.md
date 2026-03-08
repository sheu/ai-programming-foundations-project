# AI Programming Foundations Project

A capstone project for Udacity's **AI Programming with Python Nanodegree**. This project applies core AI and deep-learning concepts—Python, NumPy, pandas, Matplotlib, linear algebra, and PyTorch—to build and deploy an image classifier that identifies flower species.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Nanodegree Curriculum](#nanodegree-curriculum)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Training](#training)
  - [Prediction](#prediction)
- [Technologies Used](#technologies-used)
- [License](#license)

---

## Project Overview

The capstone project trains a deep neural network on the [102 Category Flower Dataset](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html) using transfer learning with a pre-trained model (e.g., VGG, ResNet, or DenseNet from `torchvision`). The trained model is then used as a command-line application to predict the name of a flower from an input image.

Key goals:
- Load and pre-process image data for training, validation, and testing.
- Fine-tune a pre-trained convolutional neural network.
- Save and load model checkpoints.
- Perform inference on new images with top-K class probabilities.

---

## Nanodegree Curriculum

The project draws on the following modules from the nanodegree:

| Module | Topics |
|---|---|
| **Introduction to Python** | Data types, control flow, functions, OOP |
| **NumPy & pandas** | Array operations, DataFrames, data wrangling |
| **Matplotlib** | Data visualization, plotting training curves |
| **Linear Algebra** | Vectors, matrices, transformations |
| **Neural Networks** | Perceptrons, activation functions, backpropagation |
| **Deep Learning with PyTorch** | CNNs, transfer learning, model checkpointing |

---

## Project Structure

```
ai-programming-foundations-project/
├── Image Classifier Project.ipynb   # Jupyter notebook for development
├── train.py                         # Script to train the network
├── predict.py                       # Script to run inference on an image
├── model.py                         # Model architecture and helper functions
├── utils.py                         # Data loading and image processing utilities
├── cat_to_name.json                 # Mapping of category labels to flower names
└── README.md
```

---

## Prerequisites

- Python 3.7+
- [PyTorch](https://pytorch.org/) 1.0+ with torchvision
- CUDA-capable GPU (recommended for training)

---

## Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/sheu/ai-programming-foundations-project.git
   cd ai-programming-foundations-project
   ```

2. **Create and activate a virtual environment** (optional but recommended)

   ```bash
   python -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**

   ```bash
   pip install torch torchvision numpy pandas matplotlib pillow
   ```

4. **Download the dataset**

   Download the [102 Category Flower Dataset](https://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html) and organize it into `train/`, `valid/`, and `test/` subdirectories under a `flowers/` folder.

---

## Usage

### Training

Train a new model from scratch or fine-tune a pre-trained network:

```bash
python train.py flowers/ \
    --arch vgg16 \
    --learning_rate 0.001 \
    --hidden_units 512 \
    --epochs 10 \
    --gpu
```

**Arguments**

| Argument | Default | Description |
|---|---|---|
| `data_dir` | (required) | Path to dataset directory |
| `--save_dir` | `.` | Directory to save the checkpoint |
| `--arch` | `vgg16` | Pre-trained model architecture |
| `--learning_rate` | `0.001` | Optimizer learning rate |
| `--hidden_units` | `512` | Units in the hidden layer |
| `--epochs` | `20` | Number of training epochs |
| `--gpu` | `False` | Use GPU for training |

### Prediction

Predict the flower category of a single image:

```bash
python predict.py /path/to/image checkpoint.pth \
    --top_k 5 \
    --category_names cat_to_name.json \
    --gpu
```

**Arguments**

| Argument | Default | Description |
|---|---|---|
| `input` | (required) | Path to input image |
| `checkpoint` | (required) | Path to saved model checkpoint |
| `--top_k` | `1` | Return top K most-likely classes |
| `--category_names` | `cat_to_name.json` | JSON file mapping categories to names |
| `--gpu` | `False` | Use GPU for inference |

---

## Technologies Used

- **Python 3** – core programming language
- **PyTorch & torchvision** – deep learning framework and pre-trained models
- **NumPy** – numerical computing
- **pandas** – data manipulation
- **Matplotlib** – visualization
- **Pillow (PIL)** – image loading and transformation
- **Jupyter Notebook** – interactive development environment

---

## License

This project is submitted as part of the Udacity AI Programming with Python Nanodegree. Code and assets follow the [Udacity Honor Code](https://udacity.com/legal/community-guidelines).
