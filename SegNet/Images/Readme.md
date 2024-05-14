# SegNet Implementation

We implemented a modified version of SegNet, tailored for image segmentation tasks. This model follows an encoder-decoder architecture with down-sampling and up-sampling stages.

## Model Architecture

- *Input*: The model takes an input image of size 128x128 pixels. The input image undergoes batch normalization to ensure consistent scaling and distribution of pixel values across different images in the batch.

- *Encoder (Downsampling)*: The normalized image passes through a series of downsampling blocks. Each downsampling block consists of convolutional layers followed by batch normalization and ReLU activation functions. Max pooling operations are applied after each convolutional block to reduce the spatial dimensions of the feature maps while increasing their depth. The indices and shapes obtained from max pooling operations are stored for later use in the decoder.

- *Decoder (Upsampling)*: After the encoding stage, the encoded feature maps are passed through a series of upsampling blocks in the decoder part of the network. The feature maps obtained from the upsampling blocks are further processed through convolutional layers, batch normalization, and ReLU activation functions.

- *Output*: The final output of the model is a segmentation map, where each pixel in the input image is classified into different categories based on the learned features. This segmentation map represents the model's prediction of the semantic segmentation of the input image.

## Implementation Details

- *Normalization*: Batch normalization is applied to ensure consistent scaling and distribution of pixel values.
- *Convolutional Blocks*: Each downsampling and upsampling block consists of convolutional layers, followed by batch normalization and ReLU activation functions.
- *Pooling*: Max pooling operations are applied after each convolutional block during downsampling to reduce spatial dimensions.
- *Storage of Indices*: Indices and shapes obtained from max pooling operations are stored for later use in upsampling.
- *Training*: The model is trained on labeled data to learn to accurately classify each pixel in the input image into different categories.



