## ISP-AD Anomaly Segmentation with DeepLabV3

This project applies semantic segmentation to detect surface defects in industrial screen printing using the ISP-AD dataset. The aim is to localize defects at the pixel level rather than just classifying images as good/bad.

## Dataset

We used the Industrial Screen Printing Anomaly Detection (ISP-AD) dataset, which provides both synthetic and real defect data:

~312k fault-free samples

~246k defective samples (mostly synthetic, plus 711 real factory defects)

Images are available in 256×256 and 512×512 patches

Formats include .png and .hdf5

For this project, training was done on synthetic ASM patches (256×256), and evaluation included real defect masks.

Citation:

Krassnig, P. J., Haselmann, M., Kremnitzer, M., & Gruber, D. P. (2025).
The Industrial Screen Printing Anomaly Detection Dataset (ISP-AD). Zenodo.
https://doi.org/10.5281/zenodo.14911043


## Model

Architecture: DeepLabV3 with a ResNet backbone

Framework: PyTorch / Torchvision

Classes:

0 = normal surface

1 = defect

Loss and metrics:

CrossEntropyLoss (with option to use Focal Loss for imbalance)

IoU (Intersection over Union)

Dice coefficient

## Training Setup

Platform: Kaggle Notebook

GPU: NVIDIA T4 (CUDA enabled)

Train/Val/Test split:

180k synthetic samples for training

20k synthetic samples for validation

1916 real images (good + defect) for testing

Batch size: 16

Optimizer: Adam (lr = 1e-4)

Checkpoints saved after each epoch

## Notes

The ISP-AD dataset is large; initial training was done on subsets for faster turnaround.

For better results, train on the full set and/or use more epochs.

Future work: lighter models like UNet or DeepLabV3-ResNet50 for faster experimentation.

## Author

Shivani Sharma
Project built and tested on Kaggle GPU environment.
