---
title: "A Read on \"Dynamic Routing Between Capsules\""
date: 2018-05-09
---

# A Read on "Dynamic Routing Between Capsules"

(Also check out Keran's discussion - very exciting! I might go to write a blurb on the new capsule paper which seems to be written by Hinton and friends.)

As you know this is the Hinton's new invention of capsules algorithm. It's been a while I want to delve into this idea. So here is a write up: It's tl;dr but I doubt I completely grok the idea anyway.

\* The first mention of "capsule" is perhaps in the paper "Transforming Auto-encoders" which Hinton and students coauthored.

\* It's important to understand what capsules trying to solve before you delve into the details. If you look at Hinton's papers and talks, capsule is really an idea which improve upon Convnet, there are two major complaints from Hinton.

\* First the general settings of Convnet assume that 1 filter is being used across different location. This is also known as "location invariance". In this setting, the exact location of a feature doesn't matter. That has a lot to do with robust feature parameter estimation. It also drastically simplify backprop with weight sharing.

\* But then location invariance also removes one important information of an image: the apparent location.

\* Second assumption is max pooling. As you know, pooling usually removes a high percentage of information from a layer. In early architectures, usually pooling is the key to shrink the size of a representation down. Of course, later architectures had changed. But pooling is still an important component.

\* So the design of capsule has a lot of do to tackle problems of max pooling. Instead of losing information, can we "route" this information correctly so that they are optimal use? That's the thesis.

\* Generally "capsule" represents a certain entity of an image, "such as pose (position, size, orientation), deformation, velocity, albedo, hue, texture etc". Notice that they are not hard-wired and automatically discovered.

\* Then there is how the low level information can "route" to higher level. The mechanism is intriguing in this current implementation:

\* First, your goal is to calculate a softmax in the form of

exp(b\_{ij} / Sum_k exp(b\_{ik} where b\_{ij} is the output of lower level capsule i to a higher level capsule j. This is something you can train.

\* Then what you do is iteratively estimate b\_{ij}. This appears in Procedure 1. The 4 steps are:

a, calculate the softmax weight b. b, compute the prediction vector from a capsule i, then form a weighted sum, c, squash the weighted sum d, update softmax weight b based on the squash value and weighted sum.

\* So why the squash function, my guess is it is to normalize the value computed in b. According to Hinton, a good function is

v_j = |s_j|^2 / (1 + |s_j|^2) \* s_j / |s_j|

\* The rest of the architecture actually looks very much like a Convnet. The first layer was a Convnet with ReLU activation.

\* Would this work? The authors say yes. Not only it reaches the state of art benchmark of MNIST. It can also tackle more difficult task such as CIFAR-10, SVNH. In fact, the authors found that in both task they already achieve better results when first Convnet was first used to tackle these tasks.

\* It also works well for two tasks called affMNISt and multiMNIST. First is MNIST go through affine transform, second is MNIST regenerated with many overlappings. This is quite impressive, because you will need to use much data augmentation and effort of object detection to get these cases working.

\* The part I have doubt - is this model more complex than convnet? If it is show, it's possible that we are just fitting a more complex model to get better results.

\* Nice thing about the implementation: it's tensorflow, so we can expect and play with it in the future.

That's what I have so far. Have fun!
