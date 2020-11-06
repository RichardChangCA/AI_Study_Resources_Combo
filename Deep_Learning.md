1. Medium, Reasons to Choose PyTorch for Deep Learning: https://towardsdatascience.com/reasons-to-choose-pytorch-for-deep-learning-c087e031eaca Deep learning researchers should study both PyTorch & TensorFlow 2.x but focus on only one of them.

2. Medium, Google Just Introduced TensorFlow Developer Certificate Exam: https://towardsdatascience.com/google-just-introduced-tensorflow-developer-certificate-exam-e15c385685b8 ,Tensorflow certificate granted by Google, tensorflow is wildly used in industries, as well as both pytorch and tensorflow are wildly used in academic fields.

3. Medium, 5 Important Changes Coming with TensorFlow 2.0： https://levelup.gitconnected.com/5-important-changes-coming-with-tensorflow-2-0-e6bb172c5fdf

- start to be more similar with numpy

- with keras

- clean up redundant APIs

- tf.datasets

- can run tf1.x in the env of tf.2.x , there is a srcipt to auto-transfer tf1.x to tf2.x

4. Medium, Visualising Filters and Feature Maps for Deep Learning: https://towardsdatascience.com/visualising-filters-and-feature-maps-for-deep-learning-d814e13bd671

5. Medium, Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization: https://www.coursera.org/lecture/deep-neural-network/exponentially-weighted-averages-duStO ，some optimizers are illustrated well, like adam, RMSprop, learning rate decay, momentum, etc.

6. Medium, Deep Learning using GPU on your MacBook https://towardsdatascience.com/deep-learning-using-gpu-on-your-macbook-c9becba7c43 ,use the GPU on your macbook pro to speed up your deep learning models with keras

7. Medium, Deep Learning Course notebooks worth $2,000 are now open source: https://towardsdatascience.com/deep-learning-course-notebooks-worth-2-000-are-now-open-source-7d6bc759ef47 ,GitHub open source book repo: https://github.com/fastai/fastbook , online courses video: https://course.fast.ai/videos/?lesson=1 , the open source book: Deep Learning for Coders with fastai & PyTorch

8. Youtube, Why Does Batch Normormalization Work? (C2W3L06): https://www.youtube.com/watch?v=nUUqwaxLnWs , batch normalization can speed up the training process because the covariance shift can shift the mini-batch data distribution into normal distribution(which can represent the whole dataset distribution well), and have "slight" regularization effect because normalization is processed within mini-batch(maybe not representative), which generates a little noise. 

9. Medium, Probably the Best Resource to Learn Deep Learning in 2020: https://towardsdatascience.com/probably-the-best-resource-to-learn-deep-learning-in-2020-66d13a8ab1f1 ,code out neurons, layers, activation functions, optimizers, gradients, backpropagation — pretty much everything — completely from scratch, for understanding deep learning deeper. (but no cnn and rnn includes)

10. Course_1, Youtube, Andrew Ng, deeplearning.ai ,Neural Networks and Deep Learning, https://www.youtube.com/watch?v=CS4cs9xVecg&list=PLkDaE6sCZn6Ec-XTbcX1uRg2_u4xOEky0&i ,logistic regression, gradient descent, derivatives, computation graph, vectorization(batch size and matrix computation), broadcasting in python, cost function, activation function, forward-propagation and back-propagation, random initialization, hyper-parameters.  Circuit Theory and Deep Learning: Informally, there are functions you can compute with a “small” L-layer deep neural network that shallower networks require exponentially more hidden units to compute.

11. Course_2, Youtube, deeplearning.ai ,Andrew Ng ,Improving Deep Neural Networks: Hyper-parameter Tuning, Regularization and Optimization, https://www.youtube.com/watch?v=1waHlpKiNyY&list=PLkDaE6sCZn6Hn0vK8co82zjQtt3T2Nkqc&index=2&t=0s

