# Visual Question Generation: Roadmap 
Zhanghao HU, University of Edinburgh, s2135970@ed.ac.uk

## Preface
Recently, the researches in the interaction between the domains of vision and language have attracted booming interest. One of the latest and promising examples: visual question generating(VGQ), is referring to leading the machine understand to produce questions for given images. It is originally proposed to facilitate the automatic construction of large-scale visual question answering(VQA) datasets, but now various reseaches applying to interactive application such as visual online dialogue emerge. However, different from the image captioning or VQA which describe visual information in natural language, VQG focuses more on proposing meaningful and unambiguous questions based on the visual information so that it could be answered without any confusion, which is considered to be more intelligent.   

In terms of training process, existing researches on VQG could be categorized into unconditional and conditional VQG, considering whether any contraint is added into training process to supervise. Specifically, unconditional VQG focuses on generating questions only with a given image, treating the VQG as a reverse VQA problem without any constraint. Although their models could generate a bulk of open questions, the generated questions are too abstract to be practically usable without any meaning, logic and inference. Conditional VQG aims to generate questions about an image by anxiliary information such as answers together with visual content. Previous researches have shown more meaningful and inferential in term of the object location within images.

However, in terms of the shortcomings of current researches, we might ask the following questions:

1. How could machine generate questions about abstract concepts and causal relationships with prior knowledge?
2. Could machine generate questions about a video and reveal the inference/description of the whole event?
3. Could machine generate question about multiple images and reveal their inter relations? 
4. How could we evaluate the "meaningful" and "inferential" of the generated questions and then classify the questions with high meaning and inference? 
5. Could we add the constraints about the type of the generated questions?(such as what, why, how, and yes/no question etc.)

## Pre-requisites

Most VQG tasks are completed by deep learning network. To better understand the VQG paper listed in the following sections, we might need some basic understanding of machine learning, deep learning models and evaluation methods about VQG.

### Basic machine learning understanding
* Pattern Recognition and Machine Learning. Christopher M. Bishop. 2006
* Machine Learning: A Probabilistic Perspective. Kevin P. Murphy. 2012
* Speech and Language Processing (3rd edition). Dan Jurafsky and James H. Martin. 2022 

### Deep learning models applied in VQG
Various deep learning models and framework are applied into VQG tasks. However, the inter model components are nearly the same or the variants from basic models. The papers below list the basic components.
* Compact Bilinear Pooling. Yang Gao, Oscar Beijbom, Ning Zhang, Trevor Darrell; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016, pp. 317-326
* Auto-Encoding Variational Bayes. Diederik P Kingma and Max Welling. 2013
* Learning Internal Representations by Error Propagation(Recurrent Neural Network). Rumelhart David E, Hinton Geoffrey E and  Williams Ronald J. 1985
* Long Short-Term Memory(LSTM). Sepp Hochreiter and Jürgen Schmidhuber. 1997
* Attention is All you Need. Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser and Illia Polosukhin. 2017
* Generative adversarial networks. Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville and Yoshua Bengio. 2014

