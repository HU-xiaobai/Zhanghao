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
Various deep learning models and framework are applied into VQG tasks. However, the internal model components are nearly the same or the variants from basic models. The papers below list the basic components.
* Compact Bilinear Pooling. Yang Gao, Oscar Beijbom, Ning Zhang, Trevor Darrell; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016, pp. 317-326
* Auto-Encoding Variational Bayes. Diederik P Kingma and Max Welling. 2013
* Learning Internal Representations by Error Propagation(Recurrent Neural Network). Rumelhart David E, Hinton Geoffrey E and  Williams Ronald J. 1985
* Long Short-Term Memory(LSTM). Sepp Hochreiter and Jürgen Schmidhuber. 1997
* Attention is All you Need. Ashish Vaswani, Noam Shazeer, Niki Parmar, Jakob Uszkoreit, Llion Jones, Aidan N. Gomez, Łukasz Kaiser and Illia Polosukhin. 2017
* Generative adversarial networks. Ian J. Goodfellow, Jean Pouget-Abadie, Mehdi Mirza, Bing Xu, David Warde-Farley, Sherjil Ozair, Aaron Courville and Yoshua Bengio. 2014

### Evaluation metrics
After we complete VQG tasks, we should evaluate our VQG systems to compare the state-of-the-art technique. These papers below list general evaluation metrics for VQG tasks. However, until now, actually there are not precise evaluation methods to measure some properties of VQG tasks such as ambiguity, difficulty, meaningful etc, even accuracy. Further more, the definition of these properties of VQG are also ambigious without the same standard. Hence we propose the fourth question above.
* BLEU: a method for automatic evaluation of machine translation. Kishore Papineni, Salim Roukos, Todd Ward, and Wei-Jing Zhu. 2002
* METEOR: An Automatic Metric for MT Evaluation with Improved Correlation with Human Judgments. Satanjeev Banerjee and Alon Lavie. 2005
* ROUGE: A package for automatic evaluation of summaries. Chin-Yew Lin. 2004
* CIDEr: Consensus-Based Image Description Evaluation. Ramakrishna Vedantam, C. Lawrence Zitnick, Devi Parikh; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2015, pp. 4566-4575

In addition, spefically, in VQG tasks, some novel metrics are invented to measure different properties:

* IVQA: Inverse Visual Question Answering. Feng Liu, Tao Xiang, Timothy M. Hospedales, Wankou Yang and Changyin Sun; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018, pp. 8611-8619
* Creativity: Generating Diverse Questions Using Variational Autoencoders. Unnat Jain, Ziyu Zhang and Alexander G. Schwing; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2017, pp. 6485-6494
* Predicting Difficulty and Discrimination of Natural Language Questions. Matthew A. Byrd and Shashank Srivastava. 2022

## VQG Models
This section we would list current VQG models in terms of training process condition.
### Unconditional VQG
This part we would list papers about the current work about the VQG without constrains.(The input is only images.)
* Generating Natural Questions About an Image. Nasrin Mostafazadeh, Ishan Misra, Jacob Devlin, Margaret Mitchell, Xiaodong He and Lucy Vanderwende. 2016
* Learning by Asking Questions. Ishan Misra, Ross Girshick, Rob Fergus, Martial Hebert, Abhinav Gupta, Laurens van der Maaten; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018, pp. 11-20
* Goal-Oriented Visual Question Generation via Intermediate Rewards. Junjie Zhang, Qi Wu, Chunhua Shen, Jian Zhang, Jianfeng Lu, Anton van den Hengel; Proceedings of the European Conference on Computer Vision (ECCV), 2018, pp. 186-201
* A Reinforcement Learning Framework for Natural Question Generation using Bi-discriminators. Zhihao Fan, Zhongyu Wei, Siyuan Wang, Yang Liu and Xuanjing Huang. 2018
* Visual Curiosity: Learning to Ask Questions to Learn Visual Recognition. Jianwei Yang, Jiasen Lu, Stefan Lee, Dhruv Batra and Devi Parikh. Proceedings of The 2nd Conference on Robot Learning, PMLR 87:63-80, 2018.
### Conditional VQG
This part we would list papers about the current work about the VQG with various constrains(such as answers, image caption, vedio, etc.) Current works prefer to focusing on inference of the VQG. However, there are less inputs with multiple images/videos and knowledge based for VQG. Hence we propose our first and third questions. 
* Generating Natural Questions from Images for Multimodal Assistants. Alkesh Patel, Akanksha Bindal, Hadas Kotek, Christopher Klein and Jason Williams. 2021 (with image captions)
* Inferential Visual Question Generation. Chao Bi, Shuhui Wang, Zhe Xue, Shengbo Chen and Qingming Huang. 2022 (with image caption)
* IVQA: Inverse Visual Question Answering. Feng Liu, Tao Xiang, Timothy M. Hospedales, Wankou Yang and Changyin Sun; Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2018, pp. 8611-8619 (with answers)
* Information Maximizing Visual Question Generation. Ranjay Krishna, Michael Bernstein, Li Fei-Fei; Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2019, pp. 2008-2018 (with answers)
