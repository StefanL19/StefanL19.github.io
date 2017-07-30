---
layout: post
title:  "Understanding Convolutional Neural Networks (with an implementation in Keras)"
date:   2016-08-20 11:11:11 +0100
thumbnail: understand_conv_networks_keras.jpg

---

One of the most trending deep learning techniques is called Convolutional Neural Networks (CNNs). It achieves highest scores on the ImageNet competitions in the last several years and this makes it research topic number 1 for both scientists and programmers. When I started dealing with this topic, I tought that it will be complicated and the math behind it will be so difficult that I will never understand it. You know, some kind of stuff that is composed of so many things that it will take me a lifetime to relate. Well, now I claim that by understanding just a few simple ideas you will be able to start building your knowledge on a solid foundation.

> ## Idea behind convolutions

Ok, lets start from the name. *Convolutional* stays for the idea of having a filter which convolves around an image and extracts features which then help us build our predictions. Imagine the following process:

**Input (Image) -> Black Box (Extract Features) -> Use features to classify -> Obtain result**

at the very end we have our image classified as one of the possible classes within we want our model to distinguish. The convolutions take part in the second step and are the building block behind the **Black Box**.

> ## Black Box - Extract features

First, jsut to make the things clear for those of you who are already familiar with the terminology and haven't seen this term used here. I made it up completely by myself, my idea is that sometimes when we design algorithms we take a pretrained model and treat this part exactly as a black box - we take it for granted and perfectly working. But lets get back to the convolutions. 

The output volume for our problem a.k.a. as the result from the **Input Image** step will be, usually, `N x N x 3` volume. Where the depth will mean - just the number of channels - `Red, Green, Blue`. When we have this input we perform the following steps:

1. Depending on our architecture we want to different number of layers included in our **Black Box**. Mathematically speaking, we want to apply several functions on our input before obtaining the result. Lets say the input is `x`, in order to extract the features we want to apply the following procedure:

$$result = f(f(f...f(x)))$$

2. Take the first layer after the input. We will connstruct in the following way.
<figure>
	<img src="{{ site.baseurl }}/assets/understand_conv_networks_keras.jpg" alt="image">
	<figcaption>
		Wouldn't it be great if a computer can recognize your cat?
	</figcaption>
</figure>

Swine brisket tongue pork cow pork loin beef ribs turkey flank rump strip steak.
