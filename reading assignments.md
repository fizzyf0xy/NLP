## Reading assignments

As we have mentioned in the class, read just one ACL / EMNLP / NIPS paper.   You can select any paper you like.

Append a table in a Github repo.

Since this is your first week, we shall warm up and give you two weeks for your first paper.

PS:  Note that you may not completely understand everything, but just try your best.   Once you reach the mark of 50+ papers, you will start to understand and become superman.

Enjoy reading.

Point criteria:
0:  Not done / copy
1:  Ok
2:  With good, clear, precise, personal explanations in own words

## Learning a Grammar Inducer from Massive Uncurated Instructional Videos
Link: https://preview.aclanthology.org/emnlp-22-ingestion/2022.emnlp-main.16.pdf

|Title|Learning a Grammar Inducer from Massive Uncurated Instructional Videos|
|------|-----|
|Problems|They investigate the problems about text and video are in loose correspondence, and they need to leverage video information for finding more accurate syntactic grammars for accompanying text.|
|Related works| 1. Lisa Anne Hendricks, Oliver Wang, Eli Shechtman, Josef Sivic, Trevor Darrell, and Bryan Russell. 2017. Localizing moments in video with natural language. In ICCV. |
|             |2. Luowei Zhou, Chenliang Xu, and Jason J Corso. 2018. Towards automatic learning of procedures from web instructional videos. In AAAI. |
|             |3. Jun Xu, Tao Mei, Ting Yao, and Yong Rui. 2016. MSR- VTT: A large video description dataset for bridging video and language. In CVPR.|
|Method|C- PCFG, MMC-PCFG and PTC-PCFG|
|Results|1. C-PCFG achieve better performance when they are trained with more instances from HowTo100M than the original in-domain training sets.|
|       |2. PTC-PCFG achieves the best performances in all three datasets. It can further improve S-F1 to +6.3% on DiDeMo, +16.7% on YouCook2 and +2.8% on MSRVTT|
|       |3. PTC-PCFG achieves the best performances in all three datasets.|
|Conclusion|They knew how massive instructional YouTube video and subtitle pairs can improve grammar induction through new model in multi-modal pre-training to learn better video span correlation by experimenting on three benchmarks demonstrate.|
|Limitations|1. The models only use instructional video and do not have the capability to interact with the world, they are unrealistic for human language learners.|
|           |2. The complexity of the PCFG induction algorithm they use is cubic to the number of syntactic categories, therefore potentially limits the usefulness of larger amounts of data.|

## A Fast and Accurate Dependency Parser using Neural Networks
Link: https://aclanthology.org/D14-1082.pdf

|Title|A Fast and Accurate Dependency Parser using Neural Networks|
|------|-----|
|Related Works|1. Neural networks in a broad-coverage Penn Treebank parser (Henderson, 2004)|
|             |2. Transition-based dependency parsers using a Temporal Restricted Boltzman Machine (Garg and Henderson, 2011)|
|             |3. Precursive neural networks for transition-based dependency parsing (Stenetorp, 2013)|
|Method|1. LEFT-ARC(l): adding an arc s1 → s2 with label l and removes s2 from the stack. Pre-condition: |s| ≥ 2.|
|      |2. RIGHT-ARC(l): adding an arc s2 → s1 with label l and removes s1 from the stack. Pre-condition: |s| ≥ 2.|
|      |3. SHIFT: b1 moves from the buffer to the stack. Precondition: |b| ≥ 1.|
|Results|The parser is better in terms of both accuracy and speed. When we comparing between the baselines of arc-eager and arc-standard parsers, the parser achieves 2% improvement in UAS and LAS on all datasets, while running about 20 times faster.|


## Neural Topic Model with Reinforcement Learning
Link: https://aclanthology.org/D19-1350.pdf

