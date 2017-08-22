# Experiment

I measured computation time for **one** image inference (`batch size = 1`). Larger batch sizes are somewhat out of concern since I am targeting real-time applications (inference on-the-fly).

I reported `flops` and `parameter sizes` as well as `timing`. Still, I am not sure why some networks run faster even when they have larger FLOPS and PARAMS. (E.g, see `VGG16` and `INCEPTION-V3` for classification.) **Please let me know if you know the answer**.

You will see the results of `VGG16` and `INCEPTION-V3` for ImageNet classification, and `VGG16-based SSD`, `Inception-V3-based SSD`, and `Inception-V1-based SSD` for object detection.

The `timing`s below are measured by averaging 1000 trials, excluding two extremes (min and max). I also provide timeline profiles as `.json` files, which trace each operational duration. To check them, launch `Chrome`, type `chrome:\\tracing`, and load each json file.


# System

Ubuntu 16.04 with Titan X. Tensorflow 1.2

# Classification networks 

Imagenet classification (input 1x224x224x3. output 1000 classes.)

### VGG16

| | | |
| ------------- |-------------| -----|
| timing | 8 ms | Check `vgg16_8ms.json` |
| flops | 36.01b flops | [See flops detail](vgg16_flops_detail.md) |
| parameters | 138.36m params |   [See params detail](vgg16_params_detail.md) |

### INCEPTION-V3

| | | |
| ------------- |-------------| -----|
| timing | 10 ms | Check `inception3_10ms.json` |
| flops | 6.92b flops | [See flops detail](incep3_flops_detail.md) |
| parameters | 25.57m params |   [See params detail](incep3_params_detail.md) |

# Object detection networks 

I implemented [Single-Shot Detection](https://arxiv.org/abs/1512.02325) from various base networks. All versions have similar multi-box configurations (6 multi-box layers).

### VGG16-based SSD

| | | |
| ------------- |-------------| -----|
| timing | ms | Check .json |
| flops |  flops | [See flops detail](.md) |
| parameters |  params |   [See params detail](.md) |

### Inception-V3-based SSD

| | | |
| ------------- |-------------| -----|
| timing |  ms | Check .json |
| flops | flops | [See flops detail](.md) |
| parameters | params |   [See params detail](.md) |

### Inception-V1-based SSD

| | | |
| ------------- |-------------| -----|
| timing |  ms | Check .json |
| flops |  flops | [See flops detail](.md) |
| parameters |  params |   [See params detail](.md) |

