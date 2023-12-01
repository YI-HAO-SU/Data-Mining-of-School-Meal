# Data-Mining-of-School-Meal

The dataset used in this final project is sourced from the Ministry of Education's Campus Food Ingredient Registration Platform, encompassing nutritional lunch data from primary and secondary schools. 
The image on the right illustrates the training data within the dataset, comprising a total of 50 categories.

The objective of this project is to classify images from each category effectively.
Through analysis and model training, the project aims to establish a system capable of recognizing and distinguishing various food ingredients or types. 
This system is intended to enhance efficiency and accuracy in tasks related to school lunch management.

![圖片](https://github.com/YeeHaoSu/Data-Mining-of-School-Meal/assets/90921571/d1b11dc2-514d-471d-9adb-3336788d81f4)


# Data Analysis

![圖片](https://github.com/YeeHaoSu/Data-Mining-of-School-Meal/assets/90921571/9cb9948e-610e-45ae-920f-8aca6222e186)

Average: 699 images per class
Max: Jujube 863 images
Min: Fushan Lettuce 130 images

Q1: Data imbalance
According to the information provided by the teaching assistant, some instances of data imbalance are observed. Categories such as Fushan Lettuce, Kai-lan, and Organic Qing Song Cai exhibit this imbalance.

Q2: 福山萵苣 and 大陸妹 are the same vegetable
福山萵苣 and 大陸妹 share the same botanical name, Fushan lettuce. 
However, this dataset classifies them as separate categories, potentially causing challenges in classification.

Q3: Difficulty in Vegetable Classification
Certain vegetables pose challenges in classification due to their visual similarity. 
Examples include Organic Komutsuna, Canola, Fushan Lettuce, and Spoon Cabbage.

# Data Preprocessing

In the preprocessing stage, I applied the following augmentations to the images to enhance the richness of the dataset:

- Rotation
- Filp
- random_saturation
- random_contrast
- random_brightness
- samplewise_std_normalization
- samplewise_center

# Model
The model adopted for this project is EfficientNetV2, known for its lightweight design and high accuracy, demonstrating outstanding performance in classification tasks. Here are the key differences between EfficientNetV2 and its predecessor, EfficientNetV1:

1. **Network Architecture:**
   EfficientNetV2 introduces a novel network structure called "Stochastic Depth." This structure randomly drops some layers during each training iteration, mitigating overfitting and enhancing the network's generalization capabilities.

2. **Optimization Strategy:**
   EfficientNetV2 employs a more advanced optimization strategy known as "Adaptive Gradient Clipping." This strategy automatically adjusts the gradient clipping range based on the gradient magnitudes of each parameter. This adaptation helps strike a better balance between the speed and direction of gradient updates.

