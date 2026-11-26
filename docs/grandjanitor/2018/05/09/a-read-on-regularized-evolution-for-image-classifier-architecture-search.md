---
title: "A Read on \"Regularized Evolution for Image Classifier Architecture Search\""
date: 2018-05-09
categories: ["Summary"]
---

# A Read on "Regularized Evolution for Image Classifier Architecture Search"

(First appeared in AIDL-LD and AIDL Weekly.)

This is a read on "Regularized Evolution for Image Classifier Architecture Search" which is the paper version of AmoebaNet, the latest result in AutoML (Or this page: [https://research.googleblog.com/…/using-evolutionary-automl…](https://research.googleblog.com/2018/03/using-evolutionary-automl-to-discover.html))

\* If you recall, Google already has several results on how to use RL and evolution strategy (ES) to discover model architecture in the past. e.g. Nasnet is one of the examples.

\* So what's new? The key idea is so-called regularized evolution strategy. What does it mean?

\* Basically it is a tweak of the more standard tournament strategy, commonly used as the means of selecting individual out of a population. ([https://en.wikipedia.org/wiki/Tournament_selection](https://en.wikipedia.org/wiki/Tournament_selection))

\* Tournament is not too difficulty to describe: - Choose random individuals from the population. - Choose the best candidate according to certain optimizing criterion.

You can also use a probabilistic scheme to decide whether to use the second or third best candidate. You might also think of it as throwing away the worst-N-candidate.

\* The AutoML calls this original method by Miller and Goldberg (1995) as non-regularized evolution method.

\* What is "regularized" then? Instead of throwing away the worst-N-candidates. The author proposed to throw away the oldest-trained candidate.

\* Now you won't see a justification of why this method is better until the "Discussion" section. Okay, let's go with the authors' intended flow. As it turns the regularized method is better than non-regularized method. e.g. In CIFAR-10, the evolved model is ~10% relatively better either man-made model or NasNet. On Imagenet, it performs better than Squeeze-and-Excite Net as well as NasNet. (Squeenze-and-Excite Net is the ILSVRC 2017's winner.)

\* One technicality when you read the paper is the G-X dataset, they are actually the gray-scale version the normal X data. e.g. G-CIFAR-10 is the gray-scale version of CIFAR-10. The intention of why the authors do it are probably two folds: 1) to scale the problem down, 2) to avoid overfitting to only the standard testsets of the problems.

\* Now, these are all great. But how come the "regularized" approach is better then? How would the authors explain it?

\* I don't want to come up with a hypothesis. So let me just quote the last paragraph here: "Under regularized evolution, all models have a short lifespan. Yet, populations improve over longer timescales (Figures 1d, 2c,d, 3a–c). This requires that its surviving lineages remain good through the generations. This, in turn, demands that the inherited architectures retrain well (since we always train from scratch, the weights are not heritable). On the other hand, non-regularized tournament selection allows models to live infinitely long, so a population can improve simply by accumulating high-accuracy models. Unfortunately, these models may have reached their high accuracy by luck during the noisy training process. In summary, only the regularized form requires that the architectures remain good after they are retrained."

\* And also: "Whether this mechanism is responsible for the observed superiority of regularization is conjecture. We leave its verification to future work."
