+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Topic Segmenter & Labeler for Asynchronous Conversations"

# Project summary to display on homepage.
summary = "This parser builds a discourse tree by applying an optimal parsing algorithm to probabilities inferred from two Conditional Random Fields: one for intra-sentential parsing and the other for multi-sentential parsing. "

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "fqg.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "representation-learning"]`
tags = ["discourse"]

# Optional external URL for project (replaces project detail page).
external_link = ""
highlight = false
# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "fqg.png"
caption = ""

+++

### Topic Segmentation and Labeling in Asynchronous Conversations

Topic segmentation and labeling is often considered a prerequisite for higher-level conversation analysis and has been shown to be useful in many Natural Language Processing (NLP) applications. We present two new corpora of email and blog conversations annotated with topics, and evaluate annotator reliability for the segmentation and labeling tasks in these asynchronous conversations. We propose a complete computational framework for topic segmentation and labeling in asynchronous conversations. Our approach extends state-of-the-art methods by considering a fine-grained structure of an asynchronous conversation, along with other conversational features by applying recent graph-based methods for NLP. For topic segmentation, we propose two novel unsupervised models that exploit the fine-grained conversational structure, and a novel graph-theoretic supervised model that combines lexical, conversational and topic features. For topic labeling, we propose two novel (unsupervised) random walk models that respectively capture conversation specific clues from two different sources: the leading sentences and the fine-grained conversational structure. Empirical evaluation shows that the segmentation and the labeling performed by our best models beat the state-of-the-art, and are highly correlated with human annotations.

### Source code

Download:

* [Topic Segmenter(LCSEG+FQG) and Labeler v1 [120 MB] (tested on windows)](http://www.cs.ubc.ca/cs-research/lci/research-groups/natural-language-processing/topic/topic_model.zip)
* [Topic Segmenter(LCSEG+FQG) and Labeler v2 [126 MB] (tested on Linux Matlab R2012A 64 bit)](http://www.cs.ubc.ca/cs-research/lci/research-groups/natural-language-processing/topic/topic_model[linux64].zip)

### Publications
---
S. Joty, G. Carenini and R. T. Ng (2013) Topic Segmentation and Labeling in Asynchronous Conversations  JAIR, Volume 47, pages 521-573 (2013) [[PDF](https://www.jair.org/media/3940/live-3940-7166-jair.pdf)].

```
@article{joty-carenini-ng-jair-13,
    author = {Shafiq Joty and Giuseppe Carenini and Raymond Ng},
    title = {{Topic Segmentation and Labeling in Asynchronous Conversations}},
    journal = {Journal of Artificial Intelligence Research},
    year = {2013},
    pages     = {521--573},
    volume = {47},
    url       = {https://www.jair.org/media/3940/live-3940-7166-jair.pdf},
}
```
---
Yashar Mehdad, Giuseppe Carenini, Raymond Ng and Shafiq Joty. Towards Topic Labeling with Phrase Entailment and Aggregation. In Proceedings of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL-HLT 2013), Atlanta, USA. [[PDF](https://raihanjoty.github.io/papers/mehdad-carenini-ng-joty-naacl-13.pdf)]

```
@InProceedings{mehdad-carenini-ng-joty-naacl-13,
  author    = {Mehdad, Yashar  and  Carenini, Giuseppe  and  Ng, Raymond T.  and  Joty, Shafiq},
  title     = {Towards Topic Labeling with Phrase Entailment and Aggregation},
  booktitle = {Proceedings of the 2013 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies},
  Series = {NAACL'13},
  month     = {June},
  year      = {2013},
  address   = {Atlanta, Georgia},
  publisher = {ACL},
  pages     = {179--189}
}
```
---
Shafiq Joty, Giuseppe Carenini, Gabriel Murray and Raymond Ng. Supervised Topic Segmentation of Email Conversations. In Fifth International AAAI Conference on Weblogs and Social Media (ICWSM) 2011, Barcelona, Spain, AAAI. (short paper) [[PDF](https://www.aaai.org/ocs/index.php/ICWSM/ICWSM11/paper/viewFile/2882/3228)]

```
@inproceedings{joty-carenini-murray-ng-icwsm-11,
  Address = {Barcelona, Spain},
  Author = {Shafiq Joty and Giuseppe Carenini and Gabriel Murray and Raymod Ng},
  Booktitle = {Proceedings of the Fifth International AAAI Conference on Weblogs and Social Media},
  Pages = {530--533},
  Publisher = {AAAI},
  Series = {ICWSM'11},
  url    = {https://www.aaai.org/ocs/index.php/ICWSM/ICWSM11/paper/viewFile/2882/3228},
  Title = {{Supervised Topic Segmentation of Email Conversations}},
  Year = {2011}
}
```
---
Joty S.,  Carenini G., Murray G. and Ng R.. Exploiting Conversation Structure in Unsupervised Topic Segmentation for Emails. In Proc. of the Conference on Empirical Methods in NLP (EMNLP 2010), MIT, Massachusetts, USA, Oct. 2010 . [[PDF](http://www.aclweb.org/anthology/D10-1038)]

```
@inproceedings{joty-carenini-murray-ng-emnlp-10,
  Address = {Massachusetts, USA},
  Author = {Shafiq Joty and Giuseppe Carenini and Gabriel Murray and Raymond Ng},
  Booktitle = {Proceedings of the conference on Empirical Methods in Natural Language Processing},
  Pages = {388--398},
  Publisher = {ACL},
  Series = {EMNLP'10},
  Title = {{Exploiting Conversation Structure in Unsupervised Topic Segmentation for Emails}},
  url    = {http://www.aclweb.org/anthology/D10-1038},
  Year = {2010}
}
```
