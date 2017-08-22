# Experiment

We target computation time for 1 image inference (`batch size` = 1).

# System

Ubuntu 16.04 with Titan X. Tensorflow 1.2

# Classification networks 

## VGG16. PASCAL VOC classification (input 224x224x3. output 21)

#### timing: 8 ms

### flops
    _TFProfRoot (0/36.01b flops)
      vgg_16/conv1/conv1_2/convolution (4.39b/4.39b flops)
      vgg_16/conv2/conv2_2/convolution (4.39b/4.39b flops)
      vgg_16/conv3/conv3_2/convolution (4.39b/4.39b flops)
      vgg_16/conv3/conv3_3/convolution (4.39b/4.39b flops)
      vgg_16/conv4/conv4_3/convolution (4.25b/4.25b flops)
      vgg_16/conv4/conv4_2/convolution (4.25b/4.25b flops)
      vgg_16/conv2/conv2_1/convolution (2.19b/2.19b flops)
      vgg_16/conv3/conv3_1/convolution (2.19b/2.19b flops)
      vgg_16/conv4/conv4_1/convolution (2.12b/2.12b flops)
      vgg_16/conv5/conv5_3/convolution (1.06b/1.06b flops)
      vgg_16/conv5/conv5_2/convolution (1.06b/1.06b flops)
      vgg_16/conv5/conv5_1/convolution (1.06b/1.06b flops)
      vgg_16/fc6/convolution (205.52m/205.52m flops)
      vgg_16/fc7/convolution (33.55m/33.55m flops)
      vgg_16/fc8/convolution (8.19m/8.19m flops)
      vgg_16/conv1/conv1_2/BiasAdd (3.81m/3.81m flops)
      vgg_16/conv1/conv1_1/BiasAdd (3.81m/3.81m flops)
      vgg_16/conv2/conv2_2/BiasAdd (1.91m/1.91m flops)
      vgg_16/conv2/conv2_1/BiasAdd (1.91m/1.91m flops)
      vgg_16/conv3/conv3_3/BiasAdd (952.58k/952.58k flops)
      vgg_16/conv3/conv3_2/BiasAdd (952.58k/952.58k flops)
      vgg_16/conv3/conv3_1/BiasAdd (952.58k/952.58k flops)
      vgg_16/conv4/conv4_2/BiasAdd (460.80k/460.80k flops)
      vgg_16/conv4/conv4_3/BiasAdd (460.80k/460.80k flops)
      vgg_16/conv4/conv4_1/BiasAdd (460.80k/460.80k flops)
      vgg_16/conv5/conv5_1/BiasAdd (115.20k/115.20k flops)
      vgg_16/conv5/conv5_2/BiasAdd (115.20k/115.20k flops)
      vgg_16/conv5/conv5_3/BiasAdd (115.20k/115.20k flops)
      vgg_16/fc6/BiasAdd (4.10k/4.10k flops)
      vgg_16/fc7/BiasAdd (4.10k/4.10k flops)
      vgg_16/fc8/BiasAdd (1.00k/1.00k flops)

