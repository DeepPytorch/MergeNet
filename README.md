# MergeNet
MergeNet is a type of InceptionResnet that I have created with 7 variants: Nano, Micro, Mini, Small, Standard, Large, and Mega. MergeNet's architecture makes it extremely robust to overfitting.

# Architecture
MergeNet uses Inception layers along with a skip connection per block, similar to Inception, Inception-ResNet, and ResNeXt, exept: 
- Without the branch scaling on each layer
- Without the preliminary classifiers to increase accuracy (Inception)
- It has PReLu to increase accuracy
- AdamW
- A lower Weight Decay Value
- Different Depths per branch rather than 1x1 then starting at 3x3 and increasing (Inception)
- Less prone to overfitting due to constant Batch Normalization and Smaller size

The smallest version, nano, crushes ResNeXt and Ineception-ResNet on EMNIST Digits while having between 117x and 260x less parameters, depending on the version/size. Even though this test on the accuracy in unfair to the Inception-ResNet type models becuase of the large size and small dataset, and the diffrences in which dataset it is optimized for, however based of off the modern additions such as PReLu and AdamW, and the still high relitive accuracy difference I can conclude that it would be able to outpreform these models, specificly the Small and higher models.

Due to the weak compute power and specifications of my computer, I was unable to download the ImageNet dataset, and was unable to let it run because I cannot use Cuda or ROCm, So I was only able to run Nano Completely, and I had to use EMNIST Digits, rather than ImageNet 1K. All models other than Nano have EMNIST Digits in it as a Placeholder for orginazation, however the model is for Imagenet 1K. So that is why it will raise a runtime error.

| Name | # Layers | Parameter Count | Peak Accuracy |
|---|---|---|---|
| Nano | 34 | 214,314 | 99.7975% |
| Micro | | | n/a |
| Mini | | | n/a |
| Small | | | n/a |
| Standard | | | n/a |
| Large | | | n/a |
| Mega | | | n/a |
