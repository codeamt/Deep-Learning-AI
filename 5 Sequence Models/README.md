<h1 align="center">DLAI-5: Sequence Models</h1>

<p align="center">
<img src="https://ucarecdn.com/e9905bea-68f5-49a6-a839-8816e42bc1bb/" width="70%" height="60%">
</p>

<h1 align="center">About the Course</h1>

In the [fifth and final course](https://www.coursera.org/learn/nlp-sequence-models) of the specialization, we explore Recurrent Neural Networks (RNNs) and training on sequences/time series data, where each record represents a single ***time step*** in the data sequence. In a sense, each value (time step) in a sequence of values (multiple time steps) acts as its own learning problem and undergoes linear regression to gain insights/generate a prediction for that specific time step in the series. 

Each time step inherits information from the previous time step to help generate a prediction and unlike previous architectures, with RNNs, activations and prediction outputs are calculated separately:

<p align="center">
<b>Simple Uni-directional RNN (where input and output equal the same length)</b><br>
<img src="https://ucarecdn.com/acb7e6f2-d67e-426f-99d0-edf2053facc7/" width="70%" height="60%">
</p>

Additionally, the way we learn with RNNs is different, too. Loss is calculated by summing the individual losses of each time step, and instad of backward passing in one reverse iteration, backward propagation also happens recursively through each time step. This variance of the gradient descent learning algorithm is called ***Back Propagation Through Time***: 
<p align="center">
<b>Back Propagation Through Time with a Simple Uni-directional RNN</b><br>
<img src="https://ucarecdn.com/4f65e189-ed44-4bfa-b480-cf72396b9fab/" width="70%" height="60%">
</p>


Potential use cases for RNNs include: 

  
  | Problem | Network |
| --- | --- |
| Speech Recognition | <img src="https://ucarecdn.com/ca77a526-c3e8-4e4b-a3b2-be7d1d7ae7f4/" width="300px" height="250px">|
| Music Generation | <img src="https://ucarecdn.com/a99fa010-48e4-4c44-8e08-239169a0914d/" width="300px" height="250px">|
| Sentiment Classification | <img src="https://ucarecdn.com/ed084d52-00b8-4b1a-aba2-8c16e7384891/" width="300px" height="250px">|
| Machine Translation | <img src="https://ucarecdn.com/85008935-2ff4-482a-87b1-7237f44ba6c8/" width="300px" height="250px">|


- DNA Sequence Analysis 
- Video Activity Recognition 
- Name Entity Recognition 
- Financial Series Forecasting 
- More 



## Lessons
- [x] Recurrent Neural Networks
- [x] Natural Language Processing & Word Embeddings
- [x] Sequence models & Attention mechanism

<p align="center">
<img src="https://ucarecdn.com/48d0c7e4-5cc3-4502-bf2b-76b2f2e47cbd/" width="60%" height="50%">
</p>

## Python Implementations

- [x] [Building a recurrent neural network: step by step](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/1%20RNNs/1-PA/README.md)
- [x] [Dinosaur Island - Character-Level Language Modeling](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/1%20RNNs/2-PA/README.md)
- [x] [Jazz improvisation with LSTM](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/1%20RNNs/3-PA/README.md)
- [x] [Operations on word vectors - Debiasing](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/2%20NLP%20and%20Word%20Embeddings/1-PA/README.md)
- [x] [Emojify](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/2%20NLP%20and%20Word%20Embeddings/2-PA/README.md)
- [x] [Neural Machine Translation with Attention](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/3%20Sequence%20Models%20and%20Attention%20Mechanism%20/1-PA/README.md)
- [x] [Trigger word detection](https://github.com/codeamt/Deep-Learning-AI/blob/master/5%20Sequence%20Models/Implementations/3%20Sequence%20Models%20and%20Attention%20Mechanism%20/2-PA/README.md)


## Additional Material

**Reviewed Research Papers:**

- [[1]](https://arxiv.org/pdf/1409.1259.pdf) Cho et al., 2014. *On the properties of neural machine translation: Encoder-decoder approaches*
- [[2]](https://arxiv.org/pdf/1412.3555.pdf) Chung et al., 2014. *Empirical Evaluation of Gated Recurrent Neural Network*
- [[3]](http://www.bioinf.jku.at/publications/older/2604.pdf) Hochreiter and Schmidchuber 1997. *Long short-term memory.* 
- [[4]](http://www.jmlr.org/papers/volume9/vandermaaten08a/vandermaaten08a.pdf) van der Marteen and Hinton., 2008. *Visualizing data using t-SNE.* 
- [[5]](https://www.aclweb.org/anthology/N13-1090) Mikolov et al., 2013. *Linguistic regularities in continuous space with representations*
- [[6]](http://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf) Bengio et al., 2003. *A neural probabilistic language model.*
- [[7]](https://arxiv.org/pdf/1301.3781.pdf) Mikolov et al., 2013. *Efficient estimation of word representation in vector space* 
- [[8]](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf) Mikolov et al., 2013. *Distributed representations of words and phrases and their compositionality* 
- [[9]](https://nlp.stanford.edu/pubs/glove.pdf) Pennington et al., 2014. *GloVe: Global vectors for word representations.* 
- [[10]](https://arxiv.org/pdf/1607.06520.pdf) Bolukbasi et al., 2016. *Man is to Computer Programmer as Woman is to Homemaker? Debiasing Word Embeddings?* 
- [[11]](https://arxiv.org/pdf/1409.3215.pdf) Sutskever et al., 2014. *Sequence to Sequence Learning with Neural Networks*
- [[12]](https://arxiv.org/pdf/1406.1078.pdf) Cho et al., 2014. *Learning Phrase Representations Using RNN Encoder-Decoder for Statistical Machine Translation*
- [[13]](https://arxiv.org/pdf/1412.6632.pdf) Mao et al., 2014. *Deep Captioning with Multimodal Recurrent Neural Network (m-RNN)*
- [[14]](https://arxiv.org/pdf/1411.4555.pdf) Vinyals et al., 2014. *Show and tell: Neural image captioning generator*
- [[15]](https://cs.stanford.edu/people/karpathy/cvpr2015.pdf) Karpathy and Fei Fei, 2015. *Deep Visual-Semantic Alignments for Generating Image Descriptions* 
- [[16]](https://www.aclweb.org/anthology/P02-1040.pdf) Papineni et al., 2002. *BLEU: a Method for Automatic Evaluation of Machine Translation*
- [[17]](https://arxiv.org/pdf/1409.0473.pdf) Bahdanau et al., 2014. *Neural Machine Translation by Jointly Learning to Align and Translate*
- [[18]](https://arxiv.org/pdf/1502.03044.pdf) Xu et al., 2015. *Show, Attend and Tell: Neural Image Caption Generation with Visual Attention*
- [[19]](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.75.6306&rep=rep1&type=pdf) Graves et al., 2006. *Connectionist Temporal Classification: Labeling Unsegmented Sequence Data with Recurrent Neural Networks*