|Title|Neural Topic Model with Reinforcement Learning|
|------|-----|
|Problems|They want to use inforcement learning and incorporate topic coherence measures as reward signals to guide the learning of a VAE-based topic model.|
|Related works| 1. Qingyu Yin, Yu Zhang, Wei-Nan Zhang, Ting Liu, and William Yang Wang. 2018. Deep reinforce- ment learning for chinese zero pronoun resolution. |
|             |2. Yishu Miao, Lei Yu, and Phil Blunsom. 2016. Neu- ral variational inference for text processing. |
|Method|Reinforcement Learning, VTMRL(Best practice), LDA, NVDM, NGTM|
|Results|VTMRL show superior performance both on perplexity and topic coherence measure compared to state-of-the-art neural topic models.|
|Conclusion|They have proposed a new reinforcement learning (RL) framework for neural topic modelling, where words are activated dynamically by RL according to topic coherence scores and topic overlapping values.|
|Limitations|The experiments are made on the 20 Newsgroups and NIPS datasets not temporal modelling.|


## Beyond Accuracy: Behavioral Testing of NLP Models with CheckList
Link: https://aclanthology.org/2020.acl-main.442.pdf
|Title|Beyond Accuracy: Behavioral Testing of NLP Models with CheckList|
|------|-----|
|Problems|They want to decrease biases and capability failures into specific behaviors by proposing CheckList, a new evaluation methodology and accompanying tool for comprehensive behavioral testing of NLP models.|
|Related works|1.Saleema Amershi, Andrew Begel, Christian Bird, Rob DeLine, Harald Gall, Ece Kamar, Nachi Nagap- pan, Besmira Nushi, and Tom Zimmermann. 2019. Software engineering for machine learning: A case study. |
|             |2.Mor Geva, Yoav Goldberg, and Jonathan Berant. 2019. Are we modeling the task or the annotator? an inves- tigation of annotator bias in natural language under- standing datasets. |
|             |3.Eric Wallace, Shi Feng, Nikhil Kandpal, Matt Gardner, and Sameer Singh. 2019. Universal adversarial trig- gers for attacking and analyzing nlp.|
|Method| MFT, NER, DIR, NLP tasks: sentiment analysis (Sentiment), duplicate question detection, and machine comprehension|
|Results|Users without prior experience are able to find significant bugs in a SOTA model in only 2 hours. Rate different aspects of CheckList (on a scale of 1-5), users in- dicated the testing session helped them learn more about the model (4.7  ̆ 0.5), capabilities helped them test the model more thoroughly (4.5  ̆ 0.4), and so did templates (4.3  ̆ 1.1).|
|Conclusion| CheckList reveals critical bugs in commercial systems developed by large software companies, indicating that it complements current practices well. Tests created with CheckList can be applied to any model, making it easy to incorporate in current benchmarks or evaluation pipelines.|
|Limitations|They expect that collaborative test creation will result in evaluation of NLP models that is much more ro- bust and detailed, beyond just accuracy on held-out data.|



## BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding
Link: https://arxiv.org/pdf/1810.04805.pdf
|Title|BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding|
|------|-----|
|Problems|They improve the fine-tuning based approaches by proposing BERT, which alleviates the unidirectionality constraint by using a “masked language model” (MLM) pre-training objective, inspired by the Cloze task.|
|Related works|1.Unsupervised Feature-based Approaches: William Fedus, Ian Goodfellow, and Andrew M Dai. 2018. Maskgan: Better text generation via filling in the . . arXiv preprint arXiv:1801.07736.|
|             |2.Unsupervised Fine-tuning Approaches: Jeremy Howard and Sebastian Ruder. 2018. Universal language model fine-tuning for text classification. |
|             |3.Transfer Learning from Supervised Data: Jason Yosinski, Jeff Clune, Yoshua Bengio, and Hod Lipson. 2014. How transferable are features in deep neural networks?|
|Method|BERT|
|Results|They obtain new state-of-the-art results on eleven natural language processing tasks, following as below.|
|       |GLUE score to 80.5% (7.7% point absolute improvement), MultiNLI accuracy to 86.7% (4.6% absolute improvement), SQuAD v1.1 question answering Test F1 to 93.2 (1.5 point absolute im- provement) and SQuAD v2.0 Test F1 to 83.1 (5.1 point absolute improvement).|
|Conclusion|Recent empirical improvements due to transfer learning with language models have demonstrated that rich, unsupervised pre-training is an integral part of many language understanding systems, and enable even low-resource tasks to benefit from deep unidirectional architectures.|
|Limitations|They need a further generalizing these findings to deep bidirectional architectures, allowing the same pre-trained model to successfully tackle a broad set of NLP tasks.|
