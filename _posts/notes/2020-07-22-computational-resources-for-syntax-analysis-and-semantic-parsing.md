---
layout: post
date updated: 2020-07-24 KST
date created: 2020-07-22 KST
date: 2020-07-22 KST
author: Sori Lee
---

# Computational resources for syntax analysis and semantic parsing

Here I list computational resources on [syntax analysis](https://en.wikipedia.org/wiki/Parsing) and [semantic parsing](https://en.wikipedia.org/wiki/Semantic_parsing).

<!-- ## Software or works with code-->

**ud2ccg (2019).**

- A domain adaptation method for Combinatory Categorial Grammar (CCG)
parsing [[Yosh19]](https://www.aclweb.org/anthology/P19-1013.pdf).
  - Independent of specific parser architecture.
- Resources:
  - Repository: <https://github.com/masashi-y/ud2ccg>
    - Last updated on 10 Jun 2019, as of writing.

<!--
**Consistent CCG Parsing over Multiple Sentences for Improved Logical Reasoning.**

- [[Yosh18]](https://www.aclweb.org/anthology/N18-2065.pdf)
-->

**CVT (2018).**

- [[Cla18]](https://arxiv.org/pdf/1809.08370.pdf). What it is, from its abstract:

  > We therefore propose Cross-View Training (CVT), a semi-supervised learning algorithm that improves the representations of a Bi-LSTM sentence encoder using a mix of labeled and unlabeled data.

  Why on this list:

  1. It's currently topping the 'CCG Supertagging on CCGBank' leaderboard [pwcCSC].

  2. Also currently leading the 'Depedency Parsing on Penn Treebank' benchmark [pwcDPPT] in unlabelled attachment score (UAS) and labeled attachment score (LAS).

- Computational resources: <https://github.com/tensorflow/models/tree/master/research/cvt_text>

**depccg (2017).**

- A CCG parser. Product of a 2017 research [[Yosh17]](https://www.aclweb.org/anthology/P17-1026.pdf).
  - The paper considers English and Japanese.
  - Written in Python and C++11.
- Resources:
  - Repository: <https://github.com/masashi-y/depccg>
    - [License](https://github.com/masashi-y/depccg/blob/master/LICENSE): MIT
  - PyPI: <https://pypi.org/project/depccg/>
  - Pre-trained English parsers: [listed](https://github.com/masashi-y/depccg/blob/master/README.md#using-a-pretrained-english-parser) in depccg's README.
  - Pre-trained Japanese parser: [described](https://github.com/masashi-y/depccg/blob/master/README.md#using-a-pretrained-japanese-parser) in depccg's README.

**LSTM CCG Parsing.

**EasySRL (2015).**

- A [semantic role labelling](https://en.wikipedia.org/wiki/Semantic_role_labeling) (SRL) model based on *joint* CCG syntactic and semantic parsing. [[Lew15]](https://www.aclweb.org/anthology/D15-1169.pdf)
  - Proposes, in particular, an [A* algorithm](https://en.wikipedia.org/wiki/A*_search_algorithm) for CCG parsing, faster than CKY with no loss in accuracy.[^4]
  - Achieved state-of-the-art SRL results as a non-ensemble model, which previous *joint* syntactic-semantic approaches seem to have failed.[^5]
  - Implementation written in Java.
- Computational resources:
  - Source repository: <https://github.com/uwnlp/EasySRL>
  - Pre-trained models: see the repository's [README](https://github.com/uwnlp/EasySRL/blob/master/README.md).

[^4]: [Lew15], the end of *1. Introduction*.

[^5]: [Lew15], the abstract and the beginning of *1. Introduction*.

**EasyCCG (2014).**

- A CCG parser. [[Lew14]](https://www.aclweb.org/anthology/D14-1107.pdf)
  - Written in Java.
- Web demo: [http://4.easy-ccg.appspot.com/](http://4.easy-ccg.appspot.com/do_parse?sentence=Fruit+flies+like+a+banana&nbest=5)
- Code availability:
  - Source & binaries: <https://github.com/mikelewis0/easyccg>
    - Last updated on 11 Jul 2015, as of writing.
  - Pre-trained parameters:[^1] <https://drive.google.com/#folders/0B7AY6PGZ8lc-NGVOcUFXNU5VWXc>
  - A [fork](https://github.com/stormysmoke/easyccg) by [a company](https://quantumsense.ai/). Seems to be an adaptation of EasyCCG for its products[^2].
    - Last updated on 7 Jan 2018, as of writing.
- Subsequent works:
    - TBC

[^1]: This URL is from EasyCCG's [README](https://github.com/mikelewis0/easyccg/blob/master/README.md), which was last updated on 20 Aug 2014 as of writing.

[^2]: Perhaps some chatbot, inferring from a commit message.

**OpenCCG.**

- Description from its GitHub [README](https://github.com/OpenCCG/openccg/blob/master/README.md):

  > OpenCCG is a system for parsing and generating text using combinatory categorial grammar for syntax and hybrid logic dependency semantics[^3] for, well, the semantic representation.

  From [VisCCG Tutorial](http://www.utcompling.com/wiki/openccg/visccg-tutorial):

  > OpenCCG is a comprehensive system for writing, editing, and running grammars in the Combinatory Categorial Grammar (CCG) framework.

  Characteristics:
  - Written mainly in Java.
  - Offers itself as a Java library (I haven't been able to find a documentation or tutorial on its API yet though).

- Resources:
  - Source & binaries: <https://github.com/OpenCCG/openccg>
    - Last updated on 17 Jul 2019, as of writing.

- Documentation:
  - Website: <http://openccg.sourceforge.net/>
    - *Caution.* The project itself has moved to GitHub.
  - Wiki: <http://www.utcompling.com/wiki/openccg>
  - An external [tutorial](https://davehowcroft.com/post/getting-started-with-openccg/), dated 5 Jul 2017.

[^3]: *Hybrid logic dependency semantics* refers to the work [Bal02].

### Other works

- [Søg16]. Scores lower than CVT and 'LSTM CCG Parsing' above but still competitively on 'CCG Supertagging on CCGBank' [pwcCSC].

**NLTK.**

- Uses:
  - [According to Yoshikawa](https://github.com/masashi-y/depccg#acknowledgement), it's useful for pretty printing parse derivations.

- TBC (<nltk.org>).

## Datasets

<!--Groningen Meaning Bank-->

<!-- https://esslli2016.unibz.it/wp-content/uploads/2015/10/MeaningBanking.pdf -->

## Misc. resources

- Some Yale lecture slides on CCG. <http://www.cs.yale.edu/homes/radev/nlpclass/slides2017/264.pdf>

## TODO

- LSTM CCG Parsing (NAACL 2016). It's DL CCG Parsing, and also #2 on [pwcCSC].

- Hierarchically-Refined Label Attention Network for Sequence Labeling (EMNLP 2019). #3 on [pwcCSC].

- Supertagging With LSTMs (NAACL 2016). #4 on [pwcCSC].

- Deep-Syntactic Parsing (COLING 2014).

- C&C Parser

- CCGBank

- Gronningen Tree Bank.
  - See also <https://developer.ibm.com/exchanges/data/all/groningen-meaning-bank/>

- ccg2lambda

- StatCCG

- Check up <https://aclweb.org/aclwiki/Combinatory_Categorial_Grammar#StatCCG>.

- Check out <https://mynlp.is.s.u-tokyo.ac.jp/en/projects>.

- Check out <https://esslli2016.unibz.it/wp-content/uploads/2015/10/MeaningBanking.pdf>.

- Consistent CCG Parsing over Multiple Sentences for Improved Logical Reasoning. NAACL 2018. Yoshikawa *et al.*

- Parsing Combinatory Categorial Grammar via Planning in Answer Set Programming. In *Correct Reasoning*, 2012.

- Translate Japanese into Formal Languages with an Enhanced Generalization Algorithm. SAI 2020. Kazuaki Kashihara.

- Flexible Combinatory Categorial Grammar Parsing Using the CYK Algorithm and Answer Set Programming. LPNMR 2013.

- Korean Combinatory Categorial Grammar and Statistical Parsing. 2002.

- (Old) Korean CCG papers.

## References

- [Bal02] Jason Baldridge and Geert-Jan Kruijff. "Coupling CCG and Hybrid Logic Dependency Semantics". ACL 2002. <http://dx.doi.org/10.3115/1073083.1073137>

- [Cla18] Kevin Clark, Thang Luong, Christopher D. Manning, Quoc V. Le. "Semi-Supervised Sequence Modeling with Cross-View Training". EMNLP 2018. <https://arxiv.org/abs/1809.08370>

- [Lew15] Mike Lewis, Luheng He and Luke Zettlemoyer. "Joint A* CCG Parsing and Semantic Role Labelling". EMNLP 2015. <http://dx.doi.org/10.18653/v1/D15-1169>

- [Lew14] Mike Lewis and Mark Steedman. "A* CCG Parsing with a Supertag-factored Model". EMNLP 2014. <http://dx.doi.org/10.3115/v1/D14-1107>

- [Søg16] Anders Søgaard and Yoav Goldberg. "Deep multi-task learning with low level tasks supervised at lower layers". ACL 2016. <http://dx.doi.org/10.18653/v1/P16-2038>

- [Yosh17] Masashi Yoshikawa, Hiroshi Noji, Yuji Matsumoto. "A* CCG Parsing with a Supertag and Dependency Factored Model". ACL 2017. <http://dx.doi.org/10.18653/v1/P17-1026>

- [Yosh18] Masashi Yoshikawa, Koji Mineshima, Hiroshi Noji, Daisuke Bekki. "Consistent CCG Parsing over Multiple Sentences for Improved Logical Reasoning". NAACL 2018. <http://dx.doi.org/10.18653/v1/N18-2065>

- [Yosh19] Masashi Yoshikawa, Hiroshi Noji, Koji Mineshima, Daisuke Bekki. "Automatic Generation of High Quality CCGbanks for Parser Domain Adaptation". ACL 2019. <http://dx.doi.org/10.18653/v1/P19-1013>

- [pwcCSC] Leaderboard for *CCG Supertagging on CCGBank*. <https://paperswithcode.com/sota/ccg-supertagging-on-ccgbank>

- [pwcDPPT] Leaderboard for *Dependency Parsing on Penn Treebank*. <https://paperswithcode.com/sota/dependency-parsing-on-penn-treebank>

*Footnotes.*