Train/Validation/Test Sets, Bias/Variance, Frobenius norm, L2 Regularization, Dropout, Inverted dropout, data augmentation, early stopping, normalizing inputs, vanishing/exploding gradients, weight initialization(Xavier initialization), gradient checking, mini-batch gradient descent, stochastic gradient descent loses speedup from vectorization, typical mini-batch sizes: 2^n, exponentially weighted averages(memory efficiency for calculating the average): V_t = beta\*V_(t-1)+(1-B)\*theta_t and V_t is approximately average over ~= 1/(1-beta) \*theta and the larger beta the smoother curve and epsilon = 1-beta and (1-epsilon)^(1/epsilon)=1/e. Bias correction: V_t/(1-beta^t). Gradient descent with momentum, hyper-parameters: alpha, beta. RMSprop. Adam(Adaptive Momentum estimation) optimization algorithm: combines momentum, RMS and bias correction. Learning rate decay. Tuning process(finding the most important hyper-parameters, coarse to find(find an important hyper-parameters area and focus on this area to choose dense hyper-parameters permutation), log scale(linear scale is bad because of the different sensitivity in some cases), re-test hyper-parameters occasionally in practice, babysitting one model(changing hyper-parameters after a period of time, like learning rate during training), training many models in parallel). Batch normalization(normalizing inputs to speed up learning, two more hyper-parameters: beta and gama(covariate shift, scale mean and variance), batch norm do not need parameter ‘b’ because it will be subtracted by the mean, slight regularization effect because of ‘slightly’ noisy mean and variance—>mini-batch. Batch norm at test time estimates by using exponentially weighted average during training because test case is not the mini-batch). Softmax regression(multi-classification, softmax regression generalizes logistic regression to C classes).Local optima in neural networks(saddle points, in high dimensions, most likely convex function in some directions and concave function in other directions) .The problem of plateaus(unlikely to get stuck in a bad local optima and plateaus can make learning slow). TensorFlow introduction & example.

12. Youtube, Weight Initialization explained | A way to reduce the vanishing gradient problem, deeplizard, https://www.youtube.com/watch?v=8krd5qKVw-Q ,Xavier initialization: glorot_normal hyper-parameter in kernel_initializer.

13. Medium, Activation Functions in Neural Networks, https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6 ,many linear activation functions in various layers can be combined into a single linear function(in this case, more layers do not means more complex neural networks, this is the reason why use non-linear activation functions). sigmoid(range from 0 to 1, can replace softmax during binary classification because sigmoid function is a special case of softmax function), tanh(range from -1 to 1), ReLU(Rectified Linear Unit, most used), Leaky ReLU, more activation functions: Binary Step, Logistic(a.k.a Soft Step), ArcTan, Parametric ReLU(PReLU), Exponential Linear Unit(ELU), SoftPlus.

