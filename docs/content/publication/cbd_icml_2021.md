+++
abstract = "Recent unsupervised machine translation (UMT) systems usually employ three main principles: initialization, language modeling and iterative back-translation, though they may apply these principles differently. This work introduces another component to this framework: Multi-Agent Cross-translated Diversification (MACD). The method trains multiple UMT agents and then translates monolingual data back and forth using non-duplicative agents to acquire synthetic parallel data for supervised MT. MACD is applicable to all previous UMT approaches. In our experiments, the technique boosts the performance for some commonly used UMT methods by 1.5-2.0 BLEU. In particular, in WMT'14 English-French, WMT'16 German-English and English-Romanian, MACD outperforms cross-lingual masked language model pretraining by 2.3, 2.2 and 1.6 BLEU, respectively. It also yields 1.5-3.3 BLEU improvements in IWSLT English-French and English-German translation tasks. Through extensive experimental analyses, we show that MACD is effective because it embraces data diversity while other similar variants do not." 
authors = ["Xuan-Phi Nguyen", "Shafiq Joty", "Thanh-Tung Nguyen", "Wu Kui", "Ai Ti Aw"]
date = "2021-05-15"
image = "https://nxphi47.github.io/images/publications/multi-agent-cross-translated-umt/algorithm1.png"
image_preview = ""
math = false
publication_types = ["1"]
selected = true
publication = "38th International Conference on Machine Learning (ICML), 2021"
title = "Cross-model Back-translated Distillation for Unsupervised Machine Translation"
url_code = "https://github.com/nxphi47/multiagent_crosstranslate"
url_dataset = ""
url_pdf = "https://arxiv.org/abs/2006.02163"
url_project = ""
url_slides = ""
url_video = ""
+++ 