---
description: 'You will learn: basic concepts and terms used in the AI/ML community.'
---

# ML Terminology

## Artificial Intelligence

* **Artificial Intelligence**: A non-human program or model that can solve sophisticated tasks. For example, a program or model that translates text or a program or model that identifies diseases from radiologic images both exhibit artificial intelligence.
* **Machine Learning**: A program or system that builds \(trains\) a predictive model from input data. The system uses the learned model to make useful predictions from new \(never-before-seen\) data drawn from the same distribution as the one used to train the model. Machine learning also refers to the field of study concerned with these programs or systems.
* **Deep Learning**: type of Machine Learning containing neural network with multiple hidden layers.

### Machine Learning

#### Types

* **Supervised Learning**: Training a model from input data and its corresponding labels. Supervised machine learning is analogous to a student learning a subject by studying a set of questions and their corresponding answers. After mastering the mapping between questions and answers, the student can then provide answers to new \(never-before-seen\) questions on the same topic. Compare with unsupervised machine learning.
* **Semi-supervised learning**: Training a model on data where some of the training examples have labels but others don’t. One technique for semi-supervised learning is to infer labels for the unlabeled examples, and then to train on the inferred labels to create a new model. Semi-supervised learning can be useful if labels are expensive to obtain but unlabeled examples are plentiful.
* **Unsupervised Learning**: Training a model to find patterns in a dataset, typically an unlabeled dataset.
* **Reinforcement Learning**: A family of algorithms that learn an optimal policy, whose goal is to maximize return when interacting with an environment. For example, the ultimate reward of most games is victory. Reinforcement learning systems can become expert at playing complex games by evaluating sequences of previous game moves that ultimately led to wins and sequences that ultimately led to losses.

### Training

* **Loss function**: \(also called cost function\) evaluates the penalty between the prediction and the ground truth label in every batch.
  * **Mean Absolute Error \(MAE\)**: measures the average squared difference between the actual and predicted labels in the form of:

$$
MSE = \frac{1}{N}\sum_{i=1}^{n}{(y_i-(mx_i+b))^2}
$$

* **Data augmentation**: Artificially boosting the range and number of training examples by transforming existing examples to create additional examples. For example, suppose images are one of your features, but your dataset doesn't contain enough image examples for the model to learn useful associations. Ideally, you'd add enough labeled images to your dataset to enable your model to train properly. If that's not possible, data augmentation can rotate, stretch, and reflect each image to produce many variants of the original picture, possibly yielding enough labeled data to enable excellent training.
* **Fine-tuning**: training technique that requires replacing the last fully connected layer of the network with a new classification task and use the training data from the new domain to update the weights of some layers.

#### Hyperparameters

* **Batch size**: The batch size is attributed to the number of training images in one forward or backward pass. It is important to highlight that the higher the batch size, the more memory will be needed.
* **Iterations**: The number of iterations is the number forward or backward of passes: each pass using a batch size number of images.
* **Epoch**: The number of epochs measures how many times every image has been seen during training \(i.e. one epoch means that every image has been seen once\). It can be also understood as a one forward pass and one backward pass of all the training examples.

$$
epochs = \frac{batch size * iterations}{trainingimages}
$$

* **Decay**: The weight decay is an additional weight update parameter that induces the weights to exponentially decay to zero once the update process is over.
* **Learning rate**: The learning rate parameter defines the step size for which the weights of a model are updated regarding the stochastic gradient descent.

### Evaluation metrics

#### Classification

* **Accuracy**: which computes the number of correct predictions divided by the total number of samples.
* **Sensitivity:** also known as recall, is computed as the fraction of true positives that are correctly identified.
* **Precision**: which is computed as the fraction of retrieved instances that are relevant.
* **Specificity**: computed as the fraction of true negatives that are correctly identified.

### Preprocessing

* **Mean subtraction**: in order to center the cloud of RGB values from input data around zero along every dimension of the image, a mean subtraction is applied across the image features.
* **Image normalization**: By dividing each RGB dimension of input images by its standard deviation, a normalization is obtained from its original 0 and 255-pixel values to 1 an 0 normalized values. This preprocessing technique will avoid further issues caused by poor contrast images.

