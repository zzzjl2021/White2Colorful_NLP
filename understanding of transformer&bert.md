#今天主要学习了谷歌2017年推出的Transformer这个框架，包括以此为基准而产生的BERT模型

Transformer 是一个encoder-decoder方法下的模型，它解决了以往基于RNN的，或者LTSM记忆网络等在sequence2sequence任务上无法学习到长句子的信息、训练时间长的问题
Transformer的的每一个编码器都是由(multi)self-attention和feed-forward组成，解码器除了有(multi)self-attention和feed-forward之外，还多了一个encoder-decoder-attention模块。
根据不同的任务，设置不同的编码解码器数量。

Bert全名是Bidirectional Encoder Representations from Transformers（从Transformer来的双向编码器），ohh hoo，看清楚了，它是一个编码器，是part of transformer
Bert是一个预训练模型，通过两种方式训练得来的：masked words or predict sentence.
Bert在可以通过微调完成不同的任务，little like 迁移学习，pretrained一些共有的信息，再根据具体的任务进行微调，效果据说都很好。（很明显我现在很白，，也不跟依据，慢慢来好吧，以后的话会加上参考文献什么的）

贴上几篇今天看的比较好的文章吧，回头还是需要结合代码进行详细的了解，既然想要变得colorful,那首先就得知道有哪几种颜色不是？
1 我看（attention is all you need）看不下去的时候，读的一篇中文版解读然后找到原版：https://jalammar.github.io/illustrated-transformer/
  中文版也附上去吧：https://zhuanlan.zhihu.com/p/54356280
2 这篇是纯小白才需要看的，是我看上篇中的疑问Continuous Bag of Words (CBOW) Learning，然后搜到的，有点解决吧https://iksinc.online/2015/04/13/words-as-vectors/
3 这篇强推，可谓生龙活虎吧，多角度看解释，因为看不下去原文，就要多看一些别人的理解，但也不能只看一个，有失偏颇，所以又找了一篇：
  https://www.analyticsvidhya.com/blog/2019/06/understanding-transformers-nlp-state-of-the-art-models/
4 随后一篇是我不太理解解码器的作用看的一篇：https://easyaitech.medium.com/%E4%B8%80%E6%96%87%E7%9C%8B%E6%87%82-nlp-%E9%87%8C%E7%9A%84%E6%A8%A1%E5%9E%8B%E6%A1%86%E6%9E%B6-encoder-decoder-%E5%92%8C-seq2seq-1012abf88572
5 一切的开始，源自我不知道深度学习和bert的区别，这篇就讲了从RNN如何到BERT过程，人类技术认知升级过程：https://blog.csdn.net/wozhendexiangbu/article/details/116244890
 over!
 
