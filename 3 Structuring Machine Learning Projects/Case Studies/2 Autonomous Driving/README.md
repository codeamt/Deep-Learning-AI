<h1 align="center">Autonomous driving (case study)</h1>

## Scenario

To help you practice strategies for machine learning, in this week we’ll present another scenario and ask how you would act. We think this “simulator” of working in a machine learning project will give a task of what leading a machine learning project could be like!

You are employed by a startup building self-driving cars. You are in charge of detecting road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. As an example, the above image contains a pedestrian crossing sign and red traffic lights.

<img src="https://ucarecdn.com/8d1786ff-4167-4ba8-8e12-0757cf66c5f4/" width="50%" height="40%" >

Your 100,000 labeled images are taken using the front-facing camera of your car. This is also the distribution of data you care most about doing well on. You think you might be able to get a much larger dataset off the internet, that could be helpful for training even if the distribution of internet data is not the same.

You are just getting started on this project. What is the first thing you do? Assume each of the steps below would take about an equal amount of time (a few days).

<p align="center">
<img src="../2 Autonomous Driving/cs2_q1.png" width="70%" height="60%" >
</p>

Your goal is to detect road signs (stop sign, pedestrian crossing sign, construction ahead sign) and traffic signals (red and green lights) in images. The goal is to recognize which of these objects appear in each image. You plan to use a deep neural network with ReLU units in the hidden layers.

For the output layer, a softmax activation would be a good choice for the output layer because this is a multi-task learning problem. True/False?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q2.png" width="70%" height="60%" >
</p>

You are carrying out error analysis and counting up what errors the algorithm makes. Which of these datasets do you think you should manually go through and carefully examine, one image at a time?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q3.png" width="70%" height="60%" >
</p>

After working on the data for several weeks, your team ends up with the following data:

100,000 labeled images taken using the front-facing camera of your car.
900,000 labeled images of roads downloaded from the internet.
Each image’s labels precisely indicate the presence of any specific road signs and traffic signals or combinations of them. For example, <img src="https://ucarecdn.com/f9aa0f42-54ee-4a1c-bb3d-f5ed82b17e6b/" height="60px" width="40px" style="display: inline" > means the image contains a stop sign and a red traffic light.

Because this is a multi-task learning problem, you need to have all your y(i) vectors fully labeled. If one example is equal to <img src="https://ucarecdn.com/9594ed7b-eda1-4188-90fd-6291d8af292d/" height="60px" width="40px" style="display: inline" >then the learning algorithm will not be able to use that example. True/False?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q4.png" width="70%" height="60%" >
</p>

The distribution of data you care about contains images from your car’s front-facing camera; which comes from a different distribution than the images you were able to find and download off the internet. How should you split the dataset into train/dev/test sets?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q5.png" width="70%" height="60%" >
</p>

Assume you’ve finally chosen the following split between of the data:

<p align="center">
<img src="https://ucarecdn.com/a58f736e-8e9d-4edc-af28-0114e92eaed0/" width="70%" height="60%" >
</p>

You also know that human-level error on the road sign and traffic signals classification task is around 0.5%. Which of the following are True? (Check all that apply).

<p align="center">
<img src="../2 Autonomous Driving/cs2_q6.png" width="70%" height="60%" >
</p>

Based on table from the previous question, a friend thinks that the training data distribution is much easier than the dev/test distribution. What do you think?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q7.png" width="70%" height="60%" >
</p>

You decide to focus on the dev set and check by hand what are the errors due to. Here is a table summarizing your discoveries:

<p align="center">
<img src="https://ucarecdn.com/3c9a8380-f16a-47b2-9a92-9154a4bd010e/" width="70%" height="60%" >
</p>

In this table, 4.1%, 8.0%, etc.are a fraction of the total dev set (not just examples your algorithm mislabeled). I.e. about 8.0/14.3 = 56% of your errors are due to foggy pictures.

The results from this analysis implies that the team’s highest priority should be to bring more foggy pictures into the training set so as to address the 8.0% of errors in that category. True/False?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q8.png" width="70%" height="60%" >
</p>

You can buy a specially designed windshield wiper that help wipe off some of the raindrops on the front-facing camera. Based on the table from the previous question, which of the following statements do you agree with?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q9.png" width="70%" height="60%" >
</p>

You decide to use data augmentation to address foggy images. You find 1,000 pictures of fog off the internet, and “add” them to clean images to synthesize foggy days, like this:

<p align="center">
<img src="https://ucarecdn.com/c9d0e6a0-343d-4762-b675-be67e862b35f/" width="70%" height="60%" >
</p>

Which of the following statements do you agree with?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q10.png" width="70%" height="60%" >
</p>


After working further on the problem, you’ve decided to correct the incorrectly labeled data on the dev set. Which of these statements do you agree with? (Check all that apply).

<p align="center">
<img src="../2 Autonomous Driving/cs2_q11.png" width="70%" height="60%" >
</p>

So far your algorithm only recognizes red and green traffic lights. One of your colleagues in the startup is starting to work on recognizing a yellow traffic light. (Some countries call it an orange light rather than a yellow light; we’ll use the US convention of calling it yellow.) Images containing yellow lights are quite rare, and she doesn’t have enough data to build a good model. She hopes you can help her out using transfer learning.

What do you tell your colleague?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q12.png" width="70%" height="60%" >
</p>

Another colleague wants to use microphones placed outside the car to better hear if there’re other vehicles around you. For example, if there is a police vehicle behind you, you would be able to hear their siren. However, they don’t have much to train this audio system. How can you help?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q13.png" width="70%" height="60%" >
</p>

To recognize red and green lights, you have been using this approach:

- (A) Input an image (x) to a neural network and have it directly learn a mapping to make a prediction as to whether there’s a red light and/or green light (y).
A teammate proposes a different, two-step approach:

- (B) In this two-step approach, you would first (i) detect the traffic light in the image (if any), then (ii) determine the color of the illuminated lamp in the traffic light.
Between these two, Approach B is more of an end-to-end approach because it has distinct steps for the input end and the output end. True/False?

<p align="center">
<img src="../2 Autonomous Driving/cs2_q14.png" width="70%" height="60%" >
</p>

Approach A (in the question above) tends to be more promising than approach B if you have a ________ (fill in the blank).


<p align="center">
<img src="../2 Autonomous Driving/cs2_q15.png" width="70%" height="60%" >
</p>


