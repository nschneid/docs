---
layout: base
title:  'Introduction'
permalink: ja/overview/introduction.html
---

# Introduction

The Japanese corpora annotated according to the UD annotation scheme will be obtained by conversion from several resources.

As a first step, we construct conversion rules on 'NTT Japanese phrase structure treebank' (Tanaka and Nagata 2013) on Mainichi Newspaper.
We also try to construct conversion rules on 'Balanced Corpus of Contemporary Written Japanese'(BCCWJ) (Maekawa et al. 2014) with third party annotations (Mori et al. 2014).

# Basic Policy

UD annotation scheme is far from Japanese linguistic researches for several layers.

## Word Unit

### Overview of Word Unit
Japanese sentences are not split into words or morphemes by spaces.
We have several word unit standards by corpus annotation schema or morphological analyzers' outputs.
The representative word unit standards are the following subsubsections.

### IPADIC word unit: 
This word unit standard was derived by the morphological analyzer ChaSen. IPADIC is one of morphological information annotated lexicon used in ChaSen.  The morphological analyzer MeCab is developed in 2001-2004. MeCab is independently developped from the lexicon. However, the default lexicon is IPADIC. NAIST-jdic is a successor of IPADIC. NAIST-jdic resolves the license issues in IPADIC. NAIST-jdic inherits the word unit definitiosn and POS tagset of IPADIC. 

### NINJAL UniDic word units: 
NINJAL (National Institute for Japanese Language and Linguistics, Japan) proposed several word unit standards for Japanese corpus linguistics such as minimum word unit, \alpha word unit, \beta word unit, M word unit and so on.  From 2002, they maintain a morporlogical information annotated lexicon UniDic, and propose three sorts of word unit standard:
- Short Unit Word (SUW): 
The standard is used as the most fine grained morpheme for the corpus statistics. The word unit is derived by MeCab with UniDic.
- Middle Unit Word (MUW): The standard is based on the left branching compound word construction. The word unit is based on phonological construction such as accent phrase and/or sequential voicing(連濁). The unit is derived by Comainu which is a wrapper program of MST parsing.
- Long Unit Word (LUW): The standard is composed "Bunsetsu(文節)" unit. LUW is nearly same as content or functional words bounded by bunsetsu boundaries and The unit is derives by SVM-based chunker such as YamCha or linear chain CRF chunker such as CRF++.

### JUMANdic word unit: 
This word unit standard was derived by the morphological analyzer JUMAN. The

### Analyzers


## Bunsetsu Unit (Base phrase)
We use NINJAL Short Unit Word (SUW) in UniDic. (ref. UniDic)

## PoS Tag

UD PoS for Japanese is obtained by conversion rules from UniDic PoS Tagset.

## Dependency Links

## Dependency Relations

# Background 
(To be written)

Here, we describe Japanese language resources such as basic language resources, PoS tagged lexicon/corpus, morphological analyzers, syntactic dependency annotations, semantic dependency annotations (or case frame annotations), syntactic phrase structure tree annotations.

## Basic Language Resources
* RWCP Corpus
* Kyoto Corpus
* EDR Corpus
* CSJ
* BCCWJ
* KNBC Corpus (free)
* Others

## PoS Tagsets (with lexicon, corpus)
* IPADIC POS Tagset (RWCP Corpus)
* Masuoka Takubo POS Tagset (Kyoto Corpus/JUMAN)
* UniDic POS Tagset (CSJ, BCCWJ)

## Syntactic Dependency Annotation Schema (with corpus), Syntactic Dependency Parser
* Kyoto Corpus Schema
* CSJ Schema
* BCCWJ-DepPara Schema
* Word Dependency by Mori (Mori et al. 2014)

* KNP
* CaboCha

## Semantic Dependency Annotation Schema (with corpus), Semantic Dependency Parser
* Kyoto Corpus Schema (on Mainichi Newspaper)
* NAIST Corpus Schema (on Mainichi Newspaper and BCCWJ)

