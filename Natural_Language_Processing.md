1. Youtube, Automatic image captioning: https://www.youtube.com/watch?v=yk6XDFm3J2c ,this presentation combines CNN and RNN(especially LSTM), given image inputs, generating natural languages as outputs. Although this presentation was published in 2015, the idea behind image captioning is not outdated.

2. Medium, Illustrated self-attention: https://towardsdatascience.com/illustrated-self-attention-2d627e33b20a ,the basic idea behind Transformer, Bert and etc. in NLP. This idea replaced the RNN family to extract whole sentence words together.

3. Medium, Illustrated Attention: https://towardsdatascience.com/attn-illustrated-attention-5ec4ad276ee3 , a good article, including attention mechanism, score function

- seq2seq

- seq2seq + attention

- seq2seq with bidirectional encoder + attention

- seq2seq with 2-stacked encoder + attention

- GNMT(Google Neural Machine Translation) — seq2seq with 8-stacked encoder (+bidirection+residual connections) + attention

4. Medium, Image Captioning with Keras, https://towardsdatascience.com/image-captioning-with-keras-teaching-computers-to-describe-pictures-c88a46a311b8 ,How to Prepare a Photo Caption Dataset for Training a Deep Learning Model, https://machinelearningmastery.com/prepare-photo-caption-dataset-training-deep-learning-model/ , cnn+rnn+transfer learning

5. Medium, The Mechanics of Attention Mechanism in Flowcharts: https://towardsdatascience.com/the-mechanics-of-attention-mechanism-f6e9805cca66 ,the attention mechanism in machine translation, attention mechanism can obtain the context of whole original text information to help translate into another language. two version attention: soft(softmax function, focus on a large scope with various weights), hard(max function, only focus on the most important word), soft attention performs better than hard attention in most cases probably because soft attention can be differentiable. the attention for each pair of words can be visualized.

6. Youtube, attention is all you need, https://www.youtube.com/watch?v=iDulhoQ2pro&t=941s ,the self-attention mechanism in natural language processing, especially in SOTA models, like bert, transformer, xlnet. the idea is also used in computer vision, like self-attention GAN, self-attention unet etc. There are three basic concepts in self-attention: key, value, and query(K,V,Q), key and value pairs are generated from input sentences(original sentences in machine translation), and query is generated from the previous words before the next predicting word in output sentences. After that, key and query do a dot-product to calculate the similarity between inputs and outputs(a.k.a finding the attention between inputs and outputs), and then use softmax to choose the best value for the next word prediction. The most important difference between attention and self-attention is that: (1. attention needs more parameters to store the attention values(a.k.a others supervise you) (2. self-attention can only use inputs and part of outputs theirselves to know where they should pay "closer" attention, no more parameters needed(a.k.a you has self-displine)

