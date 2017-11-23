# Capsnet
Pytorch implemented Capsnet referenced to Dynamic Routing Between Capsules. You can find the paper [here](https://arxiv.org/pdf/1710.09829.pdf)
![alt text](png/model.png)
### Two new improvement compared to traditional CNN
BatchNormalization layer somehow ignores the variance in space and spin of an image. Therefore Hinton came out with an method of dynamic routing procedure to replace the BN layer. 
#### Dynamic routing system
how to combine routing algorithm with weight update?
#### Activation scalar to vecter
#### Reconstruction —— For regularization
