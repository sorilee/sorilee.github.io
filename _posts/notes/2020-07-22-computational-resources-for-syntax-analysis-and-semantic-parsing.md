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

**Consistent CCG Parsing over Multiple Sentences for Improved Logical Reasoning.**

- [[Yosh18]](https://www.aclweb.org/anthology/N18-2065.pdf)

**ud2ccg.**

- A domain adaptation method for Combinatory Categorial Grammar (CCG)
parsing [[Yosh19]](https://www.aclweb.org/anthology/P19-1013.pdf).
  - Independent of specific parser architecture.
- Resources:
  - Repository: <https://github.com/masashi-y/ud2ccg>
    - Last updated on 10 Jun 2019, as of writing.

**depccg.**

- A CCG parser. Product of a 2017 research [[Yosh17]](https://www.aclweb.org/anthology/P17-1026.pdf).
  - The paper considers English and Japanese.
  - Written in Python and C++11.
- Resources:
  - Repository: <https://github.com/masashi-y/depccg>
    - [License](https://github.com/masashi-y/depccg/blob/master/LICENSE): MIT
  - PyPI: <https://pypi.org/project/depccg/>
  - Pre-trained English parsers: [listed](https://github.com/masashi-y/depccg/blob/master/README.md#using-a-pretrained-english-parser) in depccg's README.
  - Pre-trained Japanese parser: [described](https://github.com/masashi-y/depccg/blob/master/README.md#using-a-pretrained-japanese-parser) in depccg's README.

**EasyCCG.**

- A CCG parser. Product of a 2014 research [[Lew14]](https://www.aclweb.org/anthology/D14-1107.pdf).
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

- *OpenCCG is a system for parsing and generating text using combinatory categorial grammar for syntax and hybrid logic dependency semantics for, well, the semantic representation.*[^3]
  - 'Hybrid logic dependency semantics' refers to the work [Bal02].

- Code availability:
  - Source & binaries: https://github.com/OpenCCG/openccg
    - Last updated on 17 Jul 2019, as of writing.

- Website: <http://openccg.sourceforge.net/>
  - *Caution.* The project itself has moved to GitHub.

[^3]: Description from <https://github.com/OpenCCG/openccg/blob/master/README.md>.

**NLTK.**

- Uses:
  - [According to Yoshikawa](https://github.com/masashi-y/depccg#acknowledgement), it's useful for pretty printing parse derivations.

## Datasets

<!--Groningen Meaning Bank-->

<!-- https://esslli2016.unibz.it/wp-content/uploads/2015/10/MeaningBanking.pdf -->

## Misc. resources

- Some Yale lecture slides on CCG. <http://www.cs.yale.edu/homes/radev/nlpclass/slides2017/264.pdf>

## References

- [Bal02] Jason Baldridge and Geert-Jan Kruijff. "Coupling CCG and Hybrid Logic Dependency Semantics". ACL 2002. <http://dx.doi.org/10.3115/1073083.1073137>

- [Lew14] Mike Lewis and Mark Steedman. "A* CCG Parsing with a Supertag-factored Model". EMNLP 2014. <http://dx.doi.org/10.3115/v1/D14-1107>

- [Yosh17] Masashi Yoshikawa, Hiroshi Noji, Yuji Matsumoto. "A* CCG Parsing with a Supertag and Dependency Factored Model". ACL 2017. <http://dx.doi.org/10.18653/v1/P17-1026>

- [Yosh18] Masashi Yoshikawa, Koji Mineshima, Hiroshi Noji, Daisuke Bekki. "Consistent CCG Parsing over Multiple Sentences for Improved Logical Reasoning". NAACL 2018. <http://dx.doi.org/10.18653/v1/N18-2065>

- [Yosh19] Masashi Yoshikawa, Hiroshi Noji, Koji Mineshima, Daisuke Bekki. "Automatic Generation of High Quality CCGbanks for Parser Domain Adaptation". ACL 2019. http://dx.doi.org/10.18653/v1/P19-1013

*Footnotes.*
