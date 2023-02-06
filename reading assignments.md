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
