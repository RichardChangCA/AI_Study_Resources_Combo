1. Youtube Computer Vision Convolutional Neural Network(CNN) deeplearning.ai Andrew Ng: https://www.youtube.com/watch?v=ArPaAX_PhIs&list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF

Convolution(1D,2D,3D), Pooling, ResNet, Inception, Transfer Learning, Data Augmentation, Object Detection, Sliding Windows, Intersection Over Union(IoU), Anchor Boxes, YOLO, Region Proposals, Face Recognition, Siamese Network, Face Verification, Style Transfer

2. Medium, Transfer Learning for Image Classification using Keras: https://towardsdatascience.com/transfer-learning-for-image-classification-using-keras-c47ccf09c8c8

3. Medium, Google Open Sources SimCLR, A Framework for Self-Supervised and Semi-Supervised Image Training: https://towardsdatascience.com/google-open-sources-simclr-a-framework-for-self-supervised-and-semi-supervised-image-training-72b06d5d58a0 ,this article may be not clear, but you can check the Paper: https://arxiv.org/abs/2002.05709 and the GitHub repo: https://github.com/google-research/simclr

4. Medium, Implementing a ResNet model from scratch: https://towardsdatascience.com/implementing-a-resnet-model-from-scratch-971be7193718 ，understanding resnet in detail

5. Medium, Face Detection in 10 lines for Beginners： https://towardsdatascience.com/face-detection-in-10-lines-for-beginners-1787aa1d9127 ，face, elbow, mouse detection by opencv lib in python

6. Youtube, Autoencoders - EXPLAINED: https://www.youtube.com/watch?v=7mRfwaGGAPg ,Mask Region based Convolution Neural Networks - EXPLAINED!(mask r-cnn): https://www.youtube.com/watch?v=4tkgOzQ9yyo ,this youtuber(CodeEmporium) explains concepts in a simple way: https://www.youtube.com/channel/UC5_6ZD6s8klmMu9TXEB_1IA

7. Medium, Understanding ResNet(winner in ILSVRC 2015): https://medium.com/@14prakash/understanding-and-implementing-architectures-of-resnet-and-resnext-for-state-of-the-art-image-cf51669e1624 ,This residual architecture ensures the deeper model can outperform shallow models because the function of the residual block is F(x)=H(x)-x. If the model reaches the optima, F(x) will be 0, meaning residual connection can automatically determine the depth of deep learning models.

8. Medium, GoogLeNet(InceptionV1): https://medium.com/coinmonks/paper-review-of-googlenet-inception-v1-winner-of-ilsvlc-2014-image-classification-c2b3565a64e7 ,idea: use 1*1 conv in middle, global avg pooling to replace FC layer, 1*1 conv can increase the effect of non-linearality as well as reduce the dimentionality of models(channels) to reduce computation. global avg pooling in the last layer can reduce number of weights and less prone to overfitting, intermediate softmax branches in inception model is used for training only(auxillary loss function), these intermediate softmax results are used in weighted loss function to tackle the problem of gradient vainishing(although it can be tackled well by ResNet).

9. Medium, InceptionV3 1st Runner Up (Image Classification) in ILSVRC 2015:  https://medium.com/@sh.tsang/review-inception-v3-1st-runner-up-image-classification-in-ilsvrc-2015-17915421f77c ,inception v2 adds batch normalization based on inceptionv1 and inceptionv3 uses Factorizing Convolutions to reduce the number of parameters ,in addition, inceptionv3 uses grid size reduction to replace max pooling ,Auxiliary classifier in inceptionv3 is only used for regularization, moreover, Label Smoothing As Regularization

10. Medium, Review: MobileNetV1 — Depthwise Separable Convolution (Light Weight Model): https://towardsdatascience.com/review-mobilenetv1-depthwise-separable-convolution-light-weight-model-a382df364b69 MobileNet: MobileNet uses depthwise separable convolution to reduce the model size and complexity, which is a light-weight model. However, in most cases, depthwise separable convolution in MobileNet cannot perform better than the standard convolution. 

11. Medium, Review: VGGNet — 1st Runner-Up (Image Classification), Winner (Localization) in ILSVRC 2014 , https://medium.com/coinmonks/paper-review-of-vggnet-1st-runner-up-of-ilsvlc-2014-image-classification-d02355543a11 , VGGNet uses 3*3 filters and multi-scale training & testing first(without fully connected layers), as well as replaces fully-connected layers with convolutional layers to improve the performance.

