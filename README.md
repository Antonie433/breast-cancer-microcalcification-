# breast-cancer-microcalcification-

# Dataset 
https://www.kaggle.com/datasets/dawidstachowiak/breast-microcalcifications-dataset

# About Dataset
Dataset does not belong to me and is only shared by me. The dataset is from https://zenodo.org/record/5036062#.Y7XQB3bMLyY and the license is Creative Commons Attribution 4.0 International. The data can be useful both in research, learning to analyze data in this form and in competitions with a similar domain.

# General Information

This dataset consists of 100 pairs of mammograms, from two temporally sequential rounds. Specifically, this dataset includes the prior and recent mammograms of CC and MLO view of each patient. This is a complete dataset for the detection and BI-RADS classification of breast micro-calcifications, using digital mammograms. It contains normal (BI-RADS 1), benign (BI-RADS 2), and suspicious (BI-RADS 4-5) cases, and for each mammogram, an image with precise annotation of each individual micro-calcification, by two expert radiologists, is provided. In 32 suspicious cases, the biopsy results are also available.

# Building Models

I built a CNN from scratch with 2 convolutions for the Cancer Breast Calcification project. This custom CNN architecture was designed specifically for this task.

In addition to the custom CNN, I also utilized pre-trained models including ResNet-50, VGG-16, and EfficientNet. These models were trained on large-scale datasets and have learned a wide range of features that can be beneficial for various computer vision tasks, including breast cancer classification.

For the fine-tuning strategy, I loaded the pre-trained model weights and trained the entire model on the Cancer Breast Calcification dataset. However, to prevent the early layers from being overly influenced by the new dataset, I typically froze those layers and only fine-tuned the later layers. This allowed the model to leverage the pre-trained knowledge while adapting to the specifics of the cancer breast calcification task.

For the partial fine-tuning strategy, I selectively froze certain layers, usually the convolutional layers, and only trained the fully connected layers on the Cancer Breast Calcification dataset. By doing so, I retained the lower-level features learned by the pre-trained model, which are likely to be relevant to the task, while customizing the higher-level layers for the specific dataset.

Both fine-tuning and partial fine-tuning strategies enabled me to take advantage of the pre-trained models' knowledge and accelerate the model's learning process. By leveraging these pre-trained models and applying the appropriate fine-tuning strategy, I aimed to improve the performance and accuracy of breast cancer calcification classification on the given dataset.
