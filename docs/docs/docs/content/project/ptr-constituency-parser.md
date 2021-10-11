+++
# Date this page was created.
date = ""

# Project title.
title = "Efficient Constituency Parsing by Pointing"

# Project summary to display on homepage.
summary = "This resource contains the source code of our ACL-2020 paper entitled [Efficient Constituency Parsing by Pointing](https://arxiv.org/abs/2006.13557)"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = ""

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["parser"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# put a link to your preferred image that will be the banner of the page.
[header]
image = "ptr-const-paser.png"
caption = "Model of Pointing Constituency Parser"

+++


# Efficient Constituency Parsing by Pointing
This resource contains the source code of our ACL-2020 paper entitled [Efficient Constituency Parsing by Pointing](https://arxiv.org/abs/2006.13557)


# Source code

[Code](https://github.com/tungngthanh/ptr-constituency-parser)


# Running Experiments
For english parsing, run command 

`bash ./run_en.sh`

For other parsing, run command 

`bash ./run_spmrl.sh`


# Citation
Please cite our paper if you found the resources in this repository useful.
```
@inproceedings{nguyen-etal-2020-efficient,
    title = "Efficient Constituency Parsing by Pointing",
    author = "Nguyen, Thanh-Tung  and
      Nguyen, Xuan-Phi  and
      Joty, Shafiq  and
      Li, Xiaoli",
    booktitle = "Proceedings of the 58th Annual Meeting of the Association for Computational Linguistics",
    month = jul,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.acl-main.301",
    pages = "3284--3294",
}
```
