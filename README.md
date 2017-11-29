# Capsnet
- A introduction to Capsnet referenced to Dynamic Routing Between Capsules. You can find the paper [here](https://arxiv.org/pdf/1710.09829.pdf).
- There is a nicely organized pytorch-implemented repo of capsnet [here](https://github.com/laubonghaudoi/CapsNet_guide_PyTorch).
- The video introduction of Capsnet is [here](https://pan.baidu.com/s/1bo03udL) which is really insightful.
- A new model structure based on Capsnet which improve its routing efficiency is [here](https://openreview.net/pdf?id=HJWLfGWRb).
- Walk through and well organized blog written in CN [here](https://zhuanlan.zhihu.com/p/30970675).
![alt text](png/model.png)
### Two main improvement on traditional CNN
- Maxpooling layer -> Routing procedure
- Scalar activation -> Capsule sealed representation(vector in Hinton's paper)
##### The problem of traditional Maxpooling