* KNP
* YuCha
* ChaPas

## Syntactic phrase structure tree annotations
* NTT Japanese phrase structure treebank

## Other annotations (syntax related only)
* Scope of Negation for BCCWJ
* Passive Auxiliary Verb for BCCWJ

# Issues
* Both of Mainichi Newspaper and BCCWJ are non-free resources.

# Contributors

* Yusuke Miyao
* Hiroshi Kanayama
* Takaaki Tanaka
* Shinsuke Mori
* Sumire Uematsu
* Masayuki Asahara

# References

* Takaaki Tanaka and Masaaki Nagata. 2013. '[Constructing a Practical Constituent Parser from a Japanese Treebank with Function Labels](http://www.aclweb.org/anthology/W13-4913)' In Proceedings of the Fourth Workshop on Statistical Parsing of Morphologically-Rich Languages
* Kikuo Maekawa, Makoto Yamazaki, Toshinobu Ogiso, Takehiko Maruyama, Hideki Ogura, Wakako Kashino, Hanae Koiso, Masaya Yamaguchi, Makiro Tanaka, and Yasuharu Den. 2014. '[Balanced corpus of contemporary written Japanese](http://link.springer.com/article/10.1007/s10579-013-9261-0)'. Language Resources and Evaluation 48 (2), pp.345-371
* Shinsuke Mori, and Hideki Ogura and Tetsuro Sasada. 2014. '[A Japanese Word Dependency Corpus](http://www.lrec-conf.org/proceedings/lrec2014/pdf/42_Paper.pdf)' In Proceedings of the Ninth International Conference on Language Resources and Evaluation (LREC'14)

# Links
## Morphological Analyzer 
* JUMAN: http://nlp.ist.i.kyoto-u.ac.jp/index.php?JUMAN
* MeCab: http://mecab.googlecode.com/svn/trunk/mecab/doc/index.html
* KyTea: http://www.phontron.com/kytea/index-ja.html

## Lexicon for Morphological Analyzer 
* IPADIC legacy: http://sourceforge.jp/projects/ipadic/
* NAIST-jdic: http://sourceforge.jp/projects/naist-jdic/
* UniDic (contemporary): http://sourceforge.jp/projects/unidic/ will be moved to http://download.unidic.org/
* UniDic (modern): http://www2.ninjal.ac.jp/lrc/index.php?UniDic%2F%B6%E1%C2%E5%CA%B8%B8%ECUniDic
* UniDic (early middle): http://www2.ninjal.ac.jp/lrc/index.php?UniDic%2F%C3%E6%B8%C5%CF%C2%CA%B8UniDic

## Chunkers (for Bunsetsu Analysis)
* Comainu: http://comainu.org/
* CRF++: http://taku910.github.io/crfpp/
* YamCha: http://chasen.org/~taku/software/yamcha/

## Bunsetsu-based Syntactic Dependency Parser
* KNP: http://nlp.ist.i.kyoto-u.ac.jp/index.php?KNP
* CaboCha: http://taku910.github.io/cabocha/
* jdepp: http://www.tkl.iis.u-tokyo.ac.jp/~ynaga/jdepp/
* Yahoo! API: http://developer.yahoo.co.jp/webapi/jlp/da/v1/parse.html

## Bunsetsu-based Syntactic Dependency Annotation Corpus
* Kyoto Corpus: http://nlp.ist.i.kyoto-u.ac.jp/index.php?%E4%BA%AC%E9%83%BD%E5%A4%A7%E5%AD%A6%E3%83%86%E3%82%AD%E3%82%B9%E3%83%88%E3%82%B3%E3%83%BC%E3%83%91%E3%82%B9
* NAIST Text Corpus: https://sites.google.com/site/naisttextcorpus/
* Corpus of Spontaneous Japanese: http://pj.ninjal.ac.jp/corpus_center/csj/
* Balanced Corpus of Contemporary Written Japanese: http://pj.ninjal.ac.jp/corpus_center/bccwj/