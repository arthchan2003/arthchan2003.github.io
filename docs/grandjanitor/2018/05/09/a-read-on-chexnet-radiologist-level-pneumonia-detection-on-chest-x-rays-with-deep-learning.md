---
title: "A Read on \" CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning\""
date: 2018-05-09
---

# A Read on " CheXNet: Radiologist-Level Pneumonia Detection on Chest X-Rays with Deep Learning"

(First published at AIDL-LD and AIDL Weekly.)

This is a note on CheXNet the paper. As you know it is the widely circulated paper from Stanford, purportedly outperform human's performance on Chest X-ray diagnostic.

\* BUT, after I read it in detail, my impression is slightly different from just reading the popular news including the description on github.

\* Since the ML part is not very interesting. I will just briefly go through it - it's a 121-layer Densenet, basically it means there are feed-forward connection from every previous layers. Given the data size, it's likely a full training. 

\* There was not much justification on the why of the architecture. My guess: the team first tried transfer learning, but decide to move on to full-training to get better performance. A manageable setup would be Densenet.

\* Then there was a fairly standard experimental comparison using AUC. In a nut shell, CheXNet did perform better than humans in every one of the 14 classes of ChestX-ray-14, which is known to be the largest of the similar databases.

\* Now here is the caveat popular news hadn't mentioned: 1, First of all, humans weren't allow to access previous medical records of a patient. 2, Only frontal images were shown to human doctors. But prior work did show when the lateral view was also shown.

\* That's why on p.3 of the article, the authors note: "We thus expect that this setup provides a conservative estimate of human radiologist performance."

which should make you realize that may be it will still take a bit for deep learning to "replace radiologists".
