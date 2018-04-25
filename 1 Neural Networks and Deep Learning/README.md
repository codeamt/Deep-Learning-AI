<h1 align="center">DLAI-1: Neural Network and Deep Learning</h1>


<p align="center">
<img src="https://ucarecdn.com/cf7d2668-ef01-489f-a591-c8f6b4274c2d/" width="70%" height="60%">
</p>

<h1 align="center">About the Course</h1>

In the [first course](https://www.coursera.org/learn/neural-networks-deep-learning) of deeplearning.ai, Andrew Ng provides a thoughtful introduction to the foundational concepts of deep learning. 

Deep learning, a branch of AI, denotes the regressive process of learning from various types of data, such as images, words, and sounds. A bare bones implementation of a Neural Network requires: 

- the appropriate co-efficient values ("the weights") and bias values (together, "the parameters") for multi-dimensional inputs (meaning, featurized x values - say, a record of houses and respective features, like number of bedrooms, bathrooms, windows, etc., for those houses) 

- a schematic formula (a model), architected with these learned parameters, that predicts outputs (y values/"labels", sometimes also multi-dimensional, but following the aforementioned example, say the market price) for those inputs with a freakishly high level of accuracy. 

We start off basic in the first week, and unpack how logistic regression (weight generation), gradient descent (weight correction) and cost calculation (error analysis) work for a single training example (e.g., a single house-to-price mapping),  and move outward to apply these processes for some (n) number of training examples (e.g., ALL the houses, all in one loop), first in a single perceptron (one layer), 

<p align="center">
<img src="https://ucarecdn.com/0b85575b-6c0f-434d-8f9e-d01ca7f0c732/" width="60%" height="50%"
</p>
  
then, in a multi-layer perceptron, or a deep network.

<p align="center">
<img src="https://ucarecdn.com/70d6d8d2-699e-4869-8df3-5d9a8558a7c0/" width="60%" height="50%" >
</p>

The magic of deep learning happens in the inner parts of an architected model, using aforementioned layers of what we call "neurons" that activate and facilitate the learning process. The actual "learning" happens with the help of the ***gradient descent algorithm*** that uses partial derivatives to correct the weights generated in the forward feed process until we can't any longer (hit a local minimum for loss), thereby systematically improving our model's learning.

<p align="center">
  <img src="https://ucarecdn.com/51808340-5082-4aa6-b53c-eb09449001b0/" width="60%" height="50%" >
</p>

Professor Ng goes beyond providing the theory, and demonstrates how to implement this process in actual Python code, including methods for vectorizing some (n) number of inputs with some (m) number of features to decrease the time complexity of operations and speed up the weight learning process.

## Lessons

- [x] Neural Network Basics
- [x] Shallow Neural Networks
- [x] Deep Neural Networks


<p align="center">
<img src="https://ucarecdn.com/8b064603-8fc5-471b-80d8-4a621d2c665d/" width="60%" height="50%">
</p>


## Programming Assignments

- [x] [Logistic Regression with a Neural Network mindset](https://github.com/codeamt/Deep-Learning-AI/tree/master/1%20Neural%20Networks%20and%20Deep%20Learning/Implementations/2%20Neural%20Networks%20Basics/2-PA)
- [x] [Planar data classification with a hidden layer](https://github.com/codeamt/Deep-Learning-AI/blob/master/1%20Neural%20Networks%20and%20Deep%20Learning/Implementations/3%20Shallow%20Neural%20Networks/1-PA/README.md)
- [x] [Building your deep neural network: step by step](https://github.com/codeamt/Deep-Learning-AI/blob/master/1%20Neural%20Networks%20and%20Deep%20Learning/Implementations/4%20Deep%20Neural%20Networks/1-PA/README.md)
- [x] [Deep Neural Network Application](https://github.com/codeamt/Deep-Learning-AI/blob/master/1%20Neural%20Networks%20and%20Deep%20Learning/Implementations/4%20Deep%20Neural%20Networks/2-PA/README.md)


## Additional Material

<p align="center">
 **Heroes of Deep Learning Interview with Geoffrey Hinton**
  <br>
<img src="https://ucarecdn.com/4cdcee7d-58d4-4cc2-b2a0-120e5de1cbbc/" width="60%" height="50%">
</p>


<p align="center">
  **Heroes of Deep Learning Interview withPieter Abbeel**
  <br>
<img src="https://ucarecdn.com/98688241-365b-4930-b5fe-36788aa7ed8c/" width="60%" height="50%">
</p>


<p align="center">
  **Heroes of Deep Learning Interview with Ian Goodfellow**
  <br>
<img src="https://ucarecdn.com/61d0da6e-d8b7-4bdb-8130-94b27de9a317/" width="400px" height="350px">
</p>
