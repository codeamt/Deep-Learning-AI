<h1 align="center">DLAI-5: Sequence Models</h1>

<p align="center">
<img src="https://ucarecdn.com/e9905bea-68f5-49a6-a839-8816e42bc1bb/" width="70%" height="60%">
</p>

<h1 align="center">About the Course</h1>

In the [fifth and final course](https://www.coursera.org/learn/nlp-sequence-models) of the specialization, we explore Recurrent Neural Networks (RNNs) and training on sequences/time series data, where each input (x) chains together several ***time steps***. Temporal in structure, each time step in a sequence of time steps acts as its own learning problem and undergoes linear regression to gain insights/generate a prediction that gets carried over as input for the next step. 

<p align="center">
<b>Simple Uni-directional RNN (where input and output equal the same length)</b><br>
<img src="https://ucarecdn.com/acb7e6f2-d67e-426f-99d0-edf2053facc7/" width="70%" height="60%">
</p>

The above illustration could already be considered a deep RNN, but to solve more complex problems, architectures can often treat these individual RNNs as layers of an even *deeper* RNN. 

The way we learn with RNNs is different, too. Loss is calculated by summing the individual losses from all the time steps, and instead of backward passing in one reverse iteration, backward propagation happens recursively through each time step. 

This variance of gradient descent is called ***Back Propagation Through Time***: 

<p align="center">
<b>Back Propagation Through Time with a Simple Uni-directional RNN</b><br>
<img src="https://ucarecdn.com/0d4d15af-5828-47a8-9067-c7b3bb170291/" width="70%" height="60%">
</p>

With sequence models, the number of inputs don't always match the number of outputs. The architecture of your RNN depends on the problem you might be trying to solve. For example, below in the table are some popular sequence model problems and their corresponding RNN architectures: 

<table >
 <tr>
   <th width="40%">Problem</th><th width="60%">Network</th>
  </tr>
<tr>
  <td>Speech Recognition</td><td><img src="https://ucarecdn.com/ca77a526-c3e8-4e4b-a3b2-be7d1d7ae7f4/" width="30%" height="100px"></td>
</tr>
<tr>
  <td>Music Generation</td><td><img src="https://ucarecdn.com/a99fa010-48e4-4c44-8e08-239169a0914d/" width="30%" height="100px"></td>
</tr>
<tr>
  <td>Sentiment Classification</td><td><img src="https://ucarecdn.com/ed084d52-00b8-4b1a-aba2-8c16e7384891/" width="30%" height="100px"></td>
</tr>
<tr>
  <td>Machine Translation</td><td><img src="https://ucarecdn.com/85008935-2ff4-482a-87b1-7237f44ba6c8/" width="30%" height="100px"></td>
</tr>
</table>

As explained in previous courses, the deeper the network, the more adverse the effect on the network's memory (e.g., the vanishing gradient problem, where derivatives decrease exponentially). With natural language processing, for example, a simple RNN would have a hard time memorizing word tenses for word analysis further down the sentence sequence. To address the vanishing gradient issue, RNNs have more sophisticated neurons that help capture long-range dependencies: 


<p align="center">
<img src="https://ucarecdn.com/e73e4014-4bb7-45e2-adee-295f30a40522/" width="70%" height="60%">
</p>
<br>

And: 
<br>
<p align="center">
<img src="https://ucarecdn.com/6e5e9f94-51a6-4837-a7c1-2910797fcc7b/" width="70%" height="60%">
</p>
<br>

Both units utilize memory cells and various gates to set/reset state that then matriculates through the RNN's time steps to assist in making better associations down the way. GRUs are a more recent innovation and can sometimes outperform LSTMs with smaller data sets because of their simplicity but LSTMs outperform when it comes to memorizing exceedingly long-range connections. Ultimately, the choice of neuron is highly contingent upon the nature of the problem and the amount of data available. 

Perhaps most notable about RNNs is the ability to perform bi-directional propagation to gain insight from future and past data simultaneously and learn problems faster:

<p align="center">
<img src="https://ucarecdn.com/7848ad58-9995-4ae9-978a-5c0b2a533bab/" width="70%" height="60%">
</p>

After walking us through all the theory and associated formulas for calculating key parameters, Professor Ng then introduces us to Natural Language Processing, where we dive deep into language modeling; that is, tokenizing a glossary of terms (a ***corpus***), modeling those words with one-hot vectors, featurizing those vectors with word embeddings for application use cases (like sentiment classification) and strategies for minimizing bias transposition.

Finally, in the third and final week of the course, we explore Sequence to Sequence modeling and how encoder and decoder networks in (1) a one-to-many architecture and (2) a many-to-many architecture can work in tandem with the beam search algorithm to achieve outcomes like image captioning and machine translation or speech recognition, respectively.

This final time step in a series of courses also provided a host of programming assignments (linked below) that offered the opportunity to implement algorithms from notable research papers and solidify understanding about the most robust area of deep learning discussed in the specialization. 

I'm incredibly grateful to Andrew Ng and the deeplearning.ai staff for putting together this program! 

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

