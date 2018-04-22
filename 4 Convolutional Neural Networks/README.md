<h1 align="center">DLAI-4: Convolutional Neural Networks</h1>

<p align="center">
<img src="https://ucarecdn.com/cdf16046-ab52-4196-a75d-113304a3798f/" width="70%" height="60%">
</p>

<h1 align="center">About the Course</h1>

In the [fourth installment](https://www.coursera.org/learn/convolutional-neural-networks) of deeplearning.ai, Andrew Ng introduces the Convolutional Neural Network (CNN) and how to apply CNNs on unstructured data (in this case of this course, image data).

The most prevelant use case for the CNN architecture is <i>Computer Vision</i>; an area of deep learning that has broken ground over the past 2-3 years. Examples of Computer Vision include: 

- Autonomous Driving 
- Facial Recognition 
- Automatic Reading of Radiology Images 
- Neural Style Transfer 

Up until this point in the course, programming assignments have implemented binary image classifiers with the basic, fully connected neural network architecture. With CNNs, trainers can process big data sets of high resolution photos with fewer paramaters by *convolving* inputs with filters of smaller dimension. 

<p align="center">
<img src="https://ucarecdn.com/107f52b1-30a9-4644-995f-ce52f37b4c03/" width="60%" height="50%">
</p>

In a Convolutional NN, when applied to an input vector of images, the operation illustrated above functions like the matrix multiplication operation that occurs during the linear regression process of a fully connected layer in a traditional Deep Neural Net. 

The ***convolutional layer*** outputs a convolved matrix, ***z***, and when stacked together, each convolutional layer detects for a certain feature (like, horizontal or vertical edges) of the inputed image before undergoing some non-linear transformation (e.g., like ReLu activation) to get a visual cipher image that acts as the activation input for the next layer. 

<p align="center">
<img src="https://ucarecdn.com/52890d97-5388-4ef5-99e5-c12575a39baa/" width="60%" height="50%">
</p>

The shape of these filter cubes, together with the 1-dimensional bias variable, determine the number of parameters for the respective filter layer, regardless of how big/resolute the input image is. Parameters can also be shared when similar features need to be detected later on in the network. 

Professor Ng works through the logic of hyperparameter tuning for convolutional layers, like increasing/decreasing stride (s) and/or padding (p), as well as the types of optimization layers we can use. 

***Pooling layers***, for example, do not take in parameters, but instead help us to crop inputs, delay activation decay, keep the number of parameters reasonable, and improve performance.  Pooling is to CNNs, what Dropout is (kind of) to regular Deep NNs. 


<img src="https://ucarecdn.com/ed2f5418-fc64-4b40-ae0c-ab69ba1212ff/" width="40%" height="200px">
<img src="https://ucarecdn.com/ed2f5418-fc64-4b40-ae0c-ab69ba1212ff/" width="40%" height="200px">

We use these building box layers along with fully-connected layers (usually, at least a logistical softmax layer that outputs a probability score) to design unique architectures to solve unique computer vision problems. 

Some of the classic CNN architectures/algorithms and topics explored in this course: 

- [x] LeNet 
- [x] AlexNet 
- [x] variations of VGGNet 
- [x] ResNet 
- [x] Inception Netowrk 
- [x] YOLO 
- [x] One Shot Learning 
- [x] Siamese Network

Other best practices and takeaways: 

- [x] transfer learning and using open-source implementation 
- [x] data pre-processing techniques (e.g., data augmentation) 
- [x] Vector encoding 
- [x] Applying CNNs on 2D and 3D data 


## Lessons
- [x] Foundations of Convolutional Neural Networks
- [x] Deep convolutional models
- [x] Face recognition & Neural style transfer

<p align="center">
<img src="https://ucarecdn.com/20723218-2752-4059-a76d-6aa8a08f3575/" width="60%" height="50%">
</p>

## Python Implementations

- [x] [Convolutional Model: step by step](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/1%20Foundations%20of%20CNNs/1-PA/README.md)
- [x] [Convolutional model: application](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/1%20Foundations%20of%20CNNs/2-PA/README.md)
- [x] [Keras Tutorial - Happy Housev2](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/2%20Deep%20Convolutional%20Models/1-PA/README.md)
- [x] [Residual Networks](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/2%20Deep%20Convolutional%20Models/2-PA/README.md)
- [x] [Car detection with YOLOv2](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/3%20Object%20Detection/1-PA/README.md)
- [x] [Art generation with Neural Style Transfer](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/4a%20Neural%20Style%20Transfer/1-PA/README.md)
- [x] [Face Recognition for the Happy House](https://github.com/codeamt/Deep-Learning-AI/blob/master/4%20Convolutional%20Neural%20Networks/Implementations/4b%20Face%20Recognition/1-PA/README.md)


## Additional Material

<p align="center">
  <b>Heroes of Deep Learning Interview with Yann LeCun</b><br>
<img src="" width="400px" height="350px">
</p>

**Reviewed Research Papers:**

- [[1]]() LeCun et al., 1998. *Gradient-based learning applied to document recognition*
- [[2]]() Krizhevsky et al., 2012. *ImageNet classification with deep convolutional neural networks*
- [[3]]() Simonyan and Zisserman. 2015. *Very deep convolutional networks for large-scale image recognition*
- [[4]]() He et al., 2015. *Deep residual networks for image recognition.*
- [[5]]() Lin et al., 2013. *Network in network.*
- [[6]]() Zsegedy et al., 2014. *Going deeper with convolutions.*
- [[7]]() Redmon et al., 2015. *You Only Look Once: Unified real-time object detection.*
- [[8]]() Sermanet et al., 2014. *OverFeat: Integrated recognition, localization and detection using convolutional networks.*
- [[9]]() Girshik et al., 2013. *Rich feature heirarchies for accurate object detection and semantic segmentation.*
- [[10]]() Girshik et al., 2015. *Fast R-CNN.*
- [[11]]() Ren et al., 2016. *Faster R-CNN: Towards real-time object detection with region proposal networks.*
- [[12]]() Taigman et al., 2014. *DeepFace closing the gap to human level performance.*
- [[13]]() Schroff et al., 2015. *FaceNet: A unified embedding for face recognition and clustering.*
- [[14]]() Zeiler and Fergus., 2013. *Visualizing and understanding convolutional networks.*
- [[15]]() Gatys et al., 2015, *A neural algorithm of artistic style.*
