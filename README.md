# openai_embed_finetune

## 简介

* 大规模微调OpenAI的text-embedding-ada-002嵌入模型（Finetune text-embedding-ada-002）；

* 构建医学专业领域的OpenAI embedding嵌入模型，使用超过26w条医学数据进行联合微调得到；

* 微调构造一个专业领域文本相似度任务、问答任务的嵌入模型；


## 背景background

OpenAI的text-embedding-ada-002 嵌入模型有廉价、支持多任务且支持8192 token长度的优点，但在中文某些专业领域（如医学）的文本匹配任务中，仍然表现欠佳。

## 原理

* 使用了对比学习进行联合微调，类似Clip拉远负样本而拉近正样本之间的距离
* 在传统text-embedding-ada-002的输出后面加多了一层MLP用于对齐
* 主要可以用来预测疾病种类、辅助诊疗、会话分类、医学文本内容检索等
* 像chatpdf这种专业领域文献问答使用微调过嵌入模型效果可能会更好

## 模型 model

