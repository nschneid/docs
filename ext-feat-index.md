---
layout: base
title:  'Language-specific features'
---

# Language-specific features

In addition to the <a href="u/feat/index.html">universal set of features</a>,
it is desirable to recognize word features that are particular
to one language or a small group of related languages.
We also include here features that are not language-specific but rather treebank-specific.
They encode something that could occur in many languages but only a few treebanks choose to tag it
(for example, whether a word is an abbreviation).

These features are not part of the core universal set
but if they appear in more than one language,
they should be encoded in all the languages identically.

For the universal features, there may be additional language-specific values that are not (yet) defined at the universal level.

Features that have brackets in their name (such as `Gender[psor]`) are <a href="u/overview/feat-layers.html">layered features</a>.
It means that a feature applies more than once to a word, in layers. The layer is indicated in the brackets.
Layered features are clones of existing non-layered universal or language-specific features.
They have their own language-specific documentation that describes what is the meaning of the layer,
how the list of values is modified for the layer (if at all),
and provides layer-specific examples.

There are automatically generated approximate
<a href="tagset-conversion/">conversion tables</a>
from existing tagsets of various languages to the universal part-of-speech tags and universal + language-specific features.

## Abbr
* [Czech values](cs-feat/Abbr): Yes
* [Finnish values](fi-feat/Abbr): Yes
* [Interset](ext-feat/Abbr): Yes

## AdpType
* [Czech values](cs-feat/AdpType): Prep, Voc, Comprep
* [Interset](ext-feat/AdpType): Prep, Post, Circ, Voc

## ConjType
* [Czech values](cs-feat/ConjType): Oper
* [Interset](ext-feat/ConjType): Comp, Oper

## Connegative
* [Finnish values](fi-feat/Connegative): Yes

## Derivation
* [Finnish values](fi-feat/Derivation): Minen, Sti, Inen, Lainen, Ja, Ton, Vs, Ttain, Ttaa

## Foreign
* [Czech values](cs-feat/Foreign): Foreign, Fscript, Tscript
* [Finnish values](fi-feat/Foreign): Foreign, Fscript
* [Interset](ext-feat/Foreign): Foreign, Fscript, Tscript

## Gender[psor]
* [Czech values](cs-feat/Gender[psor]): Masc, Fem
* [Interset](ext-feat/PossGender): Masc, Fem

## Hyph
* [Czech values](cs-feat/Hyph): Yes
* [Interset](ext-feat/Hyph): Yes

## InfForm
* [Finnish values](fi-feat/InfForm): 1, 2, 3

## NameType
* [Czech values](cs-feat/NameType): Geo, Prs, Giv, Sur, Nat, Com, Pro, Oth
* [Interset](ext-feat/NameType): Geo, Prs, Giv, Sur, Nat, Com, Pro, Oth

## Number[psor]
* [Czech values](cs-feat/Number-psor): Sing, Plur
* [Finnish values](fi-feat/Number-psor): Sing, Plur
* [Interset](ext-feat/PossNumber): Sing, Plur

## NumForm
* [Czech values](cs-feat/NumForm): Digit, Roman, Word
* [Interset](ext-feat/NumForm): Digit, Roman, Word

## NumValue
* [Czech values](cs-feat/NumValue): 1, 2, 3
* [Interset](ext-feat/NumValue): 1, 2, 3

## PartForm
* [Finnish values](fi-feat/PartForm): Pres, Past, Agt, Neg

## Person[psor]
* [Finnish values](fi-feat/Person-psor): 1, 2, 3
* [Interset](ext-feat/PossPerson): 1, 2, 3

## PrepCase
* [Czech values](cs-feat/PrepCase): Npr, Pre
* [Interset](ext-feat/PrepCase): Npr, Pre

## Style
* [Czech values](cs-feat/Style): Arch, Rare, Poet, Norm, Coll, Vrnc, Slng, Expr, Derg, Vulg
* [Finnish values](fi-feat/Style): Arch, Coll
* [Interset](ext-feat/Style): Arch, Rare, Poet, Norm, Coll, Vrnc, Slng, Expr, Derg, Vulg

