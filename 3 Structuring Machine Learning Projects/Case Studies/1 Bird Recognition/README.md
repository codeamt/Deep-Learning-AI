<h1 align="center">Bird Recognition in the city of Peacetopia</h1> 


## Problem Statement
This example is adapted from a real production application, but with details disguised to protect confidentiality.


<p align="center">
<img src="https://ucarecdn.com/5577f03c-1858-46a0-862e-d9702a2c88d2/" width="70%" height="60%" >
</p>

You are a famous researcher in the City of Peacetopia. The people of Peacetopia have a common characteristic: they are afraid of birds. To save them, you have to build an algorithm that will detect any bird flying over Peacetopia and alert the population.

The City Council gives you a dataset of 10,000,000 images of the sky above Peacetopia, taken from the city’s security cameras. They are labelled:

- y = 0: There is no bird on the image
- y = 1: There is a bird on the image

Your goal is to build an algorithm able to classify new images taken by security cameras from Peacetopia.

There are a lot of decisions to make:

- What is the evaluation metric?
- How do you structure your data into train/dev/test sets?

## Metric of Success 

The City Council tells you the following that they want an algorithm that

1. Has high accuracy

2. Runs quickly and takes only a short time to classify a new image.

3. Can fit in a small amount of memory, so that it can run in a small processor that the city will attach to many different security cameras.

<b>Note:</b> Having three evaluation metrics makes it harder for you to quickly choose between two different algorithms, and will slow down the speed with which your team can iterate. True/False?

<p align="center">
<img src="../1 Bird Recognition/cs1_q1.png" width="70%" height="60%" >
</p>

After further discussions, the city narrows down its criteria to:

- "We need an algorithm that can let us know a bird is flying over Peacetopia as accurately as possible."
- "We want the trained model to take no more than 10sec to classify a new image.”
- “We want the model to fit in 10MB of memory.”<br>

If you had the three following models, which one would you choose?

<p align="center">
<img src="../1 Bird Recognition/cs1_q2.png" width="70%" height="60%" >
</p>

Based on the city’s requests, which of the following would you say is true?

<p align="center">
<img src="../1 Bird Recognition/cs1_q3.png" width="70%" height="60%" >
</p>

## Structuring Your Data

Before implementing your algorithm, you need to split your data into train/dev/test sets. Which of these do you think is the best choice?

<p align="center">
<img src="../1 Bird Recognition/cs1_q4.png" width="70%" height="60%" >
</p>

After setting up your train/dev/test sets, the City Council comes across another 1,000,000 images, called the “citizens’ data”. Apparently the citizens of Peacetopia are so scared of birds that they volunteered to take pictures of the sky and label them, thus contributing these additional 1,000,000 images. These images are different from the distribution of images the City Council had originally given you, but you think it could help your algorithm.

You should not add the citizens’ data to the training set, because this will cause the training and dev/test set distributions to become different, thus hurting dev and test set performance. True/False?

<p align="center">
<img src="../1 Bird Recognition/cs1_q5.png" width="70%" height="60%" >
</p>

One member of the City Council knows a little about machine learning, and thinks you should add the 1,000,000 citizens’ data images to the test set. You object because:

<p align="center">
<img src="../1 Bird Recognition/cs1_q6.png" width="70%" height="60%" >
</p>

You train a system, and its errors are as follows (error = 100%-Accuracy):

<img src="https://ucarecdn.com/51aed7b6-c7a6-429f-a52b-bfe013cb05c3/" width="50%" height="40%" >

This suggests that one good avenue for improving performance is to train a bigger network so as to drive down the 4.0% training error. Do you agree?

<p align="center">
<img src="../1 Bird Recognition/cs1_q7.png" width="70%" height="60%" >
</p>

You ask a few people to label the dataset so as to find out what is human-level performance. You find the following levels of accuracy:

<img src="https://ucarecdn.com/aac301d7-e4f0-40c2-8008-467ca454c908/" width="50%" height="40%" >

<p align="center">
<img src="../1 Bird Recognition/cs1_q8.png" width="70%" height="60%" >
</p>

Which of the following statements do you agree with?

<p align="center">
<img src="../1 Bird Recognition/cs1_q9.png" width="70%" height="60%" >
</p>

You find that a team of ornithologists debating and discussing an image gets an even better 0.1% performance, so you define that as “human-level performance.” After working further on your algorithm, you end up with the following:

<img src="https://ucarecdn.com/8f794608-b08d-4fd2-afd3-babdb2d44c7e/" width="50%" height="40%" >

<p align="center">
<img src="../1 Bird Recognition/cs1_q10.png" width="70%" height="60%" >
</p>


You also evaluate your model on the test set, and find the following:

<img src="https://ucarecdn.com/4d392f5e-2c42-47a8-9ef2-c0a1cbdd9aeb/" width="50%" height="40%" >

<p align="center">
<img src="../1 Bird Recognition/cs1_q11.png" width="70%" height="60%" >
</p>

After working on this project for a year, you finally achieve:

<img src="https://ucarecdn.com/54ebe674-44cc-4543-b4ac-be0e9290046d/" width="50%" height="40%" >

<p align="center">
<img src="../1 Bird Recognition/cs1_q12.png" width="70%" height="60%" >
</p>


It turns out Peacetopia has hired one of your competitors to build a system as well. Your system and your competitor both deliver systems with about the same running time and memory size. However, your system has higher accuracy! However, when Peacetopia tries out your and your competitor’s systems, they conclude they actually like your competitor’s system better, because even though you have higher overall accuracy, you have more false negatives (failing to raise an alarm when a bird is in the air). What should you do?

<p align="center">
<img src="../1 Bird Recognition/cs1_q13.png" width="70%" height="60%" >
</p>

You’ve handily beaten your competitor, and your system is now deployed in Peacetopia and is protecting the citizens from birds! But over the last few months, a new species of bird has been slowly migrating into the area, so the performance of your system slowly degrades because your data is being tested on a new type of data.

<p align="center">
<img src="https://ucarecdn.com/645306fb-c337-45b6-89c6-6dedc2229c44/" width="70%" height="60%" >
</p>

You have only 1,000 images of the new species of bird. The city expects a better system from you within the next 3 months. Which of these should you do first?

<p align="center">
<img src="../1 Bird Recognition/cs1_q14.png" width="70%" height="60%" >
</p>

The City Council thinks that having more Cats in the city would help scare off birds. They are so happy with your work on the Bird detector that they also hire you to build a Cat detector. (Wow Cat detectors are just incredibly useful aren’t they.) Because of years of working on Cat detectors, you have such a huge dataset of 100,000,000 cat images that training on this data takes about two weeks. Which of the statements do you agree with? (Check all that agree.)

<p align="center">
<img src="../1 Bird Recognition/cs1_q15.png" width="70%" height="60%" >
</p>
