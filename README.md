# Capsnet
- Pytorch implemented Capsnet referenced to Dynamic Routing Between Capsules. You can find the paper [here](https://arxiv.org/pdf/1710.09829.pdf).
- There is a nicely organized pytorch-implemented repo of capsnet [here](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch).
- The video introduction link is [here](https://pan.baidu.com/s/1bo03udL) which is quite insightful.
- A new model structure based on Capsnet which improve its routing efficiency is [here](https://openreview.net/pdf?id=HJWLfGWRb).
- Walk through and well organized blog written in CN [here](https://zhuanlan.zhihu.com/p/30970675).
![alt text](png/model.png)
### Two new improvement compared to traditional CNN
BatchNormalization layer somehow ignores the variance in space and spin of an image. Therefore Hinton came out with an method of dynamic routing procedure to replace the BN layer. 
#### Dynamic routing system
how to combine routing algorithm with weight update?
#### Activation scalar to vecter
#### Reconstruction —— For regularization
