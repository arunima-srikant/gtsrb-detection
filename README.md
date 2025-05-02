# Traffic Sign Detection and Recognition

This repository contains the code and resources for our course project on traffic sign detection and classification. We use **YOLOv8** for object detection and a variety of **custom CNN models** for classification, with experiments conducted on both the GTSRB dataset and a custom stock dataset of traffic signs.

---

## Repository Contents

* `cnn_models.py`: Contains all CNN architectures trained and tested on GTSRB and stock images.
* `pretrained_with_yolo.py`: Recommended detector-recognition pipeline, uses YOLOv8 + pretrained CNN.
* `four_conv+yolo.py`: Final custom built detector-recognition pipeline using YOLOv8 + 4-layer CNN, includes brightness enhancement.
* `weights/`: Folder containing `.pth` and `.pt` weight files for CNNs and YOLOv8.
* `Stock Images/`: Custom traffic sign images used for validation on real-world samples.

---

## Getting Started

### 1. Running CNN Models

1. Clone this repository and open in Google Colab.
2. GTSRB dataset loads automatically via `torchvision.datasets`.
3. To use saved model weights:

   * Ensure paths to `.pth` files are correctly set.
   * Skip this step if you'd like to train the model from scratch.
4. To test on stock images:

   * Use the correct path to the `Stock Images/` folder in this repo.

### 2. Running YOLOv8 + CNN Pipeline

1. Upload the YOLOv8 detector weights (`best.pt`) to Colab.
2. Upload the CNN weights corresponding to the model you're using:

   * `gtsrb_4conv.pth` for YOLO+4conv
   * `gtsrb_vgg_model.pth` for YOLO+VGG
   * *No upload needed* for YOLO+Pretrained
3. Choose to either:

   * Run the code section by section, or
   * Run the entire pipeline using the consolidated code blocks.
4. For testing:

   * Option A: Upload an image when prompted.
   * Option B: Use a GTSRB image by modifying the path in the code.

---

##  Notes

* If model accuracy differs from what's reported in the project report, the `.pth` file may be corrupted — retraining is recommended.
* For best results, use the **YOLOv8 + Pretrained CNN** configuration.
* All datasets, models, and test images are included in this repository. No external downloads required.

---

## Goal

To design a robust traffic sign detection and classification pipeline capable of generalizing across real-world conditions using both classic CNNs and modern object detection methods.

---

## Acknowledgements
This project was completed as part of an academic course project.

Project Partner: Ananya Chenny Rahul

Pretrained Model Reference:
Portions of the pretrained CNN model were adapted from the repository:
[https://github.com/Aravindlivewire/CNN-for-traffic-sign-recognition](https://github.com/poojahira/gtsrb-pytorch)

Special thanks to the authors of the GTSRB dataset and the creators of YOLOv8 for enabling powerful computer vision experimentation.