### parameters
    _TFProfRoot (--/138.36m params)
      vgg_16/conv1/conv1_1/biases (64, 64/64 params)
      vgg_16/conv1/conv1_1/weights (3x3x3x64, 1.73k/1.73k params)
      vgg_16/conv1/conv1_2/biases (64, 64/64 params)
      vgg_16/conv1/conv1_2/weights (3x3x64x64, 36.86k/36.86k params)
      vgg_16/conv2/conv2_1/biases (128, 128/128 params)
      vgg_16/conv2/conv2_1/weights (3x3x64x128, 73.73k/73.73k params)
      vgg_16/conv2/conv2_2/biases (128, 128/128 params)
      vgg_16/conv2/conv2_2/weights (3x3x128x128, 147.46k/147.46k params)
      vgg_16/conv3/conv3_1/biases (256, 256/256 params)
      vgg_16/conv3/conv3_1/weights (3x3x128x256, 294.91k/294.91k params)
      vgg_16/conv3/conv3_2/biases (256, 256/256 params)
      vgg_16/conv3/conv3_2/weights (3x3x256x256, 589.82k/589.82k params)
      vgg_16/conv3/conv3_3/biases (256, 256/256 params)
      vgg_16/conv3/conv3_3/weights (3x3x256x256, 589.82k/589.82k params)
      vgg_16/conv4/conv4_1/biases (512, 512/512 params)
      vgg_16/conv4/conv4_1/weights (3x3x256x512, 1.18m/1.18m params)
      vgg_16/conv4/conv4_2/biases (512, 512/512 params)
      vgg_16/conv4/conv4_2/weights (3x3x512x512, 2.36m/2.36m params)
      vgg_16/conv4/conv4_3/biases (512, 512/512 params)
      vgg_16/conv4/conv4_3/weights (3x3x512x512, 2.36m/2.36m params)
      vgg_16/conv5/conv5_1/biases (512, 512/512 params)
      vgg_16/conv5/conv5_1/weights (3x3x512x512, 2.36m/2.36m params)
      vgg_16/conv5/conv5_2/biases (512, 512/512 params)
      vgg_16/conv5/conv5_2/weights (3x3x512x512, 2.36m/2.36m params)
      vgg_16/conv5/conv5_3/biases (512, 512/512 params)
      vgg_16/conv5/conv5_3/weights (3x3x512x512, 2.36m/2.36m params)
      vgg_16/fc6/biases (4096, 4.10k/4.10k params)
      vgg_16/fc6/weights (7x7x512x4096, 102.76m/102.76m params)
      vgg_16/fc7/biases (4096, 4.10k/4.10k params)
      vgg_16/fc7/weights (1x1x4096x4096, 16.78m/16.78m params)
      vgg_16/fc8/biases (1000, 1.00k/1.00k params)
      vgg_16/fc8/weights (1x1x4096x1000, 4.10m/4.10m params)


## INCEPTION-V3. PASCAL VOC classification (input 224x224x3. output 21)

### timing
10 ms

