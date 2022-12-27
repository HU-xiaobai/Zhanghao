# Visual Question Generation: Roadmap 
Zhanghao HU, University of Edinburgh, s2135970@ed.ac.uk

## Preface
Recently, the researches in the interaction between the domains of vision and language have attracted booming interest. One of the latest and promising examples: visual question generating(VGQ), is referring to leading the machine understand to produce questions for given images. It is originally proposed to facilitate the automatic construction of large-scale visual question answering(VQA) datasets, but now various reseaches applying to interactive application such as visual online dialogue emerge. However, different from the image captioning which describes visual information in natural language, VQG focuses more on proposing meaningful and logical questions based on the visual information, which is more challenging.  

Existing research on VQG could be categorized into unconditional and conditional VQG, considering whether any contraint is added into training process to supervise. Specifically, unconditional VQG focuses on generating questions only with a given image, treating the VQG as a reverse VQA problem without any constraint. Although their models could generate a bulk of open questions, the generated questions are too abstract to be practically usable without any meaning, logic and inference. Conditional VQG aims to generate questions about an image by anxiliary information such as answers together with visual content. Previous researches have shown more meaningful and inferential in term of the object location within images.

However, in terms of the shortcomings of current researches, we might ask the following questions:

1. How could machine generate questions about abstract concepts and causal relationships with prior knowledge?
2. Could machine generate questions about a video and reveal the inference/description of the whole event?
3. Could machine generate question about multiple images and reveal their inter relations? 
4. How could we evaluate the "meaningful" and "inferential" of the generated questions and then classify the questions with high meaning and inference? 
