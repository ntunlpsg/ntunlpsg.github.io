+++
# Date this page was created.
date = "2019-04-04"

# Project title.
title = "Unsupervised Word Translation"

# Project summary to display on homepage.
summary = "Adversarial Autoencoder with Cycle Consistency and Improved Training"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "word-translation.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["deep-learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# Optional featured image (relative to `static/img/` folder).
[header]
image = "word-translation.png"
caption = "Unsupervised Word Translation with Adversarial Autoencoder"

+++

### About
This resource contains the source code of our NAACL-HLT 2019 paper entitled [Revisiting Adversarial Autoencoder for Unsupervised Word Translation with Cycle Consistency and Improved Training](https://arxiv.org/pdf/1904.04116).
<br>
### Source code
[Link to source code](https://github.com/ntunlpsg/unsup-word-translation)

### Datasets
* [Conneau et al. (2018) Dataset](https://github.com/facebookresearch/MUSE/tree/master/data): Consists of FastText monolingual embeddings of 300 dimensions trained on Wikipedia monolingual corpus and gold dictionaries for 110 language pairs. 
* [Dinu-Artexe dataset](https://github.com/artetxem/vecmap/): Consists of monolingual embeddings of 300 dimension for English, Italian and Spanish. English and Italian embeddings were trained on WacKy corpora using CBOW, while the Spanish embeddings were trained on WMT News Crawl. 

### Citation

		@InProceedings{mohiuddin-joty-naacl-19,
		 title="{Revisiting Adversarial Autoencoder for Unsupervised Word Translation with Cycle Consistency and Improved Training}",
		 author={Tasnim Mohiuddin and Shafiq Joty},
		 booktitle = {Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
		 series    ={NAACL-HLT'19},
		 publisher={Association for Computational Linguistics},
		 address   = {Minneapolis, USA},
		 pages={xx--xx},
		 url = {},
		 year={2019}
		}

# Licence
Creative Commons Public Licenses.
