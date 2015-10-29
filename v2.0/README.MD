## Ancient Greek Dependency Treebank 2.0

This repository contains the data for the Ancient Greek Dependency Treebank 2.0. It comprises the data available 
in the older versions plus new texts. Detailed information of the editions of the texts can be found within the files.
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
Homer | Odyssey 
Lysias | Oration 1 
Lysias | Oration 14 
Lysias | Oration 15 
Lysias | Oration 23 
Plato | Euthyphro 
Plutarch | Alcibiades 
Plutarch | Lycurgus 
Polybius | Histories (1) 
Pseudo Apollodorus | Library (1.1.1-1.4.1)
Sophocles | Ajax
 | Antigone
 | Electra
 | Oedipus Tyrannus
 | Trachinae 
Thucydides | Histories (1)

### DATA CREATION

The data have been semi-automatically annotated. The full tagsets can be consulted here:

morphology:
* https://github.com/alpheios-project/arethusa-configs/blob/gcelano/configs/arethusa.morph/gr_attributes2.json

syntax:
* https://github.com/alpheios-project/arethusa-configs/blob/gcelano/configs/arethusa.relation/relations2.json

semantics:
* https://github.com/alpheios-project/arethusa-configs/tree/gcelano/configs/arethusa.sg/sg_labels

Data have been annotated using the following guidelines:
* [Guidelines for the Syntactic Annotation of the Ancient Greek Dependency Treebank (1.1)](http://nlp.perseus.tufts.edu/syntax/treebank/agdt/1.7/docs/guidelines.pdf) (GAGDT)
* [Guidelines for the Ancient Greek Dependecy Treebank 2.0](https://github.com/PerseusDL/treebank_data/tree/master/AGDT2/guidelines) (GSAAGDT)

The GAGDT 2.0 can be basically taken to be an extension of the GSAAGDT 1.1, by making them more stringent. The GAGDT 2.0 also allows
semantic annotation. Each annotation file specifies which guidelines have been adopted.


### ANNOTATORS

(in alphabetical order)

Giuseppe G. A. Celano, J. F. Gentile, Robert Gorman, Vanessa Gorman,
Jordan Hawkesworth, Yoana Ivanova, Tovah Keynton, Florin Leonte, Alex Lessie,
Daniel Lim Libatique, Meg Luthin, Francesco Mambrini, George Matthews,
Jack Mitchell, Molly Miller, Jessica Nord, Sean Stewart, Anthony D. Yates,
Polina Yordanova, and Sam Zukoff.
