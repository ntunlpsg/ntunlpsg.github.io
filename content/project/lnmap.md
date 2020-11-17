+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "LNMap: Departures from Isomorphic Assumption in Bilingual Lexicon Induction Through Non-Linear Mapping in Latent Space"

# Project summary to display on homepage.
summary = "This paper shows with a semi-supervised algorithm that BLI is more suitable through Non-Linear Mapping (specially for low resource languages)."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "lnmap.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "representation-learning"]`
tags = ["deep-learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""
highlight = false
# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "lnmap.png"
caption = ""

+++


This resource contains the source code of our EMNLP-2020 paper entitled [LNMap: Departures from Isomorphic Assumption in Bilingual Lexicon Induction Through Non-Linear Mapping in Latent Space](https://www.aclweb.org/anthology/2020.emnlp-main.215/).

<p align="center">
<img src="https://taasnim.github.io/img/lnmap/model.png" width="800">
</p>

--------------------------------------------------------------------------------

### Source code
[Link to source code](https://github.com/taasnim/lnmap)

### Datasets
* [Conneau et al. (2018) Dataset](https://github.com/facebookresearch/MUSE/tree/master/data): Consists of FastText monolingual embeddings of 300 dimensions trained on Wikipedia monolingual corpus and gold dictionaries for 110 language pairs.
* [Dinu-Artexe dataset](https://github.com/artetxem/vecmap/): Consists of monolingual embeddings of 300 dimension for English, Italian and Spanish. English and Italian embeddings were trained on WacKy corpora using CBOW, while the Spanish embeddings were trained on WMT News Crawl.



## Citation
Please cite our paper if you found the resources in this repository useful.
```bibtex
@inproceedings{mohiuddin-etal-2020-lnmap,
    title = "{LNM}ap: Departures from Isomorphic Assumption in Bilingual Lexicon Induction Through Non-Linear Mapping in Latent Space",
    author = "Mohiuddin, Tasnim  and
      Bari, M Saiful  and
      Joty, Shafiq",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing (EMNLP)",
    month = nov,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.emnlp-main.215",
    pages = "2712--2723"
}
```

