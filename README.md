# Insightful AI Papers

## Natural Language Processing

* Baseline Needs More Love: On Simple Word-Embedding-Based Models and Associated Pooling Mechanisms, 2018
  * https://arxiv.org/abs/1805.09843
  * Can summarise a sequence as its max-pooled word embeddings. Authors call this architecture a Simple Word-Embedding-Based Model (SWEM).
  * Max pooling extracts the most salient features from the sequence.
  * Despite their simplicity, for many tasks SWEMs outperform CNNs and RNNs.
  * Recurrent connections (e.g. RNNs) are slow to train. Self-attention based methods (e.g. transformers) are faster but attention weight matrices are huge for long sequences. SWEMs have no recurrent connections and do not use self-attention, so are relatively inexpensive.
  * Particularly effective for long documents.
  * Components of the learnt word embeddings are interpretable (see section 4.1.1).
  * Would be useful to build a Python package that allows people to easily build and interpret SWEMs, along with explaining the merits of them over self-attention and RNNs.
* A Survey of Reinforcement Learning Informed by Natural Language, 2019
  * https://arxiv.org/abs/1906.03926
  * Survey of how NLP and RL have been combined.
  * Language-coniditonal RL - Tasks where the agent is unable to complete the task without the literature e.g. where the agent is instructed what to do in natural language
  * Language-assisted RL - Tasks where the agent can complete the task without the literature, but the literature assists learning e.g. describing dynamic environments
  * Most of the work has been on structured language (e.g. language is constructed from templates), which works well for games, but in the real world language is mostly unstructured, so more research is needed in this area

## Computer Vision

* An Image is 16x16 Words: Transformers for Image Recognition at Scale, 2020
  * https://arxiv.org/abs/2010.11929
  * Image classification using transformers.
  * Seems very similar to VisualBERT but without the natural language input, and instead of the input to the transformer being region proposals from an object detection network, they use linear projected image patches as input.
  * Using image patches is a bit janky, as humans don't think in 16x16 boxes, but reminds me of YOLO object detection which also describes the position of objects relative to image patches.
  * Would be interesting to apply this network to a multimodal dataset (combination of natural language and image as input), such as Hateful Memes, to see how it performs relative to VisualBERT.

## Interpretability

* A Unified Approach to Interpreting Model Predictions, 2017
  * https://proceedings.neurips.cc/paper/2017/hash/8a20a8621978632d76c43dfd28b67767-Abstract.html
  * This seems like a good way to intrepret SWEMs. 

## Applications

* Challenges in Deploying Machine Learning: a Survey of Case Studies, 2020
  * https://arxiv.org/abs/2011.09926
  * Good paper for understanding the challenges that arise when bringing a model into production.
  * A good approach is to build the pipeline around the simplest possible model, and then once the pipeline is implemented increase the complexity. 
  * Better performance on evaluation metric often doesn't translate to improved business performance.
  * Models are becoming huge e.g. transformers, but most companies don't have the resources to train and tune these huge models.
