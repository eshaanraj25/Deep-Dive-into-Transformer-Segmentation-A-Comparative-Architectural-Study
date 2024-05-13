# U-Net Model Overview

The U-Net architecture utilizes an encoder-decoder structure to effectively combine convolutional, max-pooling, and transposed convolutional layers. This structure is designed to capture context, reduce spatial dimensions, and achieve precise localization. The integration of skip connections preserves essential spatial details for accurate segmentation masks.

## Input Specifications

- *Resolution:* Images are resized to 128x128 pixels.
- *Channels:* 3 (RGB).
- *Normalization:* Pixel values normalized to a [0, 1] scale.

## Hyperparameter Tuning

Achieving optimal performance through detailed hyperparameter tuning:

- *Batch Size:* Optimal size determined at 32 (after testing 32, 64, 128).
- *Dropout Rate:* Set at 0.3 to balance regularization with training efficiency, after testing rates between 0.1 and 0.5.
- *Number of Filters:* Begins at 32, doubling in each encoder layer to enhance feature processing capabilities.
- *Epochs:* Limited to 20 to maximize efficiency and prevent overfitting, after testing 20, 50, and 100 epochs.

## Loss and Accuracy Curves for UNet_Baseline


![U-Net Architecture](UNet/Images/Baseline_Loss.png)

## Results for UNet_Baseline

