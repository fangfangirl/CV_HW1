# NYCU Computer Vision 2026 HW1

* **Student ID:** 314511037
* **Name:** 張周芳

## Introduction
This project implements image classification for HW1. It implements a student-teacher knowledge distillation approach for image classification. 
The student model learns from both hard labels and soft predictions of the teacher model to improve performance. 
The project includes training notebooks for both the teacher and student models, and an evaluation abd inference notebooks to predict on test data.

## Dataset
Place the dataset folder under `HW1/dataset/` with the following structure:
```
CV_HW1/dataset/
├─ teacher_model.pth # The teacher to train the student
├─ student_model.pth # The final model weight (result)
├─ requirements.txt # 這個是如果是在自己的環境中執行需要的
└─ data/ # 訓練資料
    ├─ train/
    ├─ val/
    └─ test/
```
## Environment Setup

- Python 3.10+
- GPU recommended (CUDA supported)

This project was developed and tested on Google Colab and Kaggle, where most required packages are pre-installed.  
If you are running this project on your local machine, please follow the steps below.

### Step1: Using Conda (Recommended do)

```bash
# Create a conda environment
conda create -n cv-hw1 python=3.10 -y

# Activate environment
conda activate cv-hw1
```
### Step2: Install PyTorch

Please install PyTorch based on your system configuration:

1. Visit: [https://pytorch.org/get-started/locally/](https://pytorch.org/get-started/locally/)
2. Select your OS, package (pip), and CUDA version
3. Run the generated command

Example (CUDA 12.6):
```bash
pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu126
```
### Step3: Install Other Dependencies
```bash
pip install -r requirements.txt
```
