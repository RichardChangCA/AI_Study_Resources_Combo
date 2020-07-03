<h3> Resources </h3>

1. Youtube, Two Minute Papers: https://www.youtube.com/user/keeroyz/videos

2. Website, Distill: https://distill.pub ,online journel with visual explanations

<h3> Articles </h3>

1. Medium, Deep Learning Research and How to Get Immersed: https://towardsdatascience.com/deep-learning-research-and-how-to-get-immersed-8bab98c20577

Consider the structure and context of the paper

Several questions during reading papers:

- What are the biggest unanswered questions in this field?

- When and why is the result useful?

- What were the constraints of the research?

- Are any of the insights transferable to other fields?

- Why do some ideas receive wider reach while others fall flat?

- What are the authors not discussing in the paper?

Read both Abstract and Introduction at first.

Pay closer attention to the methods and results.

<h3> Papers </h3>

1. 2019, Multi-Resolution CNN and Knowledge Transfer for Candidate Classification in Lung Nodule Detection, https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=8662660 ,Multi-resolution CNN, Knowledge transfer, the size of lung nodule varies, some tissues look similar with lung nodules.

2. 2016, 3D U-Net: Learning Dense Volumetric Segmentation from Sparse Annotation, https://arxiv.org/pdf/1606.06650.pdf ,3D Biomedical Volumetric Image Segmentation, Semi-automated segmentation: the user annotates some slices of each volume to be segmented. The network predicts the dense segmentation. more slices, better performance. Fully-automated segmentation: the network is trained with annotated slices from a representative training set and can be run on non-annotated volumes. Semi-automated better than Fully-automated. sparsely annotated training data. rigid transformations and slight elastic deformations still yield biologically plausible images. batch normalization(BN) before each ReLU: each batch is normalized during training with its mean and standard deviation and global statistics are updated using these values. This is followed by a layer to learn scale and bias explicitly. At test time, normalization is done via these computed global statistics and the learned scale and bias. weighted softmax loss function. Setting the weights of unlabeled pixels to zero makes it possible to learn from only the labelled ones and, hence, to generalize to the whole volume. performance gain of 3D to 2D.

3. 2017, Automatic Segmentation and Overall Survival Prediction in Gliomas using Fully Convolutional Neural Network and Texture Analysis, https://arxiv.org/pdf/1712.02066.pdf ,dataset: BraTS 2017. 3D connected component analysis -> discard components below a certain threshold -> reduce false positive. predict the prognosis of subject. FCNN -> extracted features(both low and complex level features) along with age of the subject -> Extreme gradient boosting(XGBOOST) regressor to predict the prognosis of the subject. biomedical images -> similar structure -> small dataset & less epochs enough. weighted cross entropy loss. Pyradiomics: python package -> extract features from medical images.

4. 2019, Random 2.5D U-net for Fully 3D Segmentation, https://arxiv.org/pdf/1910.10398.pdf ,maximum intensity project or the Radon-transform to project 3D volumes into 2D images, learnable reconstruction algorithm to lift 2D projection images to volumetric data. Maximum intensity projection for high sparsity. 

5. 2019, Projection-Based 2.5D U-net Architecture for Fast Volumetric Segmentation, https://arxiv.org/pdf/1902.00347.pdf ,maximum intensity projections from different directions,  the shortage of 3D-Unet: huge memory requirements and long training time, the shortage of 2D-Unet: the loss of connection between the slice images, equidistant angles for projection directions

6. 2016, V-Net: Fully Convolutional Neural Networks for Volumetric Medical Image Segmentation, https://arxiv.org/pdf/1606.04797.pdf ,data augmentation(random non-linear transformation & histogram matching), reduce resolution by using appropriate stride, residual function in each stage, differentiated Dice with respect to the j-th voxel of the prediction as the loss function to replace to the re-weighted loss, data augmentation: control-points and B-spline interpolation & histogram matching

7. 2019, Ensemble of Fully Convolutional Neural Network for Brain Tumor Segmentation from Magnetic Resonance Images, https://link.springer.com/content/pdf/10.1007%2F978-3-030-11726-9.pdf ,2*3D+2D, post-processing(CRF, class-wise 3-D connected component analysis: all components within each class were retrained while the rest were discarded), ensemble aids in reducing the variance associated in the prediction and also helped in increasing quality of the segmentation generated. 

8. 2019, 3D Dilated Multi-Fiber Network for Real-time Brain Tumor Segmentation in MRI, https://arxiv.org/pdf/1904.03355.pdf ,reduce computation cost, multi-modal MRI scans is a challenging task due to the heterogeneous appearance and shape of gliomas, the multi-fibre unit takes advantage of a multiplexer for information routing, channel grouping(fibres) is to split the convolutional channels as multiple groups that can reduce the connections between the feature maps and kernels for parameter saving significantly, two 1*1*1 convolutions(squeeze and then inflate channels) can reduce half of the parameters as compared to using one 1*1*1 convolution, dilated fibre with various dilated rates—>learnable weights for each dilated branches to select most valuable information automatically from different field of view, lightweight and efficient Dilated Multi-Fiber network(group convolution, learnable weighted 3D dilated convolution to gain multi-scale image representation)

