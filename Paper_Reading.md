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




