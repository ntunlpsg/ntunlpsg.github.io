+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Deep Learning for Crisis Computing"

# Project summary to display on homepage.
summary = "Python implementation of a number of deep neural networks classifiers for the classification of crisis-related data on Twitter."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "nn.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "representation-learning"]`
tags = ["misc"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# Optional featured image (relative to `static/img/` folder).
[header]
image = "nn.png"
caption = ""

+++

### About

[This repository](https://github.com/CrisisNLP/deep-learning-for-big-crisis-data) will host Python implementation of a number of deep neural networks classifiers
for the classification of crisis-related data on Twitter.

1. Requirementes:
        
        python 2.7
        numpy, scikit-learn
        keras, tensorflow or theano backend

2. Dataset and Pre-process
	A sample of tweet data (data/sample.csv) is a .csv format with three columns
	
        First, we need to pre-process tweets data: remove urls, special characters, lowercasing…
    
    	- python data_helpers/preprocess.py data/sample.csv
        
        Split pre-processed data (data/sample_prccd.csv) into train, test and dev part.
	
        - python data_helpers/split_data.py data/sample_prccd.csv
	  
3. Training a neural net model

	To train a classifier we create a folder containing links to train, test and dev part (data/nn_data)

	Folder embeddings/ includes word vector file, we provide our pre-trained crisis word vectors, we also can use Google word embedding here

	Folder dnn_scrips/ contains all neural nets models: CNN, RNN_LSTM, MLP…

	- bash run_cnn.sh to train a model with different parameters.

	See the results and training process in .log file

        Note that: if you do not have a GPU, you can run on CPU by change the theano flag to THEANO_FLAGS=mode=FAST_RUN,device=cpu,floatX=float32


### Publication


Dat Nguyen, Kamela Ali, Shafiq Joty, Hassan Sajjad, Muhammad Imran, and Prasenjit Mitra. Robust Classification of Crisis-Related Data on Social Networks Using Convolutional Neural Networks . In Proceedings of the Eleventh International Conference on Web and Social Media (ICWSM'17) , pages 632-635, 2017.

```
@InProceedings{nguyen-et-al-icwsm-17,
  author = {Dat Nguyen and Kamela Ali Al Mannai and Shafiq Joty and Hassan Sajjad and Muhammad Imran and Prasenjit Mitra},
  title = {Robust Classification of Crisis-Related Data on Social Networks Using Convolutional Neural Networks},
  booktitle = {Proceedings of the Eleventh International Conference on Web and Social
               Media},
  month     = {May},
  year      = {2017},
  series    = {ICWSM'17},
  address   = {Montr{\'{e}}al, Qu{\'{e}}bec, Canada},
  publisher = {AAAI},
  pages     = {xx--xx},
  url       = {papers/nguyen-et-al-icwsm-17.pdf},
  pages     = {632--635},
}
```


