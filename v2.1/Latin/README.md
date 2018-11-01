## Latin Dependency Treebank 2.1

This repository contains the data for the Latin Dependency Treebank 2.1. It comprises the data available 
in the older version plus new texts. Information about the editions of the texts can be found within the files.
The currently available texts are:

Author | Text 
------------ | ------------- 
Augustus | Res Gestae
Caesar | Commentarii de Bello Gallico (2.1-2.3; 2.5; 2.7; 2.9; 2.14-2.18; 2.32-2.33)
Cicero | In Catilinam (1.1-2.11) 
Jerome | Vulgata 
Vergil | Aeneid (6.1-6.336) 
Ovid| Metamorphoses (1.1-1.778)
Petronius | Satyricon (26-78)
Phaedrus| Fabulae (1-3) 
Propertius | Elegiae (1.1-1.22)
Sallust | Bellum Catilinae
Suetonius | Life of Augustus (1-55) 
Tacitus | Historiae (1.1.21)

### DATA CREATION

The data have been semi-automatically annotated. The full tagset can be consulted in TAGSET.xml. Each word is specified for a number of attributes describing it. The @pos attribute is a 9-character long string where each character has a particular meaning depending on its position. In TAGSET.xml this logic is documented in all detail (the file is derived from the one used in Arethusa, the online annotation environment used for annotation). In TAGSET.txt there is a more easily readable version of the tagset.

Data have been annotated using the following guidelines:
* [Guidelines for the Syntactic Annotation of Latin Treebanks (1.3)](https://github.com/PerseusDL/treebank_data/blob/master/v1/latin/docs/guidelines.pdf) (GSALT)

In the present release the following new texts have been added:

* Res Gestae
* Historiae

Res Gestae, which were treebanked following a different annotation scheme (as for syntactic labels), have been automatically converted to the common annotation scheme of the GSALT (aporiae in the conversion may be present, in that). The original syntactic labels (see Harrington-tagset.pdf and Harrington-tagset-instructions.pdf) have been preserved in the attribute @hrngtn.

The following texts have undergone a major revision in order to improve their form and consistency within themselves and with the most recently annotated texts, i.e., Fabulae, Life of Augustus, and Historiae:

* In Catilinam
* Aeneis
* Commentarii de Bello Gallico
* Elegiae
* In Catilinam

More precisely, these texts have been modified thus:

* Addition of punctuation
* Addition of missing sentences and paragraphs
* Sentences restored in their correct order
* Enclitic particles (-que, -ve, -ne) restored in their correct position
* univerbated coordinating elements (neque, nec) 
* Part of speech chosen on the basis of Lewis-Short's A Latin Dictionary and - if problems arise - Allen and Greenough’s A New Latin Grammar
* Tagset correction for gerund and gerundive  
* Some corrections related to the distinction adjective/pronouns and deponent/passive
* APOS is annotated as appositive and not as apposition (i.e., the label is on the noun considered to be the appositive)
* Some corrections related to verbal valency, the distinction between adverbial/attributive participles, personal constructions (e.g., videor)
* Normalization of the use of AuxY and auxZ

The following texts lack the preceding modifications, but punctuation has been added:

* Bellum Catilinae
* Metamorphoses
* Satyricon
* Vulgata

The structure of the original XML files (i.e., the one according to the XML schema which is digested in the Perseids platform, where annotations are peformed) has been changed in order to make it more informative and easier to query. The <code>treebank</code> root element identifies the version of the release (<code>@version</code>) and the cts for each text (<code>@cts</code>). The (pseudo-TEI) <code>header</code> element
contains information/credits about the creation of the file. The <code>biblStruct</code> element contains information about the ancient author and text, which helps interpretation of <code>@cts</code>.

The original structure of <code>sentence</code> and <code>word</code> elements is preserved with some normalization concerning non-linguistically relevant nodes: <code>@span</code> has been deleted and some normalization has been applied to the display of cts:urn values within </code>sentence</code> (these values are available on a sentence level, and sometimes also on a word level). 

### ACKNOWLEDGMENTS

We are grateful to the work of Anastasia Mellano, whose contribution has been crucial to improve annotation consistency within the texts 
