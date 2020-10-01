# nuclei-segmentation-unet
Nuclei segmentaion using UNET and some experiments

Implemented UNET https://arxiv.org/abs/1505.04597 with a few changes:
* Input has 3 channels (RGB) instead of a grayscale image
* Used transposed cpnvolutions for Upsampling
* Instead of cropping out a portion from the decoder part and concatening it in encoder part, the whole portion is so calculated to ensure the feature maps are not cropped out, rather concatenated wholly. The input image size had been adjusted accordingly. This should decrease potential loss of info due to cropping.
* Last layer is a conv2d
