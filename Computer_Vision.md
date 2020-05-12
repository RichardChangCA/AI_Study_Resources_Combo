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
