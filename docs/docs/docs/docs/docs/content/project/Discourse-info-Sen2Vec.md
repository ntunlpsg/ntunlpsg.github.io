+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Discourse-informed Sen2Vec"

# Project summary to display on homepage.
summary = "CON-S2V: A Generic Framework for Incorporating"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "sen2vec.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "representation-learning"]`
tags = ["representation-learning","discourse"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# Optional featured image (relative to `static/img/` folder).
[header]
image = "sen2vec.png"
caption = ""

+++

### About

This resource contains the source code of [CON-S2V: A Generic Framework for Incorporating Extra-Sentential Context into Sen2Vec Latent Representation for the sentences.](https://raihanjoty.github.io/papers/saha-joty-hasan-ecml-17.pdf) paper.
 

### Source code

[Link to source code](https://github.com/tksaha/con-s2v/tree/jointlearning)

### Requirements
* [Anaconda with Python 3.5](https://www.continuum.io/downloads)
* [ROUGE-1.5.5](http://www.berouge.com/Pages/DownloadROUGE.aspx)

### Python Environment setup and Update

1. Copy the sen2vec_environment.yml file into anaconda/envs folder
2. Get into anaconda/envs folder.
3. Run the following command:

```
conda env create -f sen2vec_environment.yml
```

Now, you have successfully installed sen2vec environment and now you can activate the environment using the following command. 

```
source activate sen2vec
```


If you have added more packages into the environment, you 
can update the .yml file using the following command: 

```
conda env export > sen2vec_environment.yml
```

### ROUGE Environment setup
Please go to the ROUGE directory and run the following command to check whether 
the provided perl script will work or not:
```
./ROUGE-1.5.5.pl 
```

If it shows the options for running the script, then you are fine. However, if it shows 
you haven't have XML::DOM installed then please type following command to install 
it: 

```
cpan XML::DOM
```
Here, CPAN stands for Comprehensive Perl Archive Network. 

### Database Creation and update 

If you have already installed [postgresql](http://postgresapp.com/), then 
you can create a table with the following command for the newsgroup [news] dataset: 

```
psql -c "create database news"
```

After creating the database, use pg_restore to create the schemas which is agnostic to 
the dataset: 

```
pg_restore --jobs=3 --exit-on-error --no-owner --dbname=news sql_dump.dump
```

or 
```
pg_restore --jobs=3 -n public --exit-on-error --no-owner --dbname=news sql_dump.dump
```

We are assuming that either you are using `postgres` as the username or any other username
which already has all the required privileges. To change the password for the `postgres` user,
use the following command-

```
psql -h localhost -d news -U postgres -w
\password
```

If you have made any changes to the database, you can updated the dump 
file using following command (schema only): 

[You may need to set peer authentication: [Peer authentication](http://stackoverflow.com/questions/10430645/how-can-i-get-pg-dump-to-authenticate-properly)]

```
sudo -u postgres pg_dump -s --no-owner -FC news >sql-dump.dump 
```

To dump the data of a particular table from the database: 
```
sudo -u postgres pg_dump --data-only -t summary news --no-owner -Fc > news_summary.dump
```

### Setting Environment Variables

Set the dataset folder path and the connection string in the environment.sh file properly and 
then run the following command-

```
source environment.sh #Unix, os-x
```

### Creating Executable for Word2Vec (Mikolov's Implementation)
Please go to the word2vec code directory inside the project and 
type the following command for creating executable:

```
make clean
make
```

### Installation of Theano for Skip-Thought
```
pip install theano
sudo apt install nvidia-cuda-toolkit
```

### Installation of Keras (Sequential API)
```
pip install keras
```

To change the backend to ``theano`` please change the default configuration 
in ~/.keras/keras.json

```
{
    "image_dim_ordering": "tf",
    "epsilon": 1e-07,
    "floatx": "float32",
    "backend": "theano"
}
```

### Downloading the {C-PHRASE} vectors:
Please download the C-Phrase vectors from [C-Phrase link] (http://clic.cimec.unitn.it/composes/cphrase-vectors.html) and 
join the files using following commands:

```
cat cphrase.txt.zip_* > cphrase.txt.zip 
sed -i  '1 i\174814 300'  cphrase.txt  # converting into word2vec format
```

### Downloading GLove Pretrained Vectors for SDAE:
Please download the vectors from [Glove link] (http://nlp.stanford.edu/projects/glove/) and then append 
a line in the first line using following command:

```
sed -i '1 i\400000 300' glove.6B.300d.txt
```


### Running the Project 
Run sen2vec with -h argument to see all possible options:

```
python sen2vec -h
usage: sen2vec [-h] -dataset DATASET -ld LD

Sen2Vec

optional arguments:
  -h, --help            show this help message and exit
  -dataset DATASET, --dataset DATASET
                        Please enter dataset to work on [reuter, news]
  -ld LD, --ld LD       Load into Database [0, 1]
  
  -pd PD, --pd PD       Prepare Data [0, 1]
  
  -rbase RBASE, --rbase RBASE       Run the Baselines [0, 1]
  
  -gs GS, --gs GS       Generate Summary [0, 1]
```

For example, you can run for the news dataset using the following command-

```
python sen2vec -dataset news -ld 1 -pd 1 -rbase 1 -gs 1
```

### Publications

Tanay Saha, Shafiq Joty, Naeemul Hassan, and Mohammad Hasan. Regularized and Retrofitted models for Learning Sentence Representation with Context . In Proceedings of the 26th ACM International Conference on Information and Knowledge Management (CIKM'17) , pages xx-xx, 2017.

```
@InProceedings{saha-joty-hassan-hasan-cikm-17,
  author    = {Tanay Saha and Shafiq Joty and Naeemul Hassan and Mohammad Hasan},
  title     = {Regularized and Retrofitted models for Learning Sentence Representation with Context},
  booktitle = {Proceedings of the 26th ACM International Conference on Information and Knowledge Management},
  month     = {November},
  year      = {2017},
  series    = {CIKM'17},
  address   = {Singapore},
  publisher = {ACM},
  pages     = {xx--xx},
  url       = {papers/saha-joty-hassan-hasan-cikm-17.pdf},
}
```
---
Tanay Kumar Saha, Shafiq Joty, Mohammad Al Hasan. CON-S2V: A Generic Framework for Incorporating Extra-Sentential Context into Sen2Vec. In Proceedings of the European Conference on Machine Learning (ECML-PKDD-2017), Macedonia, Skopje, 2017

```
@InProceedings{saha-joty-hasan-ecml-17,
  author    = {Tanay Saha and Shafiq Joty and Mohammad Hasan},
  title     = {CON-S2V: A Generic Framework for Incorporating Extra-Sentential Context into Sen2Vec},
  booktitle = {Proceedings of The European Conference on Machine Learning & 
Principles and Practice of knowledge discovery in databases},
  month     = {September},
  year      = {2017},
  series    = {ECML-PKDD'17},
  address   = {Macedonia, Skopje},
  publisher = {Springer},
  pages     = {xx--xx},
  url       = {papers/saha-joty-hasan-ecml-17.pdf}
```