### flops
    _TFProfRoot (0/6.92b flops)
      InceptionV3/InceptionV3/Conv2d_4a_3x3/convolution (898.28m/898.28m flops)
      InceptionV3/InceptionV3/Conv2d_2b_3x3/convolution (522.03m/522.03m flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_0/Conv2d_1a_1x1/convolution (336.42m/336.42m flops)
      InceptionV3/InceptionV3/Conv2d_2a_3x3/convolution (261.02m/261.02m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0c_3x3/convolution (130.06m/130.06m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0c_3x3/convolution (130.06m/130.06m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0c_3x3/convolution (130.06m/130.06m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_1/Conv2d_0b_5x5/convolution (120.42m/120.42m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_1/Conv2d_0b_5x5/convolution (120.42m/120.42m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_1/Conv_1_0c_5x5/convolution (120.42m/120.42m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0b_3x3/convolution (111.48m/111.48m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0b_3x3/convolution (111.48m/111.48m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0c_1x7/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0b_1x7/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0b_7x1/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0c_7x1/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0c_7x1/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0b_1x7/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0d_7x1/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0e_1x7/convolution (87.22m/87.22m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0b_3x3/convolution (86.70m/86.70m flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_0b_3x3/convolution (86.70m/86.70m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0b_3x3/convolution (86.70m/86.70m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0b_3x3/convolution (86.70m/86.70m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0e_1x7/convolution (72.68m/72.68m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0c_7x1/convolution (72.68m/72.68m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0e_1x7/convolution (72.68m/72.68m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0c_7x1/convolution (72.68m/72.68m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0a_1x1/convolution (66.06m/66.06m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0d_7x1/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0c_1x7/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0d_7x1/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0c_1x7/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0b_7x1/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0b_1x7/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0b_7x1/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0b_1x7/convolution (60.57m/60.57m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0c_7x1/convolution (58.15m/58.15m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0e_1x7/convolution (58.15m/58.15m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0a_1x1/convolution (56.62m/56.62m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_0/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_0/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_3/Conv2d_0b_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_0/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_0/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_0/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_3/Conv2d_0b_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_3/Conv2d_0b_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_3/Conv2d_0b_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0a_1x1/convolution (49.84m/49.84m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_0/Conv2d_0a_1x1/convolution (47.19m/47.19m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0a_1x1/convolution (41.53m/41.53m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0a_1x1/convolution (41.53m/41.53m flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0a_1x1/convolution (41.53m/41.53m flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0a_1x1/convolution (41.53m/41.53m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0a_1x1/convolution (41.29m/41.29m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_0/Conv2d_1a_3x3/convolution (39.81m/39.81m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0c_1x7/convolution (38.76m/38.76m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0d_7x1/convolution (38.76m/38.76m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0b_7x1/convolution (38.76m/38.76m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0b_1x7/convolution (38.76m/38.76m flops)
      InceptionV3/InceptionV3/Conv2d_3b_1x1/convolution (35.65m/35.65m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0a_1x1/convolution (35.39m/35.39m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0a_1x1/convolution (33.23m/33.23m flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0a_1x1/convolution (33.23m/33.23m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0d_3x1/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0d_3x1/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0c_1x3/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0c_3x1/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0b_1x3/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0c_1x3/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_1x3/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_3x1/convolution (31.85m/31.85m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_0/Conv2d_0a_1x1/convolution (29.49m/29.49m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_0/Conv2d_0a_1x1/convolution (28.90m/28.90m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_3/Conv2d_0b_1x1/convolution (28.90m/28.90m flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_0a_1x1/convolution (28.90m/28.90m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0a_1x1/convolution (28.90m/28.90m flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_3/Conv2d_0b_1x1/convolution (28.31m/28.31m flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_1a_1x1/convolution (28.04m/28.04m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_3/Conv2d_0b_1x1/convolution (25.69m/25.69m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0a_1x1/convolution (25.69m/25.69m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_0/Conv2d_0a_1x1/convolution (25.69m/25.69m flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_1a_3x3/convolution (23.89m/23.89m flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_1/Conv2d_0a_1x1/convolution (21.68m/21.68m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0a_1x1/convolution (19.27m/19.27m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_0/Conv2d_0a_1x1/convolution (19.27m/19.27m flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_1/Conv2d_0b_1x1/convolution (19.27m/19.27m flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_3/Conv2d_0b_1x1/convolution (17.69m/17.69m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_1/Conv2d_0a_1x1/convolution (14.45m/14.45m flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_3/Conv2d_0b_1x1/convolution (9.63m/9.63m flops)
      InceptionV3/Logits/Conv2d_1c_1x1/convolution (4.10m/4.10m flops)
      InceptionV3/InceptionV3/Conv2d_2b_3x3/BiasAdd (906.30k/906.30k flops)
      InceptionV3/InceptionV3/Conv2d_4a_3x3/BiasAdd (623.81k/623.81k flops)
      InceptionV3/InceptionV3/Conv2d_1a_3x3/BiasAdd (468.51k/468.51k flops)
      InceptionV3/InceptionV3/Conv2d_2a_3x3/BiasAdd (453.15k/453.15k flops)
      InceptionV3/InceptionV3/Conv2d_3b_1x1/BiasAdd (278.48k/278.48k flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_0b_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0c_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0b_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0c_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0c_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0b_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0b_3x3/BiasAdd (75.26k/75.26k flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_0/Conv2d_1a_1x1/BiasAdd (64.90k/64.90k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_0/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_3/Conv2d_0b_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_1/Conv2d_0b_5x5/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_2/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_3/Conv2d_0b_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_2/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_0/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_1/Conv_1_0c_5x5/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_0/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_2/Conv2d_0a_1x1/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_1/Conv2d_0b_5x5/BiasAdd (50.18k/50.18k flops)
      InceptionV3/InceptionV3/Mixed_5d/Branch_1/Conv2d_0a_1x1/BiasAdd (37.63k/37.63k flops)
      InceptionV3/InceptionV3/Mixed_5c/Branch_1/Conv2d_0b_1x1/BiasAdd (37.63k/37.63k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_1/Conv2d_0a_1x1/BiasAdd (37.63k/37.63k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0c_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0e_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0d_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0e_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_3/Conv2d_0b_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_0/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0b_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_0c_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0b_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_3/Conv2d_0b_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_0/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0c_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0c_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_0/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_3/Conv2d_0b_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0e_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0e_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_3/Conv2d_0b_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_0/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_2/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0c_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0b_1x7/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_0/Conv2d_0a_1x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6e/Branch_1/Conv2d_0c_7x1/BiasAdd (32.45k/32.45k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0b_7x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0b_1x7/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_1/Conv2d_0a_1x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0b_1x7/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0a_1x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_1/Conv2d_0a_1x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0a_1x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0d_7x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0c_1x7/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0c_1x7/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6d/Branch_2/Conv2d_0d_7x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_6c/Branch_2/Conv2d_0b_7x1/BiasAdd (27.04k/27.04k flops)
      InceptionV3/InceptionV3/Mixed_5b/Branch_3/Conv2d_0b_1x1/BiasAdd (25.09k/25.09k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0a_1x1/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0b_7x1/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0c_1x7/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_2/Conv2d_0d_7x1/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0a_1x1/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6b/Branch_1/Conv2d_0b_1x7/BiasAdd (21.63k/21.63k flops)
      InceptionV3/InceptionV3/Mixed_6a/Branch_1/Conv2d_1a_1x1/BiasAdd (16.22k/16.22k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0a_1x1/BiasAdd (16.13k/16.13k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0a_1x1/BiasAdd (16.13k/16.13k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0b_3x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0d_3x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0d_3x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_2/Conv2d_0c_1x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0c_3x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0b_1x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_1/Conv2d_0a_1x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0c_1x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_2/Conv2d_0b_3x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_3x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_1x3/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_1/Conv2d_0a_1x1/BiasAdd (13.82k/13.82k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_0/Conv2d_0a_1x1/BiasAdd (11.52k/11.52k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_0/Conv2d_0a_1x1/BiasAdd (11.52k/11.52k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_0/Conv2d_1a_3x3/BiasAdd (11.52k/11.52k flops)
      InceptionV3/InceptionV3/Mixed_7b/Branch_3/Conv2d_0b_1x1/BiasAdd (6.91k/6.91k flops)
      InceptionV3/InceptionV3/Mixed_7c/Branch_3/Conv2d_0b_1x1/BiasAdd (6.91k/6.91k flops)
      InceptionV3/InceptionV3/Mixed_7a/Branch_1/Conv2d_1a_3x3/BiasAdd (6.91k/6.91k flops)
      InceptionV3/Logits/Conv2d_1c_1x1/BiasAdd (1.00k/1.00k flops)


### parameters
    _TFProfRoot (--/25.57m params)
      InceptionV3/AuxLogits/Conv2d_1b_1x1/biases (128, 128/128 params)
      InceptionV3/AuxLogits/Conv2d_1b_1x1/weights (1x1x768x128, 98.30k/98.30k params)
      InceptionV3/AuxLogits/Conv2d_2a_3x3/biases (768, 768/768 params)
      InceptionV3/AuxLogits/Conv2d_2a_3x3/weights (3x3x128x768, 884.74k/884.74k params)
      InceptionV3/AuxLogits/Conv2d_2b_1x1/biases (1000, 1.00k/1.00k params)
      InceptionV3/AuxLogits/Conv2d_2b_1x1/weights (1x1x768x1000, 768.00k/768.00k params)
      InceptionV3/Conv2d_1a_3x3/biases (32, 32/32 params)
      InceptionV3/Conv2d_1a_3x3/weights (3x3x3x32, 864/864 params)
      InceptionV3/Conv2d_2a_3x3/biases (32, 32/32 params)
      InceptionV3/Conv2d_2a_3x3/weights (3x3x32x32, 9.22k/9.22k params)
      InceptionV3/Conv2d_2b_3x3/biases (64, 64/64 params)
      InceptionV3/Conv2d_2b_3x3/weights (3x3x32x64, 18.43k/18.43k params)
      InceptionV3/Conv2d_3b_1x1/biases (80, 80/80 params)
      InceptionV3/Conv2d_3b_1x1/weights (1x1x64x80, 5.12k/5.12k params)
      InceptionV3/Conv2d_4a_3x3/biases (192, 192/192 params)
      InceptionV3/Conv2d_4a_3x3/weights (3x3x80x192, 138.24k/138.24k params)
      InceptionV3/Logits/Conv2d_1c_1x1/biases (1000, 1.00k/1.00k params)
      InceptionV3/Logits/Conv2d_1c_1x1/weights (1x1x2048x1000, 2.05m/2.05m params)
      InceptionV3/Mixed_5b/Branch_0/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5b/Branch_0/Conv2d_0a_1x1/weights (1x1x192x64, 12.29k/12.29k params)
      InceptionV3/Mixed_5b/Branch_1/Conv2d_0a_1x1/biases (48, 48/48 params)
      InceptionV3/Mixed_5b/Branch_1/Conv2d_0a_1x1/weights (1x1x192x48, 9.22k/9.22k params)
      InceptionV3/Mixed_5b/Branch_1/Conv2d_0b_5x5/biases (64, 64/64 params)
      InceptionV3/Mixed_5b/Branch_1/Conv2d_0b_5x5/weights (5x5x48x64, 76.80k/76.80k params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0a_1x1/weights (1x1x192x64, 12.29k/12.29k params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0b_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0b_3x3/weights (3x3x64x96, 55.30k/55.30k params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0c_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5b/Branch_2/Conv2d_0c_3x3/weights (3x3x96x96, 82.94k/82.94k params)
      InceptionV3/Mixed_5b/Branch_3/Conv2d_0b_1x1/biases (32, 32/32 params)
      InceptionV3/Mixed_5b/Branch_3/Conv2d_0b_1x1/weights (1x1x192x32, 6.14k/6.14k params)
      InceptionV3/Mixed_5c/Branch_0/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5c/Branch_0/Conv2d_0a_1x1/weights (1x1x256x64, 16.38k/16.38k params)
      InceptionV3/Mixed_5c/Branch_1/Conv2d_0b_1x1/biases (48, 48/48 params)
      InceptionV3/Mixed_5c/Branch_1/Conv2d_0b_1x1/weights (1x1x256x48, 12.29k/12.29k params)
      InceptionV3/Mixed_5c/Branch_1/Conv_1_0c_5x5/biases (64, 64/64 params)
      InceptionV3/Mixed_5c/Branch_1/Conv_1_0c_5x5/weights (5x5x48x64, 76.80k/76.80k params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0a_1x1/weights (1x1x256x64, 16.38k/16.38k params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0b_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0b_3x3/weights (3x3x64x96, 55.30k/55.30k params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0c_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5c/Branch_2/Conv2d_0c_3x3/weights (3x3x96x96, 82.94k/82.94k params)
      InceptionV3/Mixed_5c/Branch_3/Conv2d_0b_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5c/Branch_3/Conv2d_0b_1x1/weights (1x1x256x64, 16.38k/16.38k params)
      InceptionV3/Mixed_5d/Branch_0/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5d/Branch_0/Conv2d_0a_1x1/weights (1x1x288x64, 18.43k/18.43k params)
      InceptionV3/Mixed_5d/Branch_1/Conv2d_0a_1x1/biases (48, 48/48 params)
      InceptionV3/Mixed_5d/Branch_1/Conv2d_0a_1x1/weights (1x1x288x48, 13.82k/13.82k params)
      InceptionV3/Mixed_5d/Branch_1/Conv2d_0b_5x5/biases (64, 64/64 params)
      InceptionV3/Mixed_5d/Branch_1/Conv2d_0b_5x5/weights (5x5x48x64, 76.80k/76.80k params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0a_1x1/weights (1x1x288x64, 18.43k/18.43k params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0b_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0b_3x3/weights (3x3x64x96, 55.30k/55.30k params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0c_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_5d/Branch_2/Conv2d_0c_3x3/weights (3x3x96x96, 82.94k/82.94k params)
      InceptionV3/Mixed_5d/Branch_3/Conv2d_0b_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_5d/Branch_3/Conv2d_0b_1x1/weights (1x1x288x64, 18.43k/18.43k params)
      InceptionV3/Mixed_6a/Branch_0/Conv2d_1a_1x1/biases (384, 384/384 params)
      InceptionV3/Mixed_6a/Branch_0/Conv2d_1a_1x1/weights (3x3x288x384, 995.33k/995.33k params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_0a_1x1/biases (64, 64/64 params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_0a_1x1/weights (1x1x288x64, 18.43k/18.43k params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_0b_3x3/biases (96, 96/96 params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_0b_3x3/weights (3x3x64x96, 55.30k/55.30k params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_1a_1x1/biases (96, 96/96 params)
      InceptionV3/Mixed_6a/Branch_1/Conv2d_1a_1x1/weights (3x3x96x96, 82.94k/82.94k params)
      InceptionV3/Mixed_6b/Branch_0/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6b/Branch_0/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0a_1x1/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0a_1x1/weights (1x1x768x128, 98.30k/98.30k params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0b_1x7/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0b_1x7/weights (1x7x128x128, 114.69k/114.69k params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0c_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6b/Branch_1/Conv2d_0c_7x1/weights (7x1x128x192, 172.03k/172.03k params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0a_1x1/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0a_1x1/weights (1x1x768x128, 98.30k/98.30k params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0b_7x1/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0b_7x1/weights (7x1x128x128, 114.69k/114.69k params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0c_1x7/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0c_1x7/weights (1x7x128x128, 114.69k/114.69k params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0d_7x1/biases (128, 128/128 params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0d_7x1/weights (7x1x128x128, 114.69k/114.69k params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0e_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6b/Branch_2/Conv2d_0e_1x7/weights (1x7x128x192, 172.03k/172.03k params)
      InceptionV3/Mixed_6b/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6b/Branch_3/Conv2d_0b_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6c/Branch_0/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6c/Branch_0/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0a_1x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0a_1x1/weights (1x1x768x160, 122.88k/122.88k params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0b_1x7/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0b_1x7/weights (1x7x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0c_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6c/Branch_1/Conv2d_0c_7x1/weights (7x1x160x192, 215.04k/215.04k params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0a_1x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0a_1x1/weights (1x1x768x160, 122.88k/122.88k params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0b_7x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0b_7x1/weights (7x1x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0c_1x7/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0c_1x7/weights (1x7x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0d_7x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0d_7x1/weights (7x1x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0e_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6c/Branch_2/Conv2d_0e_1x7/weights (1x7x160x192, 215.04k/215.04k params)
      InceptionV3/Mixed_6c/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6c/Branch_3/Conv2d_0b_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6d/Branch_0/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6d/Branch_0/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0a_1x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0a_1x1/weights (1x1x768x160, 122.88k/122.88k params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0b_1x7/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0b_1x7/weights (1x7x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0c_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6d/Branch_1/Conv2d_0c_7x1/weights (7x1x160x192, 215.04k/215.04k params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0a_1x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0a_1x1/weights (1x1x768x160, 122.88k/122.88k params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0b_7x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0b_7x1/weights (7x1x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0c_1x7/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0c_1x7/weights (1x7x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0d_7x1/biases (160, 160/160 params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0d_7x1/weights (7x1x160x160, 179.20k/179.20k params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0e_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6d/Branch_2/Conv2d_0e_1x7/weights (1x7x160x192, 215.04k/215.04k params)
      InceptionV3/Mixed_6d/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6d/Branch_3/Conv2d_0b_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6e/Branch_0/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_0/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0b_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0b_1x7/weights (1x7x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0c_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_1/Conv2d_0c_7x1/weights (7x1x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0b_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0b_7x1/weights (7x1x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0c_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0c_1x7/weights (1x7x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0d_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0d_7x1/weights (7x1x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0e_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_2/Conv2d_0e_1x7/weights (1x7x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_6e/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_6e/Branch_3/Conv2d_0b_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_7a/Branch_0/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_7a/Branch_0/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_7a/Branch_0/Conv2d_1a_3x3/biases (320, 320/320 params)
      InceptionV3/Mixed_7a/Branch_0/Conv2d_1a_3x3/weights (3x3x192x320, 552.96k/552.96k params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0a_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0a_1x1/weights (1x1x768x192, 147.46k/147.46k params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0b_1x7/biases (192, 192/192 params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0b_1x7/weights (1x7x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0c_7x1/biases (192, 192/192 params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_0c_7x1/weights (7x1x192x192, 258.05k/258.05k params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_1a_3x3/biases (192, 192/192 params)
      InceptionV3/Mixed_7a/Branch_1/Conv2d_1a_3x3/weights (3x3x192x192, 331.78k/331.78k params)
      InceptionV3/Mixed_7b/Branch_0/Conv2d_0a_1x1/biases (320, 320/320 params)
      InceptionV3/Mixed_7b/Branch_0/Conv2d_0a_1x1/weights (1x1x1280x320, 409.60k/409.60k params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0a_1x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0a_1x1/weights (1x1x1280x384, 491.52k/491.52k params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_1x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_1x3/weights (1x3x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_3x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_1/Conv2d_0b_3x1/weights (3x1x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0a_1x1/biases (448, 448/448 params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0a_1x1/weights (1x1x1280x448, 573.44k/573.44k params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0b_3x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0b_3x3/weights (3x3x448x384, 1.55m/1.55m params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0c_1x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0c_1x3/weights (1x3x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0d_3x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7b/Branch_2/Conv2d_0d_3x1/weights (3x1x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7b/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_7b/Branch_3/Conv2d_0b_1x1/weights (1x1x1280x192, 245.76k/245.76k params)
      InceptionV3/Mixed_7c/Branch_0/Conv2d_0a_1x1/biases (320, 320/320 params)
      InceptionV3/Mixed_7c/Branch_0/Conv2d_0a_1x1/weights (1x1x2048x320, 655.36k/655.36k params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0a_1x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0a_1x1/weights (1x1x2048x384, 786.43k/786.43k params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0b_1x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0b_1x3/weights (1x3x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0c_3x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_1/Conv2d_0c_3x1/weights (3x1x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0a_1x1/biases (448, 448/448 params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0a_1x1/weights (1x1x2048x448, 917.50k/917.50k params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0b_3x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0b_3x3/weights (3x3x448x384, 1.55m/1.55m params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0c_1x3/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0c_1x3/weights (1x3x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0d_3x1/biases (384, 384/384 params)
      InceptionV3/Mixed_7c/Branch_2/Conv2d_0d_3x1/weights (3x1x384x384, 442.37k/442.37k params)
      InceptionV3/Mixed_7c/Branch_3/Conv2d_0b_1x1/biases (192, 192/192 params)
      InceptionV3/Mixed_7c/Branch_3/Conv2d_0b_1x1/weights (1x1x2048x192, 393.22k/393.22k params)