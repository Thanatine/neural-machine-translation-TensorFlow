# TensorFlow-Seq2Seq
Implement English-to-French Neural Machine Translation task by implenting seq2seq in TensorFlow 1.3.  

## Datasets
[Shared Task: Machine Translation of News, WMT 16](http://www.statmt.org/wmt16/translation-task.html)  
  
I took the English and French dataset in news-test2013 as training example.  
The hyperparameter and other details in codes are not yet tuned.  

## Requirements
* Python 3.5  
* TensorFlow 1.3  
* NLTK  

## Features
* Tokenization
* Padding (*EOS* in the end of encoder input; *GO* in the beginning of decoder input and *EOS* in the end)
* Vocabulary list building
* Autoencoder/encoder-decoder in multi-RNN-layers  
* Attention mechanism (Luong's)  
* Batch-training process  
* Beamsearch/basic inference decoder  

## Features In Progress
* Bidirectional encoder  
* BLEU score metrics  
* Bucketing (Optional. Because TensorFlow's dynamic_decode doesn't require fixed length input anymore)  

## Usage
Import *mySeq2Seq.py* to have *Seq2SeqModel* class.  
You may refer to *train.ipynb* for the training process and data flow.

## Reference
[Massive Exploration of Neural Machine Translation Architectures](https://arxiv.org/abs/1703.03906)  
[TensorFlow / nmt](https://github.com/tensorflow/nmt)  
[JayParks / tf-seq2seq](https://github.com/JayParks/tf-seq2seq)  