## Typo
* [Finnish values](fi-feat/Typo): Yes
* [Interset](ext-feat/Typo): Yes

## Variant
* [Czech values](cs-feat/Variant): Short

# Interset features that are not part of this standard

The universal features are mostly derived from the
<a href="http://ufal.mff.cuni.cz/interset">Interset Project</a>
(<a href="http://ufal.mff.cuni.cz/~zeman/publikace/2008-02/tagdrivers-marrakech-styl-lrec.pdf">Zeman, 2008</a>).
Interset contains additional features that have not yet been adopted as
universal features. However, they may be used, if necessary, as part of the
"language-specific extensions" to the universal features.

The following Interset features are currently neither adopted as universal features,
nor have they been used in one of the languages as language- or treebank-specific features.

* <a href="u/ext-feat/AdvType.html">AdvType</a>
* <a href="u/ext-feat/Echo.html">Echo</a>
* <a href="u/ext-feat/NounType.html">NounType</a>
* <a href="u/ext-feat/PartType.html">PartType</a>
* <a href="u/ext-feat/Polite.html">Polite</a>
* <a href="u/ext-feat/Prefix.html">Prefix</a>
* <a href="u/ext-feat/PunctSide.html">PunctSide</a>
* <a href="u/ext-feat/PunctType.html">PunctType</a>
* <a href="u/ext-feat/VerbType.html">VerbType</a>

The following Interset features are not used under their Interset names but they are included
through the
<a href="http://universaldependencies.github.io/docs/u/overview/feat-layers.html">layered feature scheme</a>:

* <a href="u/ext-feat/PossedNumber.html">PossedNumber</a> = `Number[psee]`
* <a href="u/ext-feat/PossGender.html">PossGender</a> = `Gender[psor]`
* <a href="u/ext-feat/PossNumber.html">PossNumber</a> = `Number[psor]`
* <a href="u/ext-feat/PossPerson.html">PossPerson</a> = `Person[psor]`
* AbsPerson = `Person[abs]`
* ErgPerson = `Person[erg]`
* DatPerson = `Person[dat]`
* AbsNumber = `Number[abs]`
* ErgNumber = `Number[erg]`
* DatNumber = `Number[dat]`
* AbsPolite = `Polite[abs]`
* ErgPolite = `Polite[erg]`
* DatPolite = `Polite[dat]`
* ErgGender = `Gender[erg]`
* DatGender = `Gender[dat]`

The following features are included in the universal standard, but some values are missing there:

* <a href="u/feat/PronType.html"><tt>PronType</tt></a>`=Exc` … exclamative pronoun or determiner. It expresses the speaker's surprise towards the modified noun, e.g. _what_ in _<b>What</b> a surprise!_ In many languages, exclamative determiners are recruited from the set of interrogative determiners. Therefore, not all tagsets distinguish them. For instance, they are distinguished in Spanish (es::conll2009), Catalan (ca::conll2009) and Persian (fa::conll).
* New value 'opt' of the feature 'mood': optative mood in Ancient Greek and Turkish, to express wishes:
  "May you have a long life!" "If only I were rich!"
* New value 'des' of the feature 'mood': desiderative mood in Turkish: "He wants to come."
* New value 'nec' of the feature 'mood': necessitative mood in Turkish: "He must come. He should come."
* New value 'mid' of the feature 'voice': middle voice in Ancient Greek. (The mediopassive voice can be expressed as 'mid|pass'.)
* New value 'rcp' of the feature 'voice': reciprocal (Turkish "kar&#305;şt&#305;", "tutuştular")
* New value 'cau' of the feature 'voice': causative (Turkish "kar&#305;şt&#305;r&#305;yor" ("is confusing"))
* New value 'int' of the feature 'voice': intensive voice/aspect (the PIEL binyan) in Hebrew.
* New value 'gdv' of the feature 'verbform': gerundive (as opposed to the gerund) in Latin.
* New value 'dim' of the feature 'degree': diminutive (used for nouns e.g. in Dutch: _stoeltje, huisje, nippertje_)