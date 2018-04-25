<h1 align="center">DLAI-2: Improving Deep Neural Networks</h1>

<p align="center">
<img src="https://ucarecdn.com/04185dea-98f5-4727-86d3-8c4976e030db/" width="70%" height="60%">
</p>


<h1 align="center">About the Course</h1>

In the [second course](https://www.coursera.org/learn/deep-neural-network) of deeplearning.ai, Andrew Ng helps students migrate away from the "black box" approach to deep learning, and instead better understand optimization techniques and intuitions that give deep neural nets a performance boost. 

Some of the deep learning "tricks" explored include: 

- Intuitions about minimizing overfitting and variance in DL projects (e.g., train/dev splits, regularization, etc.)
- Popular regularization options (e.g., Euclidean Norm/L2 Regularization, using Dropout on layers inputting many params) 
- Normalizing inputs to reduce variance, improve cost function optimization and ultimately speed up training 
- How randomizing weight initialization can solve exploding/vanishing gradient issues 
- Using gradient checking to debug the back propagation process
- Optimizing (e.g.,using mini-batch gradient descent, exponentially weighted averages, Adam or RMSprop) on "big data" sets  
- Learning rate decay 
- Practical tips like on how to systematically set up the hyperparameter search process to converge effectively 
- Using batch normalization (Beta/Gamma) on a hidden layer's activation fx to reduce covariate shift (and train params faster) 
- More!

The main takeaway from this course - training deep NNs is a deeply iterative and inductive process: 

<p align="center">
<img src="https://ucarecdn.com/86127f49-327c-4153-a6d1-d9b39ce15cd9/" width="70%" height="60%">
</p>


Up until this course, the specialization mostly focuses on the binary classifier as the DL algorithm of choice. In the final week of this course, Professor Ng introduces a new type of output layer - the "Softmax" layer - which transforms a NN into a multi-class classifier, capable of mapping inputs to one (or more) of many potential prediction classes. 

Lessons on the Softmax layer plant seeds of thought about vector encoding for later courses/network architectures. 

Once all the best practices for tuning hyperparameters have been covered, the course gets into popular frameworks that handle some of the heavy lifting with built-in modular methods that we've been implementing from scratch in our programming assignments, thus far. This "learn-the-proof-first" type of teaching style helps to better understand all the moving parts of a DL framework, like Tensorflow, which we use in our final programming assignment to implement a simple computational graph (linked below). 


## Lessons

- [x] Practical Aspects of Deep Learning
- [x] Optimizing Algorithms
- [x] Tuning Hyperparameters and Batch Normalization


<p align="center">
<img src="https://ucarecdn.com/b9c85edb-9a45-47b0-a466-dd177783745b/" width="60%" height="50%">
</p>



## Programming Assignments

- [x] [Initialization](https://github.com/codeamt/Deep-Learning-AI/blob/master/2%20Improving%20Deep%20Neural%20Networks/Implementations/1%20Practical%20Aspects%20of%20Deep%20Learning/1-PA/README.md)
- [x] [Regularization](https://github.com/codeamt/Deep-Learning-AI/blob/master/2%20Improving%20Deep%20Neural%20Networks/Implementations/1%20Practical%20Aspects%20of%20Deep%20Learning/2-PA/README.md)
- [x] [Gradient Checking](https://github.com/codeamt/Deep-Learning-AI/blob/master/2%20Improving%20Deep%20Neural%20Networks/Implementations/1%20Practical%20Aspects%20of%20Deep%20Learning/3-PA/README.md)
- [x] [Optimization](https://github.com/codeamt/Deep-Learning-AI/blob/master/2%20Improving%20Deep%20Neural%20Networks/Implementations/2%20Optimization%20Algorithms/1-PA/README.md)
- [x] [Tensorflow](https://github.com/codeamt/Deep-Learning-AI/blob/master/2%20Improving%20Deep%20Neural%20Networks/Implementations/3%20Tuning%20Hyperparameters%20and%20Batch%20Normalization/1-PA/README.md)



## Additional Material

<p align="center">
  <b>Hereos of Deep Learning Interview with Yoshua Bengio</b><br>
<img src="https://ucarecdn.com/6682ae29-bb7b-447b-bd1f-c041c5a74594/" width="60%" height="50%"><br>
  Here's where I'll give a brief synopsis of the interview and my takeaways.
</p>

<p align="center">
  <b>Heroes of Deep Learning Interview with Yuanqing Lin</b><br>
<img src="https://ucarecdn.com/31a82d3d-e55f-4b05-b446-4b197c0ef279/" width="60%" height="50%"><br>
  Here's where I'll give a brief synopsis of the interview and my takeaways.
</p>
