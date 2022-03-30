+++
abstract = "Rumors spread in social media severely jeopardize the credibility of online content. Thus, automatic debunking of rumors is of great importance to keep social media a healthy environment. While facing a dubious claim, people often dispute its truthfulness sporadically in their posts containing various cues, which can form useful evidence with long-distance dependencies. In this work, we propose to learn discriminative features from microblog posts by following their non-sequential propagation structure and generate more powerful representations for identifying rumors. For modeling non-sequential structure, we firstly represent the diffusion of microblog posts with propagation trees, which provide valuable clues on how a claim in the original post is transmitted and developed over time. We then present a bottom-up and a top-down tree-structured models based on Recursive Neural Networks (RvNN) for rumor representation learning and classification, which naturally conform to the message propagation process in microblogs. To enhance the rumor representation learning, we reveal that effective rumor detection is highly related to finding evidential posts, e.g., the posts expressing specific attitude towards the veracity of a claim, as an extension of the previous RvNN-based detection models that treat every post equally. For this reason, we design discriminative attention mechanisms for the RvNN-based models to selectively attend on the subset of evidential posts during the bottom-up/top-down recursive composition. Experimental results on four datasets collected from real-world microblog platforms confirm that 1) our RvNN-based models achieve much better rumor detection and classification performance than state-of-the-art approaches; 2) the attention mechanisms for focusing on evidential posts can further improve the performance of our RvNN-based method; and 3) our approach possesses superior capacity on detecting rumors at very early stage."
authors = ["Jing Ma", "Wei Gao", "Shafiq Joty", "Kam-Fai Wong"]
date = "2020-07-01"
image = ""
image_preview = ""
math = false
publication_types = ["2"]
selected = true
publication = "ACM Transactions on Intelligent Systems and Technology (TIST)"
title = "An Attention-based Rumor Detection Model with Tree-structured Recursive Neural Networks"
url_code = ""
url_dataset = ""
url_pdf = "https://dl.acm.org/doi/abs/10.1145/3391250"
url_project = ""
url_slides = ""
url_video = ""
+++