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

* **Loss function**: Or also called **cost function**, evaluates the error between the prediction and the ground truth label in every batch. For instance:
  * **Mean Squared Error \(MSE\)**: measures the average squared difference between the actual and predicted labels in the form of:

$$
MSE = \frac{1}{N}\sum_{i=1}^{n}{(y_i-(mx_i+b))^2}
$$

* **Data augmentation**: Regularization method used to decrease the model's variance error consisting in artificially increasing the number and variance of training samples by transforming existing samples to create additional samples. For example, if images are one of the system features, data augmentation can rotate, crop, and reflect each image to produce many variants of the original,  yielding more variate labeled data to decrease the model's error.
* **Fine-tuning**:  Technique used to re-train a pre-trained neural network \(usually in a transfer learning setting\) on a new task with training data from a new domain where the weights of some layers or the whole network may be updated.

#### Hyperparameters

* **Batch size**: The batch size is attributed to the number of training images in one forward or backward pass. It is important to highlight that the higher the batch size, the more memory will be needed.
* **Iterations**: The number of iterations is the number forward or backward of passes: each pass using a batch size number of images.
* **Epoch**: The number of epochs measures how many times every image has been seen during training \(i.e. one epoch means that every image has been seen once\). It can be also understood as a one forward pass and one backward pass of all the training examples.

$$
epochs = \frac{batch\_size * iterations}{training\_
images}
$$

* **Decay**: The weight decay is an additional weight update parameter that induces the weights to exponentially decay to zero once the update process is over.
* **Learning rate**: The learning rate parameter defines the step size for which the weights of a model are updated regarding the stochastic gradient descent.

### Evaluation metrics

#### Classification

* **Accuracy**: which computes the number of correct predictions divided by the total number of samples.
* **Sensitivity:** also known as recall, is computed as the fraction of true positives that are correctly identified.
* **Precision**: which is computed as the fraction of retrieved instances that are relevant.
* **Specificity**: computed as the fraction of true negatives that are correctly identified.

### Data Preprocessing

* **Handling null values:**  Drop samples with null values or replace the null value with some predefined value \(e.g. feature mean or median\). 
* **Standardization:** transform our features  values such that the mean of the values

   is 0 and the standard deviation is 1.

* **Handling categorical variables:** A categorical variable is a variable whose values take on the value of labels. For example, the variable may be _color_ and may take on the values “_purple_,” “_white_,” and “_black_.”  There are many ways to encode categorical variables, although the three most common are as follows:
  1. **One Hot Encoding**: Where each label is mapped to a binary vector.
  2. **Integer Encoding**: Where each unique label is mapped to an integer.
  3. **Learned Embedding**: Where a distributed representation of the categories is learned.

### Image Data Preprocessing

* **Mean subtraction**: in order to center the cloud of RGB values from input data around zero along every dimension of the image, a mean subtraction can be applied across the image features.
* **Image normalization**: By dividing each RGB dimension of input images by its standard deviation, a normalization is obtained from its original 0 and 255-pixel values to 1 an 0 normalized values. This preprocessing technique will avoid further issues caused by poor contrast images.