12. Medium, Review: Pre-Activation ResNet with Identity Mapping — Over 1000 Layers Reached (Image Classification)： https://towardsdatascience.com/resnet-with-identity-mapping-over-1000-layers-reached-image-classification-bb50a42af03e ,pre-activation can ensure ResNet do clean identity mapping, this new ResNet can reach 1001 layers.

13. Medium, DenseNet — Dense Convolutional Network(CVPR 2017), https://towardsdatascience.com/review-densenet-image-classification-b6631a8ef803 ,while batch normalization can tackle the gradient vanishing & exploding, and deeper neural network is not overftting(overfitting is low bias and high variance), it is more likely a degradation, because deeper neural network training loss is higher than shallow neural network(higher bias) in plain neural networks. This is probably because the non-linear transformation lost the information of the original images, this is maybe why retnet works. Since this reason, Dense network works better than Resnet because each layer combines shallow features and higher features together.

14. Medium, Depth-wise Convolution and Depth-wise Separable Convolution: https://medium.com/@zurister/depth-wise-convolution-and-depth-wise-separable-convolution-37346565d4ec ,in computer vision, we use depth-wise conv more, but the problem of this is too much paramters(input channel*output channel*filter size*2), we can use depth-wise separable conv(1*1 conv after depth-wise conv) to reduce parameters(input channel*filter size*2 + input channel*output channel), this method also works well.

15. Medium, AlexNet, CaffeNet: https://medium.com/coinmonks/paper-review-of-alexnet-caffenet-winner-in-ilsvrc-2012-image-classification-b93598314160 ,AlexNet is a milestone architecture in deep learning, CaffeNet is a single-GPU version of AlexNet, some ideas in these two architectures are old-school.

16. Medium, SqueezeNet: https://towardsdatascience.com/review-squeezenet-image-classification-e7414825581a ,use fire model to squeeze model parameters.SqueezeNet can perform same as original models without squeezing. squeeze ratio set is another hyper-parameter to fine-tune. In this article, the complex bypass SqueezeNet performs worse than simple bypass SqueezeNet probably because only 1*1 conv cannot extract more contextual features as good as expanded (1*1, 3*3) conv sets.

17. Medium, Counting No. of Parameters in Deep Learning Models by Hand https://towardsdatascience.com/counting-no-of-parameters-in-deep-learning-models-by-hand-8f1716241889 reduce the model size and training time with less parameters. predict whether your model is out of memory before training and determine suitable batch size. including cnn,rnn,mlp. You can know how to calculate feature maps in CNN models, cnn uses the most number of parameters and rnn uses the least number of parameters in common compared with these three models.

18. Medium & Paper, WRNs — Wide Residual Networks (Image Classification): https://towardsdatascience.com/review-wrns-wide-residual-networks-image-classification-d3feb3fb2004 ,less layers(training faster) with higher accuracy but wider(more parameters). The problem of restnet is diminishing feature reuse, where a lot of blocks parameters in resnet cannot learn too much, a.k.a less gradient(other researchers randomly disable some blocks when training, similar to dropout). The idea of WRN is from "circuit complexity theory literature showing that shallow circuits can require exponentially more components than deeper circuits"  original paper: https://arxiv.org/pdf/1605.07146.pdf this paper WRN researched resnet a lot, including where use dropout, how much filter size should be used in blocks, pre-activation: conv-BN-ReLU to BN-ReLU-conv. Width in this article means number of channels, which is confused at first glance.

19. Medium, Inception V4: https://towardsdatascience.com/review-inception-v4-evolved-from-googlenet-merged-with-resnet-idea-image-classification-5e8c339d18bc , combine new Inception v4 with Residual Inception v2 as ensemble learning to get a good result,  inception v4 has more inception models than inception v3.

20. Medium, Self-Attention In Computer Vision: https://towardsdatascience.com/self-attention-in-computer-vision-2782727021f6 ,use the idea from NLP to CV(including 3 paper ideas in this article), this idea is efficient maybe because "For radiologists, the experience in reading the images comes mostly from knowing where exactly to look in order to find a certain pathology". fuse local images(self-attention which part is important) and global images(whole image) together to do detection or classification, mask(self-attention) is generated according to the maximal values of different channels in feature maps and this mask can crop the original image to "self-attentioned" image. The first part of this articile uses the hard attention(either 0 or 1) not soft attention(range from 0-1). Since hard attention is not differentiable(cannot be trained), soft self-attention is used in Squeeze-And-Excitation-Networks, this model squeenze feature maps of the image into 1*1*channel (squeeze block)and use relu and sigmoid activation function(reduce dimentionality and expand) to find soft attention values for each global feature maps(channel-wise attention, excitation block). Shallow layer attention values are similar and deeper layer attention values are different, and this shows shallow layers can extract general features and deeper layers can extract specific features. The last article uses the idea of self-attention in NLP(K V Q), the brief idea of this model is transform the current "attention" to the most important part around its neighbors(a.k.a. "share weights" in paper, so this will lose the positional impormation of original images, and this problem is solved by position embedding). this papers visual self-attention is local attention(only consider its neighbors not whole feature maps).

