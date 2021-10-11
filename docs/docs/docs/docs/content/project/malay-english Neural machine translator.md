+++
# Date this page was created.
date = "2018-09-07"

# Project title.
title = "Malay-English Neural Machine Translation System."

# Project summary to display on homepage.
summary = "A demo of malay english Machine translation system."

# Optional image to display on homepage (relative to `static/img/` folder).
image_preview = "mt.png"

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "graphical-model"]`
tags = ["multi-lingual", "deep-learning"]

# Optional external URL for project (replaces project detail page).
external_link = ""
highlight = false
# Does the project detail page use math formatting?
math = false

# Optional featured image (relative to `static/img/` folder).
[header]
image = "mt.png"
caption = "Only accessible inside ntu network. (http://172.21.145.63:4200/)"

+++

This is a tool to translate an English sentence into Malay and vice versa. Developing a translation tool for low-resource languages like Malay has always been a challenge. The main challenge comes from the fact that machine translation systems typically rely on a huge amount of sentence-parallel data, and creating such datasets is an expensive process. In our work, we collected parallel datasets from various sources including News, OpenSubtitiles (OPUS), Ted talks, and Youtube video. Therefore, our corpus is quite generic and covers both texts and conversations.

We used various state of the art deep **Neural Machine Translation** (NMT) architecture for training our model. More specifically we use both **seq2seq** and **transformer-net** architecture for finding our best model. For pre-processing and post-processing datasets we used various tools of **moses**. To train our model we used **OpenNMT-py** framework which is very standard in the NMT community for it's robust and modular implementation.

Currently the live demo can only be accessed from inside NTU network.
<form action="http://172.21.145.63:4200">
    <input type="submit" value="The link of the demo" />
</form>
