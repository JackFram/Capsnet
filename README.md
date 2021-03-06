# Capsnet
- A introduction to Capsnet referenced to Dynamic Routing Between Capsules. You can find the paper [here](https://arxiv.org/pdf/1710.09829.pdf).
- There is a nicely organized pytorch-implemented repo of capsnet [here](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch).
![alt text](png/model.png)
- The video introduction of Capsnet is [here](https://pan.baidu.com/s/1bo03udL) which is really insightful.
- A new model structure based on Capsnet which improve its routing efficiency is [Matrix Capsules with EM routing](https://openreview.net/pdf?id=HJWLfGWRb).
- Walk through and well organized blog written in CN [here](https://zhuanlan.zhihu.com/p/30970675).
![alt text](png/png2.png)
### Three main improvement on traditional CNN.
- Maxpooling layer -> Routing procedure
- Scalar activation -> Capsule sealed representation(vector in Hinton's paper)
- Affine transformation as different view points.
#### The problem of traditional Maxpooling
- Traditional methods for down sampling like Maxpooling, Avgpooling or Convpooling are not sensible with significant linear transformation in image, we need to use some preprocessing tricks like rotationing and cropping to increase model's robustness to transformation invariance. Maxpooling which is widely used can show some invariance to slight changes in an image, but we are more comfortable with equivariance as human vision does. As we human view a same object from a different position relative to our view point, our brain does a dynamic procedure to adjust our attention and that's why dynamic routing is more like a attention model, it not simply use maxpool to down-sample which is too stiff but rather make the network more flexible regard to the capsule position.
- The math trick is to use cosine likelyhood to measure the covariance between two capules in two adjacent layers and adjust the routing coefficiency.
- We don't make elaborations here since in the paper it has been well introduced and shown below.
![alt text](png/routing.png)
#### Why use capsule instead of scalar activation
- We can see that from the prevalent of nerual network up to now, the activation founction always return a scalar to represent the activated propability of that unit, Hinton said it was not enough to use a single number to represent the information in the receptive field. Instead of which, he advocates for a more natural method, Capsule. Personaly, I regard capsule as a wrapper that contain various information of the entity that capsule represent, which is quite intuitive. Between adjacent layers, capsules from a layer above usually seek information from the capsules in the lower layer, which provide the information of some entities that is explainable which is really important to reveal the black box of neural network.
