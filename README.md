Part 2 of Assignment 1 for CS 587 - Adversarial Machine Learning course, taught by Alexandar Vakanski in Spring 2024 at the University of Idaho - Department of Computer Science.

The objective of this assignment is to implement white-box evasion attacks against deep learning-based classification models.

We used the Oxford Flowers Dataset ( https://www.robots.ox.ac.uk/~vgg/data/flowers/102/ ) for this assignment. The dataset consists of images with 102 categories of flowers, and it has 8,189 images in total.

We trained a deep-learning VGG16 model for classification of the Oxford Flowers dataset, using the PyTorch library. 

Train a deep-learning  for classification of the Oxford Flowers dataset, using the
PyTorch library

We acheieved accuracy of the network on the test images: 87.745098 %.

We imported cleverhans to implement FGSM and PGD attacks.

(
import cleverhans
from cleverhans.torch.attacks.fast_gradient_method import fast_gradient_method
from cleverhans.torch.attacks.projected_gradient_descent import projected_gradient_descent
)

We then applied the FSGM and PGD attacks to create non-targeted adversarial examples using the first 200 images of the test set. The following perturbation magnitudes:  

[1/255, 3/255, 5/255, 8/255, 20/255, 50/255, 80/255].

Further analysis can be found on Shahi_Assignment_1.pdf.
