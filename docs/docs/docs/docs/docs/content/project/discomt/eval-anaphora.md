+++
# Date this page was created.
date = "2019-10-30"

# Project title.
title = "Evaluating Pronominal Anaphora in Machine Translation: An Evaluation Measure and a Test-suite"

# Project summary to display on homepage.
summary = "An extensive, targeted dataset that can be used as a test suite for pronoun translation, covering multiple source languages and different pronoun errors drawn from real system translations, for English"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = ""

# Tags: can be used for filtering projects.
# Example: `tags = ["representation-learning"]`
tags = ["representation-learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""
highlight = false
# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = ""
caption = ""

+++

This repository contains the data and source code of our paper "[Evaluating Pronominal Anaphora in Machine Translation: An Evaluation Measure and a Test-suite](https://arxiv.org/abs/1909.00131)" in EMNLP-IJCNLP 2019.


### Prerequisites

```
* PyTorch 0.4 or higher
* Python 3
* AllenNLP
* SQLite3
```

### Datasets - Training/Development/Testing
The training data consists of system translations vs. reference text from WMT 2011-15. There are two versions of the development data: one with unique system translations vs. reference, and one with unique noisy sentences vs. reference. Both are from WMT2014. The test data is the data used for the user studies in French, German, Russian and Chinese. Both the original database and the processed pickle files are provided.

Development and test data are uploaded here. The training data and a trained model are available at the following link: https://www.dropbox.com/sh/ol66hb2t3jcdeny/AADrfqm7fH1Cq8uiIvzcUuUra?dl=0

## How To Run
You can use your own data from any other MT translations to train the evaluation measure. For training, ensure that the pickle file is serialized (each dictionary sample is written individually) and contains the data required; alternately, you can make corresponding changes in the code. Other paramaters can also be changed in `train.py`.

* Training: <br>
```
python train.py [training_data] [dev_data]
```


* Testing: <br>
```
python test_trained_model.py [model] [test_data]
```

## User Study
Both the study data and the anonymized user responses for each language are provided. The Chinese/English data is separated; both these studies use the same data (English study done without source language) for comparison. The pickle file `pronoun_pair_list.pkl` contains the pronoun pairs of reference and error pronouns after filtering based on agreement (agreements and counts of responses included). 

### Test Suite
The sqlite3 database with the pronoun test suite contains all the samples for all source languages from WMT2011-2017; filter by source language as required. Among other data, each sample provides the source sentence and two previous sentences for context, the equivalent for reference, and also which system translation error it originated from. This test suite is not filtered by the results of the user study to keep it unrestricted; if required, use the pronoun pairs from the keys in the `pronoun_pair_list.pkl` dictionary file, and filter using the `reference_pronoun` and `system_pronoun` fields. 

codes are available [here](https://github.com/ntunlp/eval-anaphora).

## Citation
Please cite our paper if you found the resources in this repository useful.
```
@inproceedings{EvalAnaphora,
  title={Evaluating Pronominal Anaphora in Machine Translation: An Evaluation Measure and a Test Suite},
  author={Prathyusha Jwalapuram and Shafiq Joty and Irina Temnikova and Preslav Nakov},
  booktitle={EMNLP-IJCNLP},
  year={2019}

}	
```

