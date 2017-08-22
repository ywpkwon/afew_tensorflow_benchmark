# Experiment

I measured computation time for **one** image inference (`batch size = 1`). Larger batch sizes are somewhat out of concern since I am targeting real-time applications (inference on-the-fly).

I reported `flops` and `parameter sizes` as well as `timing`. Still, I am not sure why some networks run faster even when they have larger FLOPS and PARAMS. (E.g, see `VGG16` and `InceptionV3` for classification.) **Please let me know if you know the answer**.

You will see the results of `VGG16` and `InceptionV3` for ImageNet classification, and `VGG16-based SSD`, `InceptionV3-based SSD`, and `InceptionV1-based SSD` for object detection.

The `timing`s below are measured by averaging 1000 trials, excluding two extremes (min and max). I also provide timeline profiles as `.json` files, which trace each operational duration. To check them, launch `Chrome`, type `chrome:\\tracing`, and load each json file.


# System

| System | OS | GPU | CPU | Tensorflow ver. |
| ------------- | ------- | ------ | ----- | ---- |
| A | Ubuntu 16.04 | Titan X | | 1.2 |
| B | Ubuntu 16.04 | GeForce GTX 1080 8Gb | | 1.2 |

# Classification networks 

Imagenet classification (input 1x224x224x3. output 1000 classes.)

### VGG16

| | | |
| ------------- |-------------| -----|
| timing @ A | 8 ms | Check `A_cls_vgg16/A_cls_vgg16.json` |
| timing @ B | 10.4 ms | Check `B_cls_vgg16/B_cls_vgg16.json` |
| flops | 36.01b flops | [See flops detail](vgg16_flops_detail.md) |
| parameters | 138.36m params |   [See params detail](vgg16_params_detail.md) |


### InceptionV3

| | | |
| ------------- |-------------| -----|
| timing @ A | 10 ms | Check `A_cls_incep3/A_cls_incep3.json` |
| timing @ B | 7.5 ms | Check `B_cls_incep3/B_cls_incep3.json` |
| flops | 6.92b flops | [See flops detail](incep3_flops_detail.md) |
| parameters | 25.57m params |   [See params detail](incep3_params_detail.md) |


# Object detection networks 

I implemented [Single-Shot Detection](https://arxiv.org/abs/1512.02325) from various base networks. All versions have similar multi-box configurations (6 multi-box layers).

### VGG16-based SSD

| | | |
| ------------- |-------------| -----|
| timing @ A | ms | Check `A_ssd_incep3/A_ssd_incep3.json` |
| timing @ B | 21 ms | Check `B_ssd_vgg16/B_ssd_vgg16.json` |
| flops | 87.21b flops | [See flops detail](ssd_vgg16_flops_detail.md) |
| parameters | 24.01m params | [See params detail](ssd_vgg16_params_detail.md) |

### InceptionV3-based SSD

| | | |
| ------------- |-------------| -----|
| timing @ A |  ms | Check `A_ssd_incep3/A_ssd_incep3.json` |
| timing @ B | 16.2 ms | Check `B_ssd_incep3/B_ssd_incep3.json` |
| flops | 17.21b flops | [See flops detail](ssd_incep3_flops_detail.md) |
| parameters | 45.12m params |   [See params detail](ssd_incep3_params_detail.md) |

### InceptionV1-based SSD

| | | |
| ------------- |-------------| -----|
| timing @ A |  ms | Check `A_ssd_incep3/A_ssd_incep3.json` |
| timing @ B | 12.0 ms | Check `B_ssd_incep1/B_ssd_incep1.json` |
| flops | 12.83b flops | [See flops detail](ssd_incep1_flops_detail.md) |
| parameters | 19.52m params |   [See params detail](ssd_incep1_params_detail.md) |

