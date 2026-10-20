# Ilya Sutskever 的 AI 阅读清单（“30 篇论文”）

> 传说：OpenAI 前首席科学家 Ilya Sutskever 给 John Carmack 开过一份书单，并说：“如果你真正吃透这些，你就掌握了如今 AI 领域 90% 的精髓。”

## 先说明三点

- **实际流传下来的是 27 项，不是 30 篇。** 一般的说法是原清单约 30 项，剩下几项没有公开。
- **Ilya 本人从未公开确认过这份清单。** 它在 2024 年开始广泛流传，社区普遍认可，但“90%”这句话也是转述。
- **不全是论文。** 里面还有博客文章、课程、博士论文和一本书的章节。

---

## 一、Transformer 与注意力机制

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 1 | [Attention Is All You Need](https://arxiv.org/abs/1706.03762) | Vaswani et al., 2017 | 论文 | 提出 Transformer，现代大模型的基础架构 |
| 2 | [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/) | Harvard NLP（Rush 等） | 博客 / 代码 | 逐行代码讲解 Transformer，最适合入门 |
| 3 | [Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473) | Bahdanau, Cho, Bengio, 2014 | 论文 | 首次在翻译中引入注意力机制 |

## 二、循环神经网络（RNN / LSTM）

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 4 | [The Unreasonable Effectiveness of Recurrent Neural Networks](https://karpathy.github.io/2015/05/21/rnn-effectiveness/) | Andrej Karpathy, 2015 | 博客 | 用字符级 RNN 生成文本，直观展示 RNN 的能力 |
| 5 | [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) | Christopher Olah, 2015 | 博客 | 图解 LSTM 的门控结构，经典入门文章 |
| 6 | [Recurrent Neural Network Regularization](https://arxiv.org/abs/1409.2329) | Zaremba, Sutskever, Vinyals, 2014 | 论文 | 如何在 LSTM 上正确使用 Dropout |
| 7 | [Pointer Networks](https://arxiv.org/abs/1506.03134) | Vinyals, Fortunato, Jaitly, 2015 | 论文 | 输出指向输入位置，可以解决排序、凸包等问题 |
| 8 | [Order Matters: Sequence to Sequence for Sets](https://arxiv.org/abs/1511.06391) | Vinyals, Bengio, Kudlur, 2015 | 论文 | 输入和输出的顺序会影响 seq2seq 的学习效果 |
| 9 | [Neural Turing Machines](https://arxiv.org/abs/1410.5401) | Graves, Wayne, Danihelka, 2014 | 论文 | 给神经网络加上可读写的外部记忆 |
| 10 | [Relational Recurrent Neural Networks](https://arxiv.org/abs/1806.01822) | Santoro et al., 2018 | 论文 | 在记忆单元之间用注意力做关系推理 |

## 三、卷积网络与计算机视觉

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 11 | [ImageNet Classification with Deep Convolutional Neural Networks](https://proceedings.neurips.cc/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html)（AlexNet） | Krizhevsky, Sutskever, Hinton, 2012 | 论文 | 引爆深度学习时代的里程碑 |
| 12 | [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)（ResNet） | He et al., 2015 | 论文 | 残差连接，让上百层的网络也能训练 |
| 13 | [Identity Mappings in Deep Residual Networks](https://arxiv.org/abs/1603.05027) | He et al., 2016 | 论文 | 改进 ResNet，分析残差连接为什么有效 |
| 14 | [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122) | Yu & Koltun, 2015 | 论文 | 空洞卷积，不降分辨率就能扩大感受野 |
| 15 | [CS231n: Convolutional Neural Networks for Visual Recognition](https://cs231n.github.io/) | Stanford（Karpathy 等） | 课程 | 斯坦福经典课程，系统打基础 |

## 四、关系推理与图网络

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 16 | [A Simple Neural Network Module for Relational Reasoning](https://arxiv.org/abs/1706.01427) | Santoro et al., 2017 | 论文 | Relation Network，用一个简单模块学会关系推理 |
| 17 | [Neural Message Passing for Quantum Chemistry](https://arxiv.org/abs/1704.01212) | Gilmer et al., 2017 | 论文 | 统一图神经网络的“消息传递”框架 |

## 五、生成模型

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 18 | [Variational Lossy Autoencoder](https://arxiv.org/abs/1611.02731) | Chen et al., 2016 | 论文 | 结合 VAE 与自回归模型，控制表征学到什么 |

## 六、规模化：扩展定律与工程

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 19 | [Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361) | Kaplan et al.（OpenAI）, 2020 | 论文 | 模型性能随参数、数据、算力按幂律提升 |
| 20 | [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://arxiv.org/abs/1811.06965) | Huang et al., 2018 | 论文 | 流水线并行，训练超大模型的工程方法 |
| 21 | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](https://arxiv.org/abs/1512.02595) | Amodei et al., 2015 | 论文 | 端到端语音识别，展示规模和工程的威力 |

## 七、理论基础：信息、复杂度与智能

| # | 标题 | 作者 / 年份 | 类型 | 一句话 |
|---|---|---|---|---|
| 22 | [Keeping Neural Networks Simple by Minimizing the Description Length of the Weights](https://www.cs.toronto.edu/~hinton/absps/colt93.pdf) | Hinton & van Camp, 1993 | 论文 | 从最小描述长度的角度看神经网络的泛化 |
| 23 | [A Tutorial Introduction to the Minimum Description Length Principle](https://arxiv.org/abs/math/0406077) | Peter Grünwald, 2004 | 教程 | MDL 原则入门：学习就是压缩 |
| 24 | *Kolmogorov Complexity and Algorithmic Randomness* | Shen, Uspensky, Vereshchagin | 书（第 14 章） | 柯尔莫哥洛夫复杂度的理论基础 |
| 25 | [The First Law of Complexodynamics](https://scottaaronson.blog/?p=762) | Scott Aaronson, 2011 | 博客 | 为什么系统的“有趣程度”先升后降 |
| 26 | [Quantifying the Rise and Fall of Complexity in Closed Systems: The Coffee Automaton](https://arxiv.org/abs/1405.6903) | Aaronson, Carroll, Ouellette, 2014 | 论文 | 用“咖啡与奶混合”的模型量化复杂度变化 |
| 27 | [Machine Super Intelligence](https://www.vetta.org/documents/Machine_Super_Intelligence.pdf) | Shane Legg, 2008 | 博士论文 | DeepMind 联合创始人对“通用智能”的形式化定义 |

---

## 建议阅读顺序（入门者）

1. **先建立直觉**：#5 LSTM 图解 → #4 Karpathy RNN → #2 Annotated Transformer
2. **再读核心论文**：#11 AlexNet → #12 ResNet → #3 Bahdanau 注意力 → #1 Attention Is All You Need
3. **理解规模化**：#19 Scaling Laws → #20 GPipe
4. **最后读理论**：#22、#23 MDL → #25、#26 复杂度 → #27 机器超级智能

## 参考来源

- [The 27 papers – LessWrong](https://lesswrong.com/posts/t4ZBjAjXk2NqqAqJ7/the-27-papers)
- [Ilya Sutskever reading list – Turing Post](https://turingpost.com/p/ilya-sutskever-reading-list)
- [Deep Learning Legends: Ilya's List – Gonzo ML](https://gonzoml.substack.com/p/deep-learning-legends-ilyas-list)