![avator](https://github.com/RichardChangCA/AI_Study_Resources_Combo/blob/master/images/activation_functions.png)

14. Course3, Youtube, deeplearning.ai Andrew Ng, Structuring Machine Learning Projects(some advices for real world deep learning projects) https://www.youtube.com/watch?v=dFX8k1kXhOw&list=PLkDaE6sCZn6E7jZ9sN_xHwSHOdjUxUW_b&index=1 : precision/recall/F1-Score(harmonic mean of precision and recall), satisfying and optimizing metrics in real world, use much smaller validation and test set in modern very large dataset, set your test set to be big enough to give high confidence in the overall performance of your system. train+validation set is enough in some cases. Human level performance. Avoidable bias(training error - Bayes error). Human-level error as a proxy for Bayes error. error analysis. Deep learning algorithms are quite robust to random errors(randomly mislabeled examples) in the training set. The different distribution(data mismatch) between training and testing sets in practice(make training data more similar, or collect more data similar to dev/test sets, artificial data synthesis), training-dev set: same distribution as training set but not used for training, to evaluate the proportion of variance problem and different distribution problem. Testing error may be lower than training error mainly because the training set is much harder than testing set(human level error is different). Transfer learning(even small dataset works well, task A and B have the same input X, you have a lot more data for task A than task B, low level features from A could be helpful for learning B). Multitask learning(training on a set of tasks that could benefit from having shared lower-level features, usually amount of data you have for each task is quite similar, can train a big enough neural network to do well on all the tasks).  End-to-end deep learning(works well for large dataset). Pros and cons of end-to-end deep learning(Pros: let the data speak, less hand-designing of components needed. Cons: may need large amount of data, excludes potentially useful hand-designed components)

15. Medium, What is Gradient Accumulation in Deep Learning? https://towardsdatascience.com/what-is-gradient-accumulation-in-deep-learning-ec034122cfa ,small batch sizes may cause gradient fluctuation and gradient accumulation can tackle this problem. Run a number of steps without updating parameters and then accumulate these steps gradients to update variables. 

16. Medium, Label Smoothing & Deep Learning: Google Brain explains why it works and when to use (SOTA tips), https://medium.com/@lessw/label-smoothing-deep-learning-google-brain-explains-why-it-works-and-when-to-use-sota-tips-977733ef020 ,label smoothing is a loss function modification that can improve the performance of image classification, translation and speech recognition. Label smoothing forces neural networks to be less confident in their answers(not hard 0 and 1, 0.9 confident of 1). Not suitable for teacher model during knowledge distillation.

17. Medium, Intuitive Guide to Understanding KL Divergence, https://towardsdatascience.com/light-on-math-machine-learning-intuitive-guide-to-understanding-kl-divergence-2b382ca2b2a8 ,KL Divergence measures the how much a given arbitrary distribution is away from the true distribution. Lower the KL divergence value, the better we have matched the true distribution with our approximation. 

18. Medium, To See Is To Believe: Visualizing The Training Of Machine Learning Models, https://medium.com/skilai/to-see-is-to-believe-visualizing-the-training-of-machine-learning-models-664ef3fe4f49 ,training loss, validation loss, metrics growing plot

19. Medium, Artificial Intelligence vs. Machine Learning vs. Deep Learning(with audio version), https://towardsdatascience.com/artificial-intelligence-vs-machine-learning-vs-deep-learning-2210ba8cc4ac , AI includes ML, which includes DL. Deep Learning do not need feature extraction. 

20. Medium, Here Are My Top Resources to Learn Deep Learning, https://medium.com/datadriveninvestor/my-top-resources-to-learn-deep-learning-a14d1fc8e95a 

21. Medium, How to Prevent Overfitting in Machine Learning Models, https://medium.com/@sksoumik/how-to-prevent-overfitting-in-machine-learning-models-803f23bd9b8 ,reduce network size, cross-validation, add weight regularization(L1, L2-weight decay), removing irrelevant features, adding dropout, data augmentation

22. Medium, Deep Learning: Regularization Techniques to Reduce Overfitting, https://medium.com/analytics-vidhya/deep-learning-regularization-techniques-to-reduce-overfitting-e623c5900d97 L2-regularization, Dropout(only used on training, not used on testing), Data augmentation, Early stopping, Population Based Augmentation(more lite than Google AutoAugment) https://bair.berkeley.edu/blog/2019/06/07/data_aug/ 

23. Medium, Why I Switch From Keras to PyTorch, https://medium.com/swlh/why-i-switch-from-keras-to-pytorch-e48922f5846 ,PyTorch is Pythonic. The strength of PyTorch: debugging, amount of built-in datasets, performance. The strength of Keras/TensorFlow, class-based and sequential-based modelling(both), portability(Mobile), industry product use case.

24. Medium, Weights and Biases Sweep with Model Timeouts, https://medium.com/@kevin.horecka/weights-and-biases-sweep-with-model-timeouts-f81843e503f8 ,GitHub: https://github.com/kevroy314/wandb-sweeps-timeout ,tracking hyper-parameter tuning.

25. Medium, Multi-Label Image Classification with Neural Network | Keras, https://towardsdatascience.com/multi-label-image-classification-with-neural-network-keras-ddc1ab1afede ,activation function: replace softmax with sigmoid, loss function: from categorical_crossentropy to binary_crossentropy, data imbalanced problem.

26. Blog, A Beginner's guide to Deep Learning based Semantic Segmentation using Keras, https://divamgupta.com/image-segmentation/2019/06/06/deep-learning-semantic-segmentation-keras.html
SegNet: does not have any skip connections, no learnable parameters are used for upsampling, max unpooling(use position from pooling layer)

27. Blog, Learning through Auxiliary Tasks, https://vivien000.github.io/blog/journal/learning-though-auxiliary_tasks.html ,auxiliary learning tasks performed during training: one or several primary tasks, one or several auxiliary tasks; auxiliary learning tasks considered when assessing performance: primary tasks. Leveraging auxiliary tasks is an elegant way to improve learning, especially in the case of supervised learning with too few labelled examples or reinforcement learning with sparse rewards. However, auxiliary tasks may sometimes hurt the performance on the primary task(negative transfer).

28. Blog, A Beginner's guide to Deep Learning based Semantic Segmentation using Keras, https://divamgupta.com/image-segmentation/2019/06/06/deep-learning-semantic-segmentation-keras.html
SegNet: does not have any skip connections, no learnable parameters are used for upsampling, max unpooling(use position from pooling layer)

29. Medium, 5 YouTubers Data Scientists And ML Engineers Should Subscribe To, https://towardsdatascience.com/5-youtubers-data-scientists-and-ml-engineers-should-subscribe-to-e5bf5e2e9167 ,Data Science basic, Data Scientist career path, Paper illustration, AI-based real world projects, etc.

Medium, The Hitchhiker’s Guide to Feature Extraction, https://towardsdatascience.com/the-hitchhikers-guide-to-feature-extraction-b4c157e96631
