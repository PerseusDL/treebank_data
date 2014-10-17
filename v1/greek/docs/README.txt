This is a README file for the Ancient Greek Dependency Treebank, version 1.7.


1. Preamble

	1.1 Source
	
		The Ancient Greek Dependency Treebank is available at:
		
		http://nlp.perseus.tufts.edu/syntax/treebank/
		
		
	1.2 License
	
		AGDT 1.7 is licensed under a Creative Commons Attribution- 
		NonCommercial-ShareAlike 2.5 License:
		
		http://creativecommons.org/licenses/by-nc-sa/2.5
		
		
2. Documentation

	2.1 Data Format
	
		The data given in this treebank is provided as an XML document.  Each 
		word contains six required attributes:
		
		id: This is a unique identifier, and corresponds to the word's linear 
		position in the sentence.  The first word in a sentence is given 
		id 1.
		
		cid: This is a canonical identifier for the word within the larger corpus.
		
		form: The token form of the word, in Beta Code.
		
		lemma: The base lemma from which the word is derived, in Beta Code.
		
		head: The id of the word's parent.  If a word depends on the sentence 
		root, its head is 0.
		
		relation: The syntactic relation between the word and its parent.  A 
		catalogue of syntactic tags can be found in the syntactic guidelines 
		described below.
		
		postag: The morphological analysis for the word.  This field is 9 
		characters long, and corresponds to the following morphological 
		features:
		
			1: 	part of speech
			
				n	noun
				v	verb
				t	participle
				a	adjective
				d	adverb
				l	article
				g	particle
				c	conjunction
				r	preposition
				p	pronoun
				m	numeral
				i	interjection
				e	exclamation
				u	punctuation
			
			2: 	person
			
				1	first person
				2	second person
				3	third person
			
			3: 	number
			
				s	singular
				p	plural
				d	dual
			
			4: 	tense
			
				p	present
				i	imperfect
				r	perfect
				l	pluperfect
				t	future perfect
				f	future
				a	aorist
			
			5: 	mood
			
				i	indicative
				s	subjunctive
				o	optative
				n	infinitive
				m	imperative
				p	participle
			
			6: 	voice
			
				a	active
				p	passive
				m	middle
				e	medio-passive
			
			7:	gender
			
				m	masculine
				f	feminine
				n	neuter
			
			8: 	case
			
				n	nominative
				g	genitive
				d	dative
				a	accusative
				v	vocative
				l	locative
			
			9: 	degree
			
				c	comparative
				s	superlative
			
			---
			
			For example, the postag for the noun "a)/ndra" is "n-s---ma-", 
			which corresponds to the following features:
			
			1: n	noun
			2: -
			3: s	singular
			4: -
			5: -
			6: -
			7: m	masculine
			8: a	accusative
			9: -

		
	
	2.2 Text
	
		AGDT 1.7 is comprised of 18 texts, in the following distribution:
		
		Hesiod, Shield of Heracles: 3,834 words
		Hesiod, Theogony: 8,106 words
		Hesiod, Works and Days: 6,941 words
		
		Homer, Iliad: 128,102 words
		Homer, Odyssey: 104,467 words

		Aeschylus, Agamemnon: 9,806 words
		Aeschylus, Eumenides: 6,380 words
		Aeschylus, Libation Bearers: 6,566 words
		Aeschylus, Persians: 6,270 words
		Aeschylus, Prometheus Bound: 7,058 words
		Aeschylus, Seven Against Thebes: 6,232 words
		Aeschylus, Suppliants: 5,949 words
		
		Sophocles, Ajax: 9,474 words
		Sophocles, Antigone: 8,751 words
		Sophocles, Electra: 10,489 words
                Sophocles, Oedipus Tyrannus: 11,185 words
		Sophocles, Trachiniae: 8,822 words
  
                Plato, Euthyphro: 6,097 words
		
		The editions of these texts are as follows:
		
		Hesiod. The Homeric Hymns and Homerica with an English Translation by 
		Hugh G. Evelyn-White. Works and Days. Cambridge, MA.,Harvard University 
		Press; London, William Heinemann Ltd. 1914.

		Homer. The Odyssey with an English Translation by A. T. Murray. 
		Cambridge, MA., Harvard University Press; London, William Heinemann, 
		Ltd. 1919.
		
		Homer. Homeri Opera in five volumes. Oxford, Oxford University Press. 
		1920.

		Aeschylus. Aeschylus, with an English translation by Herbert Weir Smyth,
		Ph. D. in two volumes. Cambridge. Cambridge, Mass., Harvard University 
		Press; London, William Heinemann, Ltd. 1926.  Including edits proposed by
                by Francesco Mambrini for Libation Bearers, Persians, Prometheus Bound,
		Seven Against Thebes, and Suppliant Women. 2012.
			
		Sophocles. Sophocles. Vol 1: Oedipus the king. Oedipus at Colonus. Antigone. 
		With an English translation by F. Storr. The Loeb classical library, 20. 
		Francis Storr. London; New York. William Heinemann Ltd.; The Macmillan Company. 1912. 		
                Including edits proposed by Francesco Mambrini. 2012.

		Sophocles. Sophocles. Vol 2: Ajax. Electra. Trachiniae. Philoctetes With an 
		English translation by F. Storr. The Loeb classical library, 21. Francis Storr. 
		London; New York. William Heinemann Ltd.; The Macmillan Company. 1913. 
                Including edits proposed by Francesco Mambrini. 2012.

                Plato. Platonis Opera, ed. John Burnet. Oxford University Press. 1903.

		The following document_ids in the treebank correspond to the following 
		works:

		Perseus:text:1999.01.0127			Hesiod (Shield of Heracles)
		Perseus:text:1999.01.0129			Hesiod (Theogony)
		Perseus:text:1999.01.0131			Hesiod (Works and Days)
		
		Perseus:text:1999.01.0133			Homer (Iliad)
		Perseus:text:1999.01.0135			Homer (Odyssey)

		Perseus:text:1999.01.0003			Aeschylus (Agamemnon)
		Perseus:text:1999.01.0005			Aeschylus (Eumenides)
		Perseus:text:9999.01.0006			Aeschylus (Libation Bearers)
		Perseus:text:9999.01.0008			Aeschylus (Prometheus Bound)
		Perseus:text:9999.01.0009			Aeschylus (Persians)
		Perseus:text:9999.01.0007			Aeschylus (Seven Against Thebes)
		Perseus:text:9999.01.0010			Aeschylus (Supplian Women)

		Perseus:text:1999.01.0183			Sophocles (Ajax)
                Perseus:text:9999.01.0013			Sophocles (Antigone)
                Perseus:text:9999.01.0012			Sophocles (Electra)
                Perseus:text:1999.01.0191			Sophocles (Oedipus Tyrannus)
                Perseus:text:9999.01.0011			Sophocles (Trachinae)


                urn:cts:greekLang:tlg0059.tlg001.perseus-grc1	Plato (Euthyphro)
		
	2.3 Annotation Standards

		This release of the treebank has been annotated according to the 
		guidelines specified in version 1.1 of the "Guidelines for the Syntactic 
		Annotation of the Ancient Greek Dependency Treebank (1.1)," found in 
		docs/guidelines.pdf
			  
		
	2.4 Authorship

		Aside from the scholarly treebanks of Aeschylus (ed., Francesco Mambrini),
                Plato (ed., Giuseppe G.A. Celano) and Sophocles (ed., Dan Libatique and 
                ed., Francesco Mambrini), each sentence in the Ancient Greek Dependency Treebank 
		is built from the efforts of two independent annotators (marked "primary" in the data) 
		reconciled by a third (marked "secondary").  We would like to recognize the contribution 
                of the following individuals toward its creation and thank them for their 
                commitment to the advancement of Classical scholarship:
	
		Jennifer Adams, James Artz, Jennifer Curtin, James C. D'Amico, W. B. Dolan, 
		Calliopi Dourou, Scott J. Dube, C. Dan Earley, J. F. Gentile, Francis Hartel, 
		Connor Hayden, Kenny Hickman, Tovah Keynton, Michael Kinney, Florin Leonte, 
		Alex Lessie, Daniel Lim Libatique, Brian Livingston, Viet Luong, Meg Luthin, 
		George Matthews, Molly Miller, Jack Mitchell, Skylar Neil, Robin Ngo, Jessica 
		Nord, Anthony D. Yates, Sam Zukoff and the Tufts University LAT-181 class 
		(Spring 2008).

		
		