9. 2019, MASK-RCNN AND U-NET ENSEMBLED FOR NUCLEI SEGMENTATION, https://arxiv.org/pdf/1901.10170.pdf ,open source package CellProfiler supports adding neural networks to its processing pipeline, Mask-RCNN: find the bounding boxes(good object detection) and then segmentation, which is worse than U-Net,  segmentation overlap between two models and above the threshold are recognized as final segmentation, watershed post-processing for U-Net, different  kinds of segmentation errors in Mask-RCNN & U-Net and ensemble them can get better performance. 

10. 2018, 3D MRI brain tumor segmentation using autoencoder regularization, https://arxiv.org/pdf/1810.11654.pdf ,Due to a limited training dataset size, a variational auto-encoder branch is added to reconstruct the input image itself in order to regularize the shared decoder and impose additional constraints on its layers. The VAE branch reconstructs the input image into itself, and is used only during training to regularize the shared encoder. Group Normalization shows better than Batch Normalization performance when batch size is small. 3D bilinear upsampling with 1*1*1 convolution for upsampling, to reduce channels. Sigmoid function in multi-channels rather than softmax function in the last layer.  Combined loss: dice loss + 0.1 * L2 distance + 0.1 * KL divergence.

11. 2014, R-CNN, Rich feature hierarchies for accurate object detection and semantic segmentation Tech report (v5) , https://arxiv.org/pdf/1311.2524.pdf , OverFeat: sliding-window detector based on a similar CNN architecture, R-CNN: input image —> extract region proposals —> compute CNN features(extract fixed-length feature vector) —> classify regions(linear SVMs), various category-independent region proposals methods(selective search in R-CNN), semantic segmentation: support vector regresssion(SVR) —> multi-scale per-pixel classifier

12. 2018, AnatomyNet: Deep learning for fast and fully automated whole-volume segmentation of head and neck anatomy, https://aapm.onlinelibrary.wiley.com/doi/pdf/10.1002/mp.13300?casa_token=Ev2mBXkz0joAAAAA:ONW24Vd4DQoKDEhVSBOB_00oQbiUaNE92YR8zYDZI2pT68laqzILXb3VzRc6c7rfpaVx2KVgOLm3H78 ,based-on 3D-UNet, a)a new encoding scheme to allow auto segmentation on whole-volume CT images, b)incorporating 3D squeeze-and-excitation residual blocks in encoding layers, c)a new loss function combining Dice scores and focal loss. Address two main challenges 1)small anatomies occupying only a few slices 2)training with inconsistent data annotations with missing ground truth for some anatomical structures. Traditional atlas-based anatomy segmentation methods is difficult to handle anatomy variations among patients. Missing annotation problem: masked and weighted loss function, too much downsampling may have a negative impact on small anomalies, hybrid loss(dice loss + focal loss, the dice loss learns the class distribution alleviating the imbalanced voxel problem, where as the focal loss forces the model to learn poorly classified voxels better, modified hybrid loss to handle missing annotations problem), the U-Net with one downsampling layer works better on small organ segmentation than the standard U-Net probably because downsampling reduces image resolution and makes it harder to segment small organs.

13. 2017, ShuffleNet: An Extremely Efficient Convolutional Neural Network for Mobile Devices, http://openaccess.thecvf.com/content_cvpr_2018/CameraReady/0642.pdf ,point-wise group convolution(first introduced in AlexNet), channel shuffle, group number g controls the connection sparsity of point wise convolutions

14. 2019, Squeeze-and-Excitation Networks, https://arxiv.org/pdf/1709.01507.pdf ,adaptively recalibrate channel-wise feature responses by explicitly modelling interdependencies between channels, author claim that providing the unit with a mechanism to explicitly model dynamic non-linear dependencies between channels using global information can ease the learning process, and significantly enhance the representational power of the network. Squeeze: Global Information Embedding. Excitation: Adaptive Recalibration, gating mechanism(bottleneck with two fully-connected(FC) layers around the non-linearity in the output of squeeze block, dimensionality-reduction layer with reduction ratio r and then dimensionality-increasing layer returning to the channel dimension of the transformation output U). F_scale refers to channel-wise multiplication between the scalar s and the feature map u. SE-block has more computational burden, trade-off between the number of parameters and the performance(the majority of parameters come from the final stage of the network, so in practice, remove SE-block on final stage with only small cost in performance), SE blocks consistently improve performance across different depths with an extremely small increase in computational complexity, 

15. 2020, Segmentation Loss Odyssey, https://arxiv.org/pdf/2005.13449.pdf ,various loss function in deep learning-based medical image segmentation methods, PyTorch implementations of these loss functions are https://github.com/JunMa11/SegLoss 

