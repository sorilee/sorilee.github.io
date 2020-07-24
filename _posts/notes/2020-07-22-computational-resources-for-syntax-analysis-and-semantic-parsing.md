---
layout: post
date updated: 2020-07-24 KST
date created: 2020-07-22 KST
date: 2020-07-22 KST
author: Sori Lee
---

# Computational resources for syntax analysis and semantic parsing

Here I list computational resources on [syntax analysis](https://en.wikipedia.org/wiki/Parsing) and [semantic parsing](https://en.wikipedia.org/wiki/Semantic_parsing).

## Software or works with code

**EasyCCG.**

- A CCG parser. Product of a 2014 research [[Lew14]](https://www.aclweb.org/anthology/D14-1107.pdf).
  - Written in Java.
- Web demo: [http://4.easy-ccg.appspot.com/](http://4.easy-ccg.appspot.com/do_parse?sentence=Fruit+flies+like+a+banana&nbest=5)
- Code availability:
  - Source & binaries: <https://github.com/mikelewis0/easyccg>
    - Last updated on 11 Jul 2015, as of writing.
  - Pre-trained models:[^1] <https://drive.google.com/#folders/0B7AY6PGZ8lc-NGVOcUFXNU5VWXc>
  - A [fork](https://github.com/stormysmoke/easyccg) by [QuantumSense](https://quantumsense.ai/). Seems to be an adaptation of EasyCCG for their products[^2].
    - Last updated on 7 Jan 2018, as of writing.
- Subsequent works:
    - 
 TBC

[^1]: This URL is provided in <https://github.com/mikelewis0/easyccg/blob/master/README.md>, which is last updated on 20 Aug 2014 as of writing.

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

## Datasets

<!--Groningen Meaning Bank-->

<!-- https://esslli2016.unibz.it/wp-content/uploads/2015/10/MeaningBanking.pdf -->

## Misc. resources

- Some Yale lecture slides on CCG. <http://www.cs.yale.edu/homes/radev/nlpclass/slides2017/264.pdf>


## References

- [Bal02] Jason Baldridge and Geert-Jan Kruijff. "Coupling CCG and Hybrid Logic Dependency Semantics". ACL 2020. <http://dx.doi.org/10.3115/1073083.1073137>

- [Lew14] Mike Lewis and Mark Steedman. "A* CCG Parsing with a Supertag-factored Model". EMNLP 2014. <http://dx.doi.org/10.3115/v1/D14-1107>

*Footnotes.*
