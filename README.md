# Experiment

I measured computation time for **one** image inference (`batch size = 1`). Larger batch sizes are less out of concern since I am targeting real-time applications (inference on-the-fly).

I tried to also report `flops` and `parameter sizes`. Still, I am not sure why some networks run faster even when they have larger FLOPS and PARAMS. (E.g, see `VGG16` and `INCEPTION-V3` for classification.) **Please let me know if you know the answer**.

The computation durations below are measured by averaging 1000 trials, with excluding two extremes (min and max). You can see also timeline profiling which shows each operational duration. The are `.json` files, and you can check them using `Chrome`. Type `chrome:\\tracing` and load each json file.


# System

Ubuntu 16.04 with Titan X. Tensorflow 1.2

# Classification networks 

Imagenet classification (input 1x224x224x3. output 1000 classes.)

### VGG16

| ------------- |:-------------:| -----:|
| flops      | centered      |   $12 |
| parameters | are neat      |    $1 |

#### timing: 8 ms

#### flops: 36.01b flops
[See flops detail](vgg16_flops_detail.md)

#### parameters: 138.36m params
[See params detail](vgg16_params_detail.md)

### INCEPTION-V3

#### timing: 10 ms

#### flops: 6.92b flops
[See flops detail](incep1_flops_detail.md)

#### parameters: 25.57m params
[See params detail](incep1_params_detail.md)

# Object detection networks 

I implemented Single-Shot Detection from various base networks (input 1x270x480x3). All have similar multi-box configurations (6 multi-box layers).

### VGG16-based SSD

#### timing:  ms

#### flops:  flops
[See flops detail]()

#### parameters:  params
[See params detail]()

### Inception-V3-based SSD

#### timing:  ms

#### flops:  flops
[See flops detail]()

#### parameters:  params
[See params detail]()


### Inception-V1-based SSD

#### timing:  ms

#### flops:  flops
[See flops detail]()

#### parameters:  params
[See params detail]()

