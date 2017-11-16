#FairSeq - Translator

A quick Tensorflow implementation of Facebook FairSeq[1] for character-level neural machine translation (EN -> JP). Notebooks for preprocessing, training, and testing are inside ```notebooks/```

1. ```Preprocessing.ipynb```

 1.1 Download English//Japanese parallel corpus from tatoeba.org.

 1.2 Extract EN and JP characters and create vocab lists.

 1.3 Convert all characters to token IDs and create training data file.

2. ```Train [GLU].ipynb``` -- defines and trains a Convolution sequence-to-sequence with multi-step attention, as defined in [1]. (support multi-GPUs training)

3. ```Test [GLU].ipynb``` -- for testing and visualizing model's attentions. EN-> JP translation is generated using beam search.

### TODOs
- mask zero-padded elements from attention
- proper weights init
- gradients scaling
- generate output in O(n) 

[1] Convolutional Sequence to Sequence Learning [https://arxiv.org/abs/1705.03122](https://arxiv.org/abs/1705.03122) 