21. Youtube, how to do bilinear interpolation in image upsampling: https://www.youtube.com/watch?v=q4-FJeWcidE ,linear interpolation in 2 dimensions by following a horizontal, vertical and center sequence.

22. Medium, A Walk-through of AlexNet, https://medium.com/@smallfishbigsea/a-walk-through-of-alexnet-6cbd137a5637 

23. Medium, 5 Awesome Projects to Hone Your Deep Learning Skills, https://towardsdatascience.com/5-awesome-projects-to-hone-your-deep-learning-skills-a2d6252b9b9b ,Implementing a convolutional neural network from scratch, Visual exploration of convolutional networks, Building an API for your deep learning model, Contributing to open source frameworks, Paper reproductions

24. Medium, Image Classification of X-Ray Scans, https://towardsdatascience.com/image-classification-of-x-ray-scans-ffaf970783f9 , VGG, data augmentation, binary classification

25. Medium, Face Identification: Siamese Convolutional Neural Nets, https://medium.com/@mark.s.cleverley/face-identification-siamese-convolutional-neural-nets-b4c66771595c ,Siamese Nets: twinned neural networks to identify whether two inputs are same or not. Suitable for the dataset which has limited images for each identity. Good idea(works well with fine-tuning) but poor result in this article.

26. Medium, Understanding Deep Self-attention Mechanism in Convolution Neural Networks, https://medium.com/datadriveninvestor/understanding-deep-self-attention-mechanism-in-convolution-neural-networks-e8f9c01cb251 ,covariance matrix, SAGAN: self-attention GAN

27. Medium, GAN for unsupervised anomaly detection on X-ray images. https://medium.com/vitalify-asia/gan-for-unsupervised-anomaly-detection-on-x-ray-images-6b9f678ca57d , have some issues in this method(just insights), Bi-directional GAN(encoder, generator, discriminator, discriminate between pair of data X and latent variable Z), AlphaGAN(combining autoencoder),

28. Medium, Generative Adversarial Networks (GANs) in 50 lines of code (PyTorch), https://medium.com/@devnag/generative-adversarial-networks-gans-in-50-lines-of-code-pytorch-e81b79659e3f ,original data, random noise, generator, discriminator, teach G to trick D and D to beware G, GAN are not stable.

29. Medium, Guide how to learn and master computer vision in 2020, https://towardsdatascience.com/guide-to-learn-computer-vision-in-2020-36f19d92c934 ,Albumentation(image augmentation framework), catalyst(high-level API on top of pytorch), Kaggle Kernels(30 hours/week free), Google Colab, Courses(Stanford CS231n, Fast.ai), paperswithcode, Kaggle Competitions provide many free open kernels. 

30. Medium, Brain Tumor Segmentation in MRI, https://medium.com/@prajbhumkar/brain-tumor-segmentation-in-mri-abc268faa304 ,MASK R-CNN, transfer learning based on COCO dataset

31. Medium, Analyze Knee MRIs with Python, https://towardsdatascience.com/deep-learning-and-medical-imaging-part-1-explore-the-mrnet-mri-dataset-of-knee-injuries-f519d063165 ,MRNet(knee MRI dataset), MRI scan, interactive plot

32. Medium, How to Train an MRI Classifier with PyTorch, https://medium.com/datadriveninvestor/deep-learning-and-medical-imaging-how-to-provide-an-automatic-diagnosis-f0138ea824d ,model architecture: MRNet, geometric transformations for data augmentation, To take into account the imbalanced nature of the classes, the loss of an example was scaled inversely proportionally to the prevalence of that example’s class in the dataset in order to penalize the error more on the least present examples. Accumulated gradients to prevent fluctuations in the loss.

33. Medium, Interpret What A Deep Learning Model Sees In Medical Imaging, https://medium.com/swlh/deep-learning-and-medical-imaging-interpret-what-the-model-sees-3a1a35b2a323 ,class activation map(weighted sum of the filters)

34. Medium, Build a simple Image Retrieval System with an Autoencoder, https://towardsdatascience.com/build-a-simple-image-retrieval-system-with-an-autoencoder-673a262b7921 ,autoencoder to encoder images + nearest neighbour algorithm to find similar images




