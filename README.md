# OpenCLaP：多领域开源中文预训练语言模型仓库

## 目录
* [项目简介](#项目简介)
* [模型概览](#模型概览)
* [使用方式](#使用方式)
* [项目网站](#项目网站)
* [作者与致谢](#作者与致谢)

## 项目简介

OpenCLaP（Open **C**hinese **La**nguage **P**re-trained Model Zoo）是由清华大学人工智能研究院自然语言处理与社会人文计算研究中心推出的一个多领域中文预训练模型仓库。预训练语言模型通过在大规模文本上进行预训练，可以作为下游自然语言处理任务的模型参数或者模型输入以提高模型的整体性能。该模型仓库具有如下几个特点：

- 多领域。我们目前训练出了基于法律文本和百度百科的预训练模型，以提供多样化的可选择模型。
- 能力强。我们使用了当前主流的 BERT 模型作为预训练的神经网络结构，并支持最大 512 长度的文本输入来适配更加多样的任务需求。
- 持续更新。我们将在近期加入更多的预训练模型，如增加更多样的训练语料，使用最新的全词覆盖（Whole Word Masking）训练策略等。

## 模型概览

以下是我们目前公开发布的模型概览：

| 名称         | 基础模型  | 数据来源                            | 训练数据大小 | 词表大小 | 模型大小 | 下载地址 |
| ------------ | --------- | ----------------------------------- | ------------ | -------- | -------- | -------- |
| 民事文书BERT | bert-base | 全部民事文书                        | 2654万篇文书 | 22554    | 370MB | [点我下载](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/ms.zip)     |
| 刑事文书BERT | bert-base | 全部刑事文书                        | 663万篇文书  | 22554  | 370MB  | [点我下载](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/xs.zip)     |
| 百度百科BERT | bert-base | [百度百科](http://baike.baidu.com/) | 903万篇词条  | 22166  | 367MB  | [点我下载](https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/baike.zip)     |

## 使用方式

我们提供的模型可以被开源项目[pytorch-pretrained-BERT](https://github.com/huggingface/pytorch-pretrained-BERT)直接使用。以民事文书BERT为例，具体使用方法分为两步：

* 首先使用脚本下载我们的模型

```
wget https://thunlp.oss-cn-qingdao.aliyuncs.com/bert/ms.zip
unzip ms.zip
```

* 在运行时指定使用我们的模型`--bert_model $model_folder`来进行使用

## 项目网站

请访问 http://zoo.thunlp.org 以获得更多有关信息。

## 作者与致谢

Haoxi Zhong（钟皓曦，硕士生）, Zhengyan Zhang（张正彦，本科生）, [Zhiyuan Liu](http://nlp.csai.tsinghua.edu.cn/~lzy/)（刘知远，副教授）, [Maosong Sun](http://nlp.csai.tsinghua.edu.cn/site2/index.php/zh/people?id=16)（孙茂松，教授）.

感谢[幂律智能](http://powerlaw.ai/)对本项目的大力支持与帮助。

![img](http://zoo.thunlp.org/static/images/powerlaw.png)