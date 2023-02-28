# Image_classification_with_Vision_Transformer-Python

This example implements the Vision Transformer (ViT) model by Alexey Dosovitskiy et al. for image classification, and demonstrates it on the CIFAR-100 dataset. 
The ViT model applies the Transformer architecture with self-attention to sequences of image patches, without using convolution layers.

After 100 epochs, the ViT model achieves around 55% accuracy and 82% top-5 accuracy on the test data.
These are not competitive results on the CIFAR-100 dataset, as a ResNet50V2 trained from scratch on the same data can achieve 67% accuracy.
Note that the state of the art results reported in the paper are achieved by pre-training the ViT model using the JFT-300M dataset, then fine-tuning it on the target dataset. To improve the model quality without pre-training, you can try to train the model for more epochs, use a larger number of Transformer layers, resize the input images, change the patch size, or increase the projection dimensions. Besides, as mentioned in the paper, the quality of the model is affected not only by architecture choices, but also by parameters such as the learning rate schedule, optimizer, weight decay, etc. 
In practice, it's recommended to fine-tune a ViT model that was pre-trained using a large, high-resolution dataset.
