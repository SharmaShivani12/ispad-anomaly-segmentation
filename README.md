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
