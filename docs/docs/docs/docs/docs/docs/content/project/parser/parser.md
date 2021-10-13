+++
# Date this page was created.
date = "2016-04-28"

# Project title.
title = "Discourse Parser for English"

# Project summary to display on homepage.
summary = ""

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "dt1.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning", "demo"]`
tags = ["discourse", "parser"]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Does the project detail page use math formatting?
math = false
highlight = false
# Optional featured image (relative to `static/img/` folder).
[header]
image = "dt1.png"
caption = "discourse parse tree"

+++

### About
This package includes:

* A discourse segmenter
* A discourse parser
* Evaluation metrics for discourse parsing

### Download
[Document-level Discourse Parser for English](https://drive.google.com/file/d/1p6UWefyI7l2_nIj249UoaMAu1lOp5UQo/view?usp=sharing)

### Demo
[Link](http://alt.qcri.org/demos/Discourse_Parser_Demo/)


### Installation
Required for the discourse segmenter:

1. [Charniak's reranking parser](https://github.com/BLLIP/bllip-parser). Put it in Tools/CharniakParserRerank and install it.
2. [Taggers from UIUC](http://cogcomp.cs.illinois.edu/page/software). Download POS tagger and shallow chunker [LBJPOS.jar, LBJChunk.jar, LBJ2.jar, LBJ2Library.jar] and put these in Tools/UIUC_TOOLs/
3. Install scikit-learn and scipy [(instructions)](http://scikit-learn.org/stable/install.html)
4. Install java if not installed [(instructions for Ubuntu)](https://help.ubuntu.com/community/Java)
5. Make sure the Tools/SPADE_UTILS/bin/edubreak is set to executable.

Required for the discourse parser:

1. Install wordNet (for example, On ubuntu you can write: apt-get install science-linguistics) and set the WNHOME environment variable to the WordNet directory. WNHOME should contain the dictionary files.
2. Install WordNet::QueryData (http://search.cpan.org/dist/WordNet-QueryData/QueryData.pm; also provided). To install it properly you may need to set the `$wnHomeUnix` and `$wnPrefixUnix` to the appropriate directories.


### Usage
For parsing a raw text, you should run discourse segmenter followed by discourse parser.

Running the discourse segmenter:

$ python Discourse_Segmenter.py <infile>
If it shows errors in apply_model method in loading the model, then it is due to differnt versions of the logistic regression in sklearn. To overcome this, open the commented "train_model" in do_segment method and run the segmenter. This learns the model and saves it. If it runs once, you don't need to run train_model again. You should comment it to save time.

Running the discourse parser:

$ python Discourse_Parser.py <discourse segmented file>



### Download 
[Evaluation Metrics for Discourse Parsing](http://alt.qcri.org/tools/discourse-eval/releases/current/discourse_eval.tar.gz). Latest release.
Implementation of the standard evaluation metrics as described in [Dan Marcu's book](http://mitpress.mit.edu/books/theory-and-practice-discourse-parsing-and-summarization's book).

### Usage
* Extract Set.tar.gz.
* Run the perl script:

```
Perl ParsingAccuracyMeasuresDocLevelForSystems.pl path_to_sys_dir path_to_gold_dir res.out
```

The main perl script takes three arguments:

1. Path to the directory with the system annotations: The filenames should end with *. doc_dis, but you can change the code according to your need. Here is where you need to change:

```
my @canFiles = grep /\w+\.doc_dis/, readdir(DIR);
```

2. Path to the Directory with the gold annotations: It assumes that the file names are the same as the system outputs (e.g., *.doc_dis).
3. The name of the output file: In the output file, it shows the results for the individual documents as well as the summary.

A sample output file is attached. The parsed documents should have the same format as RST-DT.



### Related publications
---
Shafiq Joty, Giuseppe Carenini, and Raymond Ng. 2015. CODRA: A Novel Discriminative Framework for Rhetorical Analysis. Computational Linguistics, Volume 41:3, MIT Press. [[Link to PDF](https://www.mitpressjournals.org/doi/abs/10.1162/COLI_a_00226)]


```
@article{joty-carenini-ng-cl-15,
  title="{CODRA: A Novel Discriminative Framework for Rhetorical Analysis}",
  author={Joty, Shafiq and Carenini, Giuseppe and Ng, Raymond T},
  journal = {Computational Linguistics},
  volume={41:3},
  publisher={MIT Press},
  pages={385-435},
  year={2015},
}
```
---
Shafiq Joty, Giuseppe Carenini, Raymond Ng and Yashar Mehdad. Combining Intra- and Multi-sentential Rhetorical Parsing for Document-level Discourse Analysis. In Proceedings of the 51st Annual Meeting of the Association for Computational Linguistics (ACL 2013), Sofia, Bulgaria. [[Link to PDF](https://aclanthology.info/papers/P13-1048/p13-1048)] 

```
@inproceedings{joty-carenini-ng-mehdad-acl-13,
  Title = {Combining Intra- and Multi-sentential Rhetorical Parsing for Document-level Discourse Analysis},  
  Author = {Joty, Shafiq and Carenini, Giuseppe and Ng, Raymond T. and Mehdad, Yashar},
  Address = {Sofia, Bulgaria},
  Booktitle = {Proceedings of the 51st Annual Meeting of the Association for Computational Linguistics},
  Numpages = {9},
  Publisher = {ACL},
  Series = {ACL-13},
  pages = {486-496},
  Year = {2013},
} 
```
---
Shafiq Joty, Giuseppe Carenini and Raymond Ng. A Novel Discriminative Framework for Sentence-Level Discourse Analysis. In Proceedings of the Conference on Empirical Methods in Natural Language Processing and the Conference on Natural Language Learning (EMNLP-CoNLL 2012), Jeju, Korea. [[PDF](http://www.aclweb.org/anthology/D12-1083)]

```
@inproceedings{joty2012novel,
  title={A novel discriminative framework for sentence-level discourse analysis},
  author={Joty, Shafiq and Carenini, Giuseppe and Ng, Raymond T},
  booktitle={Proceedings of the 2012 Joint Conference on Empirical Methods in Natural Language Processing and Computational Natural Language Learning},
  Series = {EMNLP-CoNLL-12},
  pages={904-915},
  year={2012},
  organization={Association for Computational Linguistics}
}
```





# License
The Discourse Parser is an Open Source Software, and is released under the Common Public License. You are welcome to use the code under the terms of the licence for research purposes ONLY, however please acknowledge its use with a citation given above in the Related publications.
