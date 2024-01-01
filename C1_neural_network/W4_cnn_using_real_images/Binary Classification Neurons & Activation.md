# Binary Classification: Neurons & Activation

**Binary Classification**: In multiclass classification, the output layer can be configured with one neuron per class when employing the **softmax** activation function. However, for binary class classification using the **sigmoid** activation function, only a single neuron is needed to represent two classes. This is due to the fact that in the sigmoid function, one class tends toward 0 while the other class tends toward 1. While it's possible to use the **softmax** activation in binary classification, it requires two neurons in that scenario.

Compressing images to lower resolution will decrease the training time but it may not provide good predictions.

---

1. After reducing the size of the images, the training results were different. Why?
    - There was less information in the images
    - We removed some convolutions to handle the smaller images
    - The training was faster
    - There was more condensed information in the images

Incorrect

Not quite. Reducing the size doesn’t condense information.

AI Explanation:

1. "There was less information in the images": Reducing the size of images typically means a loss of information, which could affect training results.
2. "We removed some convolutions to handle the smaller images": Altering the convolutional structure can indeed impact training outcomes, so this could be a valid reason.
3. "The training was faster": Smaller images often lead to faster training times, but it doesn't necessarily guarantee different results. The speed of training and the outcome are somewhat independent.
4. "There was more condensed information in the images": This option seems contradictory to the idea of reducing image size, as it implies an increase in information density.