+++
# Date this page was created.
date = "2021-05-01"

# Project title.
title = "RST Parsing from Scratch"

# Project summary to display on homepage.
summary = "A novel top-down end-to-end formulation of document level discourse parsing in the Rhetorical Structure Theory (RST) framework."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "naacl21-rst-parsing-model.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["discourse-analysis", "seq2seq", "parser"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# put a link to your preferred image that will be the banner of the page.
[header]
image = "naacl21-rst-parsing-model.png"
caption = ""

+++


# RST Parsing from Scratch
This repository contains the source code of our paper [RST Parsing from Scratch](https://arxiv.org/abs/2105.10861) in NAACL 2021.
## Requirements
* `python`: 3.7
* `pytorch`: 1.4
* `transformers`: 3.0

## Usage

To train a discourse parser:

    ./*_train.sh
    
To predict discourse tree:
 
    ./*_predict.sh

## Data Format

* For end-to-end parsing from scratch (no sentence guidance): 
we need to create the data with dummy edu_break and doc_structure. Refer to `create_sample_dummy_format_data.py` and `dummy_format_data/sample_rawtext_data_format`
* For other parsing models:
Refer to `create_sample_dummy_format_data.py` and `dummy_format_data/sample_full_data_format`
  
## Citation
Please cite our paper if you found the resources in this repository useful.

    @inproceedings{nguyen-etal-2021-rst-scratch,
    title = "RST Parsing from Scratch",
    author = "Nguyen, Thanh-Tung  and
      Nguyen, Xuan-Phi  and
      Joty, Shafiq  and
      Li, Xiaoli",
    booktitle = "Proceedings of the 2021 Conference of the North {A}merican Chapter 
    of the Association for Computational Linguistics: Human Language Technologies, 
    Volume 1 (Long and Short Papers)",
    month = jun,
    year = "2021",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://arxiv.org/abs/2105.10861",
    doi = "",
    pages = "xx--xx",}
    }	
