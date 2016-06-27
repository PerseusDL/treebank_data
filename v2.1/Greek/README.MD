## Ancient Greek Dependency Treebank 2.1

This repository contains the data for the Ancient Greek Dependency Treebank 2.1. In this release no change has been made to the texts already contained in the version 2.0. Information about the editions of the texts can be found within the files.
The currently available texts are:

Author | Text 
------------ | ------------- 
Aesop | Fables (1.1-1.50) 
Aeschylus | Agamemnon 
 | Eumenides 
 | Libation Bearers 
 | Persians 
 | Prometheus Bound 
 | Seven Against Thebes 
 | Suppliants 
Athenaeus | The Deipnosophists (12-13) 
Diodorus Siculus | Library (11) 
Herodotus | Histories (1)
Hesiod | Shield of Heracles 
 | Theogony
 | Works and Days 
Homer | Iliad 
 | Odyssey 
Lysias | Oration 1 
 | Oration 14 
 | Oration 15 
 | Oration 23 
Plato | Euthyphro 
Plutarch | Alcibiades 
 | Lycurgus 
Polybius | Histories (1) 
Pseudo Apollodorus | Library (1.1.1-1.4.1)
Pseudo Homer |Hymn to Demeter
Sophocles | Ajax
 | Antigone
 | Electra
 | Oedipus Tyrannus
 | Trachinae 
Thucydides | Histories (1)

### DATA CREATION

The data have been semi-automatically annotated. They have been annotated manually, but many corrections have been performed automatically in order to improve consistency. Morphology has been annotated with the help of the Morpheus tagger. 

The full tagsets can be consulted in TAGSETS.xml.

Data have been annotated using the following guidelines:
* [Guidelines for the Syntactic Annotation of the Ancient Greek Dependency Treebank (1.1)](http://nlp.perseus.tufts.edu/syntax/treebank/agdt/1.7/docs/guidelines.pdf) (GSAAGDT)
* [Guidelines for the Ancient Greek Dependecy Treebank 2.0](https://github.com/PerseusDL/treebank_data/tree/master/AGDT2/guidelines) (GAGDT)

The GAGDT 2.0 can be considered as an extension of the GSAAGDT 1.1, by making them more stringent. The GAGDT 2.0 also allows
semantic annotation. Each annotation file specifies which of the above guidelines has been adopted.

This release of the data has mainly concerned normalization and harmonization with respect to Ancient Greek characters, XML structure, and morphological annotation.

The structure of the original XML files (i.e., the one according to the XML schema which is digested in the Perseids platform, where annotations are peformed) has been changed in order to make it more informative and easier to query. The <code>treebank</code> root element identifies the version of the release (<code>@version</code>) and the cts for each text (<code>@cts</code>). The (pseudo-TEI) <code>header</code> element
contains information/credits about the creation of the file. The <code>biblStruct</code> element contains information about the ancient author and text, which helps interpretation of <code>@cts</code>.

The original structure of <code>sentence</code> and <code>word</code> elements is preserved with some normalization concerning non-linguistically relevant nodes: <code>@span</code> and <code>@cid</code> have been deleted and some normalization has been applied to the display of cts:urn values within </code>sentence</code> (such values are available on a sentence level, and sometimes also on a word level). 

The texts have been checked/normalized for the Greek characters and the punctuation marks. The decomposed Greek forms (NFD) in <code>@artificial</code> (i.e., elliptical) nodes have been made composed (NFC). 

The <code>@form</code> and <code>@lemma</code> values for punctuation marks have been corrected and levelled: both values now contain the form of a punctuation mark and @postag contains u--------

The tagsets form morphology have been harmonized. Previous versions of the treebank had "participle" also as a part of speech. Now "participle" is only treated as a kind of mood. Similarly, all words with morphological category "exclamation" have been assigned the category "interjection". 

Some work is still needed in order to satisfactorily deal with the distinction adverb/particle.

A major effort has been put to correct errors contained in <code>@postag</code> for nouns. Some problems remains for those nouns
which have not been annotated properly (missing values), which will have to be corrected manually.

### ANNOTATORS

(in alphabetical order)

Giuseppe G. A. Celano, J. F. Gentile, Robert Gorman, Vanessa Gorman,
Jordan Hawkesworth, Yoana Ivanova, Tovah Keynton, Florin Leonte, Alex Lessie,
Daniel Lim Libatique, Meg Luthin, Francesco Mambrini, George Matthews,
Jack Mitchell, Molly Miller, Jessica Nord, Sean Stewart, Anthony D. Yates,
Polina Yordanova, and Sam Zukoff.
