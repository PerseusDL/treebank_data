This is a README file for the Latin Dependency Treebank, version 1.5.


1. Preamble

	1.1 Source
	
		The Latin Dependency Treebank is available at:
		
		http://nlp.perseus.tufts.edu/syntax/treebank/1.5
		
		
	1.2 License
	
		LDT 1.5 is licensed under a Creative Commons Attribution- 
		NonCommercial-ShareAlike 2.5 License:
		
		http://creativecommons.org/licenses/by-nc-sa/2.5
		
		
2. Documentation

	2.1 Data Format
	
		The data given in this treebank is provided as an XML document.  Each 
		word contains six required attributes:
		
		id: This is a unique identifier, and corresponds to the word's linear 
		position in the sentence.  The first word in a sentence is given 
		id 1.
		
		form: The token form of the word.
		
		lemma: The base lemma from which the word is derived.
		
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
			
			4: 	tense
			
				p	present
				i	imperfect
				r	perfect
				l	pluperfect
				t	future perfect
				f	future
			
			5: 	mood
			
				i	indicative
				s	subjunctive
				n	infinitive
				m	imperative
				p	participle
				d	gerund
				g	gerundive
				u	supine
			
			6: 	voice
			
				a	active
				p	passive
			
			7:	gender
			
				m	masculine
				f	feminine
				n	neuter
			
			8: 	case
			
				n	nominative
				g	genitive
				d	dative
				a	accusative
				b	ablative
				v	vocative
				l	locative
			
			9: 	degree
			
				c	comparative
				s	superlative
			
			---
			
			For example, the postag for the adjective "alium" is "a-s---ma-", 
			which corresponds to the following features:
			
			1: a	adjective
			2: -
			3: s	singular
			4: -
			5: -
			6: -
			7: m	masculine
			8: a	accusative
			9: -

		
	
	2.2 Text
	
		LDT 1.5 is comprised of excerpts from eight texts, in the following 
		distribution:
		
		Caesar:	1,488 words
		Cicero:	6,229 words
		Jerome:	8,382 words
		Ovid: 4,789 words
		Petronius: 12,474 words
		Propertius: 4,857 words
		Sallust: 12,311 words
		Vergil:	2,613 words
		
		The editions of these texts are as follows:
		
		Caesar, C. Julius, Commentarii Rerum in Gallia Gestarum VII: A Hirti 
		Commentarius VIII.  T. Rice Holmes (Oxford: Clarendon Press, 1914).
		
		Cicero, M. Tullius, Orationes.  Recognovit brevique adnotatione critica 
		instruxit Albertus Curtis Clark (Oxford: Clarendon Press, 1908).
		
		Jerome, Vulgate Bible.  Bible Foundation and On-Line Book Initiative.  
		ftp.std.com/obi/Religion/Vulgate. 
		
		Ovid, Metamorphoses.  Hugo Magnus (ed.) (Gotha: Friedr. Andr. Perthes, 
		1892).
		
		Petronius, Satyricon.  W. H. D. Rouse (ed.) (London: William Heinemann, 
		1913).
		
		Propertius, Charm. Vincent Katz (trans.) (Los Angeles: Sun and Moon 
		Press, 1995).
		
		Vergil, Bucolica, Aeneis, Georgica. The Greater Poems of Virgil. J. B. 
		Greenough (Boston: Ginn & Co., 1882).
		
		C. Sallusti Crispi Catilina, Iugurtha, Orationes et epistulae excerptae
		de historiis. Axel W. Ahlberg (Leipzig: Teubner, 1919).
		
		The following document_ids in the treebank correspond to the following 
		works:
		
		Perseus:text:1999.02.0002	Caesar (Commentarii de Bello Gallico)
		Perseus:text:1999.02.0010	Cicero (In Catilinam)
		Perseus:text:1999.02.0060	Jerome (Vulgata)
		Perseus:text:1999.02.0055	Vergil (Aeneid)
		Perseus:text:1999.02.0029	Ovid (Metamorphoses)
		Perseus:text:2007.01.0001	Petronius (Satyricon)
		Perseus:text:1999.02.0066	Propertius (Elegies)
		Perseus:text:2008.01.0002	Sallust (Bellum Catilinae)
		
	2.3 Annotation Standards

		This release of the treebank has been annotated according to the 
		guidelines specified in version 1.3 of the "Guidelines for the Syntactic 
		Annotation of Latin Treebanks," found in docs/guidelines.pdf
			  
		
	2.4 Authorship

		Each sentence in the Latin Dependency Treebank is built from the efforts
		of two independent annotators (marked "primary" in the data) reconciled
		by a third (marked "secondary").  We would like to recognize the 
		contribution of the following individuals toward its creation and thank
		them for their commitment to the advancement of Classical scholarship:
	
		James Artz, Calliopi Dourou, J. F. Gentile, Kenny Hickman, Alex Lessie, 
		Viet Luong, Meg Luthin, Molly Miller, Robin Ngo, Skylar Neil and the 
		Tufts University LAT-181 class (Spring 2008).

		
		