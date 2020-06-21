---
layout: post
title: "Dog Breed Classification PyTorch"
date: 2020-06-10
---

### Summary

Using the dog image dataset, train a CNN that can classify different dog breeds over 133 kinds. Build an app that can detect a human or a dog's face and classify which dog breed it is closest to.

### Outline

1. Face Recognition
   - Detect a face (human or dog) using a pre-traiend cv2 module in python and VGG16 in `torchvision.models`
2. Creating CNN from scratch
   - Use CNN artchitecture (Conv2d-BatchNorm-ReLU blocks, AvgPool2D transition)
   - Train using crossentropy loss and ADAM optimizer iteration
3. Transfer learning with ResNet50
   - Load the ResNet50 model and train against our own dog image dataset
4. Combining it together
   - Create one function that takes in a image, detect a face, and print out the closest dog breed.

### Result

CNN from scratch: Accuracy of 13% after 20 epochs (800,000 params)
Transfer from ResNet50: Accuracy of 80% after 20 epochs (272,000 trainable params)

### Tools

- PyTorch

<span class="improved">Link</span> [Colab Notebook](https://colab.research.google.com/drive/1S8Lcqo9BoAn12Z0q9jg3hu9J3oJm_W62#scrollTo=9uPWOoBcbSGB)
