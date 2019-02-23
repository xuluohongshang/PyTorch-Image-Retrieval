# PyTorch Image Retrieval  
PyTorch framework for image retrieval task including implementations of [N-pair Loss (NIPS 2016)](http://papers.nips.cc/paper/6199-improved-deep-metric-learning-with-multi-class-n-pair-loss-objective)
 and [Angular Loss (CVPR 2017)](https://arxiv.org/pdf/1708.01682.pdf).

### Loss function
We implemented loss functions to train the image retrieval network.  
Batch sampler for the loss function borrowed from [here](https://github.com/adambielski/siamese-triplet).
- [N-pair Loss (NIPS 2016)](http://papers.nips.cc/paper/6199-improved-deep-metric-learning-with-multi-class-n-pair-loss-objective): Sohn, Kihyuk. "Improved Deep Metric Learning with Multi-class N-pair Loss Objective," Advances in Neural Information
    Processing Systems. 2016.
- [Angular Loss (CVPR 2017)](https://arxiv.org/pdf/1708.01682.pdf): Wang, Jian. "Deep Metric Learning with Angular Loss," CVPR, 2017

### Self-attention module
We attached the Self-attention module of the [Self-Attention GAN](https://arxiv.org/abs/1805.08318) to the conventional classification networks (e.g. DenseNet, ResNet or SENet).  
Implementation of the module borrowed from [here](https://github.com/heykeetae/Self-Attention-GAN).

### Data augmentation
We adopted data augmentation techniques used by [Single Shot MultiBox Detector](https://arxiv.org/abs/1512.02325).

### Post processing
We utilized some post-processing while the inference phase.
- Moving the origin of the feature space to the center of the feature vectors
- L2-normalization
- [Average query expansion](https://www.robots.ox.ac.uk/~vgg/publications/papers/chum07b.pdf)
- [Database-side feature augmentation](https://arxiv.org/pdf/1610.07940.pdf)