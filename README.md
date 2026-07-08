# MergeNet
MergeNet is a type of InceptionResnet that I have created with 7 variants: Nano, Micro, Mini, Small, Standard, Large, and Mega. \

# Architecture
MergeNet uses Inception layers along with a skip connection per block, similar to Inception, Inception-ResNet, and ResNeXt, exept: 
- Without the branch scaling on each layer
- Without the preliminary classifiers to increase accuracy (Inception)
- It has PReLu to increase accuracy
- AdamW
- A lower Weight Decay Value
- Different Depths per branch rather than 1x1 then starting at 3x3 and increasing (Inception)
- Less prone to overfitting due to constant Batch Normalization and Smaller size while the smallest version, nano, crushes ResNeXt and Ineception-ResNet while having between 117x and 260x smaller, depending on the version/size.

Due to the weak compute power and specifications of my computer, I was unable to download the ImageNet dataset, and was unable to let it run because I cannot use Cuda or ROCm, So I was only able to run Nano Completely, and I had to use EMNIST Digits.

| Name | # Layers| Parameter Count | Peak Accuracy |
| -------- | -------- | -------- |
| Nano | 34 | 214,314 |  |
| Micro |  |  | n/a |
| Mini |  |  | n/a |
| Standard |  |  | n/a |
| Large |  |  | n/a |
| Mega |  |  | n/a |
