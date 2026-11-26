---
title: "Weekly Issue 27 - Origin Story of Prof. Andrew Ng, Backdoored ANN and Superconvergence"
date: 2019-07-02
---

# Weekly Issue 27 - Origin Story of Prof. Andrew Ng, Backdoored ANN and Superconvergence

## Editorial

### Thoughts From Your Humble Curators

Our main piece this week is about Prof. Andrew Ng, on his earlier work on machine learning and why he decided to teach ML to the public. We also take a closer look at the secret sauce of Waymo's SDC development: their Texas campus and their simulation facilities.

Other than that, we have links on six blog posts and three papers. They are mostly technical topics - leisure reading for the last week in the Summer. Perhaps what caught our eyes is the idea of backdoored neural network and superconvergence. The former is a new form of attack on DNN from the a malicious model preparer. The latter promises 10x training speed for a class of loss functions.

Finally, if you want to take the deeplearning.ai class, AIDL now has a [new satellite group](https://www.facebook.com/groups/DeepLearningAISpecialization/) just for you!

---

As always, if you like our newsletter, remember to subscribe and forward it your colleagues!

Artificial Intelligence and Deep Learning Weekly

## Sponsor

### [Use Slack? Amplify your team's productivity with this collaboration tool](https://www.cyclops.io/?utm_source=AIDL-newsletter)

[Add to your Slack team](https://www.cyclops.io/slack) and launch from Slack. Works in your browser. No Download. No login. Get up and running in seconds. [Multiply](https://www.youtube.com/watch?v=QCf_XHQXuV4) team's productivity

[cyclops.io](https://www.cyclops.io/?utm_source=AIDL-newsletter)

## [Sponsor AIDL Weekly and reach thousands of A.I. & Deep Learning researchers and developers](http://aidl.io/sponsorship/index.html)

## News

### [Origin Story of Prof. Andrew Ng](https://apnews.com/83b60f5e55f04e8184608b0eb1bf7d0a)

A piece on Prof. Ng., his view on AI and his recent work on deeplearning.ai. What fascinates us? Do you know Andrew and his team once crash a $10000 helicopter drone? And he starts to program neural network when he was 16! So check it out.

[apnews.com](https://apnews.com/83b60f5e55f04e8184608b0eb1bf7d0a)

---

### [Waymo Simulation Facilities](https://www.theatlantic.com/technology/archive/2017/08/inside-waymos-secret-testing-and-simulation-facilities/537648/)

In this article, Atlantic's Alexis C. Madrigal brought us to the secret sauce of Waymo's SDC development. There are so many interesting part we can comment. But the whole idea that the Waymo team would simply set up physical prop and test SDC is fairly interesting. Another important idea there is simulation-based driving.

[theatlantic.com](https://www.theatlantic.com/technology/archive/2017/08/inside-waymos-secret-testing-and-simulation-facilities/537648/)

## Blog Posts

### [A Write-Up from Brain Resident Colin Raffel](http://colinraffel.com/blog/)

This is a great write-up by Colin Raffel who was a Brain Resident, and now a Google Brain Scientist. Raffel's description on his technical work is certainly interesting, but more fascinating is how Google Brain works as a research institute.

[colinraffel.com](http://colinraffel.com/blog/)

---

### [OpenAI Release Two More Baseline Algorithms](https://blog.openai.com/baselines-acktr-a2c/)

That includes the algorithm Actor Critic using Kronecker-factored Trust Region (ACKTR) and Asynchronous Advantage Actor Critic (A3C).

[openai.com](https://blog.openai.com/baselines-acktr-a2c/)

---

### [How does Physics Connect to Machine Learning?](https://jaan.io/how-does-physics-connect-machine-learning/)

This is a great note on Ising model, as well as how physics and ML are related in general. I think it is an interesting read for any one who is studying probabilistic graphical models.

[jaan.io](https://jaan.io/how-does-physics-connect-machine-learning/)

---

### [Pytorch or Tensorflow?](https://awni.github.io/pytorch-tensorflow/)

Here is a point by point comparison between Pytorch and Tensorflow. It does confirm our feeling that while Tensorflow is still the most prominent toolkit, Pytorch is gaining ground and its debugging capability gain more love from researchers.

[github.io](https://awni.github.io/pytorch-tensorflow/)

---

### [Backprop is Not Just The Chain Rule](http://timvieira.github.io/blog/post/2017/08/18/backprop-is-not-just-the-chain-rule/)

Backpropagation is a deep concept. There are thousands of tutorial will teach you to "understand ANN" by using very small network, and doing differentiation explicitly. To Dr Karpathy's, a much more sophisticated thinking is seeing the data as flowing backward in the computational graphs. Theory of back-propagation is fascinating. And as Tim Viera said, it is not just simply about chain rule.

In this post, the OP describes the significance of using backprop to do audo-differentiation, which is significantly different from what we learn in calculus or symbolic differentiation. He also poses differentiation as a Langrangian problem. The blog describes several important results such as calculation of gradient of function is provably be as fast as a function. We found it very important to grok, especially if you want to learn the detail of the modern deep learning framework.

[github.io](http://timvieira.github.io/blog/post/2017/08/18/backprop-is-not-just-the-chain-rule/)

---

### [Imposter Syndrome](https://brohrer.github.io/imposter_syndrome.html)

An interesting blog post which discuss being a data scientist but not having formal credential. I bet it resonates with many of our readers.

[github.io](https://brohrer.github.io/imposter_syndrome.html)

## Paper/Thesis Review

### [BadNets: A Backdoored Neural Network](https://arxiv.org/abs/1708.06733)

NYU presents a new idea which suggest that a malicious human model preparer can create a backdoor weakness in a neural network. That results in what they called BadNets. In essence what you need to do is just to train two classifier, one normal and one trained with backdoor samples. Then you just create a network that run in parallel of the two. Indeed, in the sea of parameters within an NN, it would be a very difficult to detect such malicious behavior.

NYU researchers does argue that it is very dangerous to outsource model training to a 3rd party. It's also very important to use trusted individual to create a benign network.

[arxiv.org](https://arxiv.org/abs/1708.06733)

---

### [A Brief Survey of Deep Reinforcement Learning](https://arxiv.org/pdf/1708.05866v1.pdf)

A great survey on deep reinforcement learning, which read like a condensed version of both David Silver's class as well as the Berkeley RL's class combined. The author starts from the basics such as DP-based, MCMC-based algorithms. Then move towards to motivate deep reinforcement learning which a deep neural network is used to represent the value function. Then touch modern topics such as trusted policy region optimization (TRPO) and the latest challenges in the field such as limitation of behavior cloning, exploration vs exploitation etc. It will be a great read for you if you already took at least one RL class.

[arxiv.org](https://arxiv.org/pdf/1708.05866v1.pdf)

---

[*[image not recovered: twenty_by_nine_extra_large_fb0e953f-8b2d-4ef3-8992-4f878ca211d6.png]*](https://arxiv.org/pdf/1708.07120.pdf) 

### [Super Convergence](https://arxiv.org/pdf/1708.07120.pdf)

This is interesting preprint published 2 days ago and it quickly become the top-hyped at arxiv-sanity. If what the author said is true, it would mean a class of loss function could be trained with 10x the speed. The method is also quite simple which all of you can implement. There are Math and code to support it. 

It's still a preprint. So be cautious to use it in practice!

[arxiv.org](https://arxiv.org/pdf/1708.07120.pdf)
