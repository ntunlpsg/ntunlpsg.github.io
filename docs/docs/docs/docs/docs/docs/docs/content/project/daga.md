+++
# Date this page was created.
date = 2021-02-24

# Project title.
title = "DAGA: Data Augmentation with a Generation Approach for Low-resource Tagging Tasks"

# Project summary to display on homepage.
summary = "Data augmentation for low resource tagging."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = ""

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "graphical-model"]`
tags = ["deep-learning"]

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

[Github](https://github.com/ntunlp/daga)

# DAGA
This is the source code of our method proposed in paper "[DAGA: Data Augmentation with a Generation Approach for Low-resource Tagging Tasks](https://www.aclweb.org/anthology/2020.emnlp-main.488/)" accepted by EMNLP 2020.

# Examples 
## flair\_seq\_tagger: sequense tagging model
```
cd flair_seq_tagger;

python train_tagger.py \
  --data_dir PATH/TO/TRAIN_DIR \
  --train_file  train.txt \
  --dev_file  dev.txt \
  --data_columns text ner \
  --model_dir ./model \
  --comment_symbol "__label__" \
  --embeddings_file PATH/TO/emb \
  --optim adam \
  --learning_rate 0.001 --min_learning_rate 0.00001 \
  --patience 2 \
  --max_epochs 100 \
  --hidden_size 512 \
  --mini_batch_size 32 \
  --gpuid 0
```

## lstm-lm: LSTM language model
- train lstm-lm on linearized sequences
```
cd lstm-lm;

python train.py \
  --train_file PATH/TO/train.linearized.txt \
  --valid_file PATH/TO/dev.linearized.txt \
  --model_file PATH/TO/model.pt \
  --emb_dim 300 \
  --rnn_size 512 \
  --gpuid 0 
```

- generate linearized sequences
```
cd lstm-lm;

python generate.py \
  --model_file PATH/TO/model.pt \
  --out_file PATH/TO/out.txt \
  --num_sentences 10000 \
  --temperature 1.0 \
  --seed 3435 \
  --max_sent_length 32 \
  --gpuid 0
```

## tools: tools for data processing
- preprocess.py: sequence linearization
- line2cols.py: convert linearized sequence back to two-column format

# Requirements
- flair\_seq\_tagger/requirements.txt
- lstm-lm/requirements.txt

# Citation
Please cite our paper if you found the resources in this repository useful.
```
@inproceedings{ding-etal-2020-daga,
    title = "{DAGA}: Data Augmentation with a Generation Approach for Low-resource Tagging Tasks",
    author = "Ding, Bosheng  and
      Liu, Linlin  and
      Bing, Lidong  and
      Kruengkrai, Canasai  and
      Nguyen, Thien Hai  and
      Joty, Shafiq  and
      Si, Luo  and
      Miao, Chunyan",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
    month = nov,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.emnlp-main.488",
    doi = "10.18653/v1/2020.emnlp-main.488",
    pages = "6045--6057",
}
```
