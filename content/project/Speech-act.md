+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Speech act recognizer for synchronous and asynchronous conversations"

# Project summary to display on homepage.
summary = "This resource addresses the problem of speech act recognition in written asynchronous conversations"

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "speech_act.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "graphical-model"]`
tags = ["discourse"]

# Optional external URL for project (replaces project detail page).
external_link = ""
highlight = false
# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "speech_act.png"
caption = ""

+++


### About
This resource includes,

- A bi-directional LSTM for speech act recognition (theano, keras)
- A global CRF model for thread-level inference (Matlab)
- Tensorflow implementation of all the models presented in the Journal version.
- Tensorflow implementation of all the models presented in the NAACL-HLT 2019 paper.
- **A web demo**.

### Related publications
- Shafiq Joty and Enamul Hoque. 2016. *Speech Act Modeling of Written Asynchronous Conversations with Task-Specific Embeddings and Conditional Structured Models*. In Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics (ACL-2016) , Berlin, Germany. [[PDF](http://alt.qcri.org/~sjoty/paper/speech-act-acl-16.pdf)]


```
@inproceedings{joty-hoque-acl-16,
  Author = {Shafiq Joty and Enamul Hoque},
  Booktitle = {Proceedings of the 54th Annual Meeting of the Association for Computational Linguistics},
  Numpages = {9},
  pages = {1746--1756},
  Title = {Speech Act Modeling of Written Asynchronous Conversations with Task-Specific Embeddings and Conditional Structured Models},
  address   = {Berlin, Germany},
  Series = {ACL'16},
  Publisher = {ACL},
  url = {papers/joty-hoque-acl-16.pdf},
  Year = {2016}
} 
```

---

- Shafiq Joty and Tasnim Mohiuddin. *Speech Act Modeling of Written Asynchronous Conversations: A Neural CRF Approach*. In Computational Linguistics (Special Issue on Language in Social Media, Exploiting discourse and other contextual information) : Volume 44 | Issue 4 | December 2018 | pages (859-894). [[PDF](https://www.mitpressjournals.org/doi/pdf/10.1162/coli_a_00339)]

```
@article{joty-cl-si-18,
  title="{Speech Act Modeling of Written Asynchronous Conversations: A Neural CRF Approach}",
  author={Shafiq Joty and Tasnim Mohiuddin},
  journal = {Computational Linguistics (Special Issue on Language in Social Media, Exploiting discourse and other contextual information)},
  publisher={MIT Press},
  issue={4},
  pages={859-894},
  year={2018},
  url = {https://www.mitpressjournals.org/doi/full/10.1162/coli_a_00339}
}
```


- Tasnim Mohiuddin and Thanh-Tung Nguyen and Shafiq Joty. 2019. *Adaptation of Hierarchical Structured Models for Speech Act Recognitionin Asynchronous Conversation*. In Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Minneapolis, USA. [[PDF](https://arxiv.org/pdf/1904.04021.pdf)]


```
@InProceedings{mohiuddin-nguyen-joty-naacl-19,
     title="{Adaptation of Hierarchical Structured Models for Speech Act Recognitionin Asynchronous Conversation}",
     author={Tasnim Mohiuddin and Thanh-Tung Nguyen and Shafiq Joty},
     booktitle = {Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
     series    ={NAACL-HLT'19},
     publisher={Association for Computational Linguistics},
     address   = {Minneapolis, USA},
     pages={xx--xx},
     url = {},
     year={2019}
} 
```


### Download
- [Data - QC3 and BC3 ](http://alt.qcri.org/tools/speech-act/corpus.zip) We do not release other datasets (MRDA, SWBD, TA) for license issues
- [ Conversational Word Embeddings](https://entuedu-my.sharepoint.com/:f:/g/personal/mohi0004_e_ntu_edu_sg/EsjZMPnoYsRIvqzjSA-rGg8BDm-hlAvT6DQSWxFuudYVWA?e=8x054k)
<!--- - [Code (drafty)](http://alt.qcri.org/tools/speech-act/code.zip)-->
- [Code: ACL-16 (theano, keras, Matlab)](http://alt.qcri.org/tools/speech-act/code.zip)
- [Code: CL Journal (Tensorflow)](https://github.com/ntunlpsg/speech-act)
- [Code: NAACL-HLT 2019 (Tensorflow)](https://github.com/ntunlpsg/speech-act-hierarchical)


# License
The speech act recognizer is an Open Source Software, and is released under the Common Public License. You are welcome to use the code under the terms of the licence for research purposes ONLY, however please acknowledge its use with a citation.

### Demo
**Currently only accessible inside ntu network.**
The demo can take a paragraph of sentences and predicts speech-act for each of the sentences.

<form action="http://172.21.144.214:4200/">
    <input type="submit" value="The link of the demo" />
</form>
