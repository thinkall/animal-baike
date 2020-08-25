# animal-baike
基于PaddleHub动物识别模型及百度百科的动物百科AI老师。

- PaddleHub: https://www.paddlepaddle.org.cn/hub
- PaddlePaddle: https://www.paddlepaddle.org.cn/

## How to use
Read more in [animal-baike.ipynb](animal-baike.ipynb).


## PaddleHub用后感
PaddleHub是飞桨生态的预训练模型应用工具，开发者可以便捷地使用高质量的预训练模型结合Fine-tune API快速完成模型迁移到部署的全流程工作。PaddleHub提供的预训练模型涵盖了图像分类、目标检测、词法分析、语义模型、情感分析、视频分类、图像生成、图像分割、文本审核、关键点检测等主流模型。

作为国内最大的AI预训练模型仓库，[PaddleHub](https://www.paddlepaddle.org.cn/hub)可对标于[TensorFlow Hub](https://www.tensorflow.org/hub)和[Pytorch Hub](https://pytorch.org/hub/)，PaddleHub在模型数量、模型类型丰富性、模型实用性、模型性能等多个方面都可比甚至优于TensorFlow Hub和Pytorch Hub。

首先说模型数量，PaddleHub现有模型100+；TensorFlow Hub作为最早的预训练模型仓库，现有模型600+；Pytorch Hub应该是三者中最晚建立的，现有模型30+。

其次看模型类型丰富性，PaddleHub现包含NLP、CV等多个领域十多个子领域的模型；TensorFlow Hub现包含NLP、CV、Audio等各大领域20+子领域的模型；Pytorch现包含多个子领域模型。但PaddleHub包含一些独有的model类型，比如人脸关键点检测模型，starGAN等高级图像生成模型，OCR等高实用性模型，目前都是只有PaddleHub上有；另外对于中文语料的模型，PaddleHub就更是远比另外2个Hub要丰富了。

再次，对于模型的实用性，PaddleHub的众多模型都既有server端，又有mobile端，对于常用模型经过了调优，更有很多模型经过了百度自建大数据集的训练，比如本repo的动物识别模型，可以识别7000+动物种类；对于中文语料而言，PaddleHub上的模型自然更是比另外2个Hub的更接近开箱可用。

最后，对于模型性能，PaddleHub中的模型基本都经过了调优，性能不输对应算法原始论文，对于yolov3等模型，PaddleHub中优化的模型超越了原版。

前面说了很多优点，下面谈谈使用过程中遇到的一个问题。我本来还想用PaddleHub的人脸关键点检测模型做个人脸融合的算法，但是发现该算法准确度不够，检测出的眼睛、嘴巴位置不够准确，导致融合的人脸眼睛和嘴巴没有对齐，也就没有合二为一，而是叠影重重，效果较差。

总体而言，对于PaddlePaddle用户而言，PaddleHub是一个很好用的工具，能够找到很多预训练模型帮助你通过简单的几行代码迅速搭建原型。
