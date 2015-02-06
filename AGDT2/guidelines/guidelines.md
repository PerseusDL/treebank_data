<a id="guidelines">

### GUIDELINES FOR THE ANCIENT GREEK DEPENDENCY TREEBANK 2.0 (beta version)

#### Giuseppe G. A. Celano

#### Tufts University &amp; Universität Leipzig

<a id="sum">

### Summary

*   1. [Introduction](#int)
*   2. [Morphological layer](#mph_tgs)
    *   2.1[ article](#art)
    *   2.2[ noun(/substantive)](#nou)
    *   2.3[ adjective](#adj)
    *   2.4[ pronoun](#prn)
    *   2.5[ verb](#vrb)
    *   2.6[ adverb](#adv)
    *   2.7[ adposition](#adp)
    *   2.8[ conjunction](#cnj)
    *   2.9[ numeral](#nmr)
    *   2.10[ interjection](#exc)
    *   2.11[ punctuation](#pct)
*   3.[ Syntactic layer](#prg_ann)
    *   3.1[ PRED](#pred)
    *   3.2[ SBJ](#sbj)
    *   3.3[ OBJ](#obj)
    *   3.4[ ATR](#atr)
    *   3.5[ ADV](#adv_fnc)
    *   3.6[ ATV/atvV](#atv)
    *   3.7[ PNOM](#pnom)
    *   3.8[ OCOMP](#ocomp)
    *   3.9[ COORD](#coord)
    *   3.10[ APOS](#apos)
    *   3.11[ MWE](#apos)
    *   3.12[ AuxP](#auxp)
    *   3.13[ AuxC](#auxc)
    *   3.14[ AuxX](#auxx)
    *   3.15[ AuxG](#auxg)
    *   3.16[ AuxK](#auxk)
    *   3.17[ AuxY](#auxy)
    *   3.18[ AuxZ](#auxz)
    *   3.19[ ExD](#exd)
    *   3.20[ Suffixes](#suffixes)
        *   3.20.1 [_CO](#_CO)
        *   3.20.2 [_AP](#_AP)
*   4.[ Advanced syntactic layer / semantic layer](#sg_ann)
    *   4.1[ Morphosyntactic tagset](#morphsyn_tagset)
         *   4.1.1[ Syntax of the case](#snt_cas)
            *   4.1.1.1[ Nominative](#nom)
                  *   4.1.1.1.1 [Dependent](#nmn_dpn)
                  *   4.1.1.1.2 [Independent](#nmn_ind)
                  *   4.1.1.1.3 [Citation](#nmn_ctc)
                  *   4.1.1.1.4 [Nominativus pendens](#nmn_pnd)
                  *   4.1.1.1.5 [Exclamation](#nmn_exc)
            *   4.1.1.2[ Genitive](#gnt)
            *   4.1.1.3[ Dative](#dtv)
            *   4.1.1.4[ Accusative](#acc)
            *   4.1.1.5[ Adposition](#prp)
         *   4.1.2[ Adjective proper](#adj_prp)
         *   4.1.3[ Substantive adjective](#sbs_adj)
         *   4.1.4[ Verbal adjective in τος/τεος](#vrb_adj)
         *   4.1.5[ Substantive verbal adjective in τος/τεος](#vrb_adj_sbs)
         *   4.1.6[ Substantive pronoun](#sbs_prn)
         *   4.1.7[ Adjective pronoun](#adj_prn)
         *   4.1.8[ Syntax of the finite verb](#fnt_moo)
         *   4.1.9[ Adjective participle](#adj_prt)
         *   4.1.10[ Substantive participle](#sbs_prt)
         *   4.1.11[ Syntax of the infinitive](#inf)
            *   4.1.11.1 [Dependent](#dpn_inf)
            *   4.1.11.2 [Independent](#idp_inf)
            *   4.1.11.3 [Articular infinitive](#art_inf)
            *   4.1.11.4 [Verbal infinitive](#vrl_inf)
         *   4.1.12[ Syntax of the adverb](#adv_snt)
            *   4.1.12.1 [Particles](#part)
            
</a>

<a id="int">

### 1. Introduction

The Ancient Greek Dependency Treebank 2.0 (AGDT 2.0) is an extension of the [Ancient Greek Dependency Treebank 1.0](http://nlp.perseus.tufts.edu/syntax/treebank/greek.html) (AGDT 1.0), which subsumes and integrates the morphosyntactic analysis available in the AGDT 1.0 with a more fine-grained annotation based on the categories identified in [H. W. Smyth's Greek Grammar for Colleges](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1&fromdoc=Perseus%3Atext%3A1999.04.0007) (SG).

Despite having being published at the beginning of the 20th century, SG turns out to be, in its foundations, a highly valuable compendium of Ancient Greek grammar, which is still widely used and consulted in the Anglo-Saxon world to study the Greek language. Because of its intermediate nature/size between a school grammar and a reference grammar, SG is particularly well suited to provide the framework which a computational model for Ancient Greek (AG) grammar can be built on. Such a computional model, which is outlined in the present guidelines, introduces modifications and integrations to SG to make it fully coherent, and consistent with more recent linguistic literature.

The AGDT 2.0 is organized into three layers: the morphological layer, the (Prague) syntactic layer, and the (SG) advanced syntax layer (which someone may want to call "semantic layer"). The first and the second layer were already present in the AGDT 1.0: they have been incorporated into the AGDT 2.0, even though modifications and corrections have been introduced, which are detailed in Section [2](#mph_tgs) and [3](#prg_ann).

The advanced syntax layer allows, by means of a complex algorithm relying on morphosyntax, the (guided) annotation of the syntax of the sentence as described by SG ([900](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+900&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2687](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&fromdoc=Perseus%3Atext%3A1999.04.0007)): this includes semantic roles (SRs) (such as "location", expressed, e.g., by the SG "genitive of place" or "dative of place"; see also [Luraghi 2003](http://www.worldcat.org/title/on-the-meaning-of-prepositions-and-cases-the-expression-of-semantic-roles-in-ancient-greek/oclc/227038149&referer=brief_results)) and the various types of subordinate clause. In the present guidelines, I will use the term "(morpho-)syntax" in Smyth's terms, i.e. to also include the analysis of what is usually described in some theoretical frameworks as belonging to a semantic layer. This is in accordance with the view that grammar consists of pairings of form and meaning, and not separate components (see, among others, [Langacker 1981-1991](http://www.worldcat.org/title/foundations-of-cognitive-grammar/oclc/13859017&referer=brief_results)). The SG annotation algorithm has been written in such a way that a certain SR can always be annotated at every grammar level (i.e., although "manner" can be expressed by a dative or an adverb or a PP, it is possible to label it in each case).

The advanced syntax annotation (also referred to, for convenience, as "SG annotation") is designed to complement the annotation of the Prague syntactic layer, i.e., a revised version of the analytical layer of the Prague Dependency Treebank 2.0, already adopted in the AGDT 1.0 (henceforth "Prague annotation"). The Prague analytical layer also informs the syntactic layer adopted in the [PROIEL](http://www.hf.uio.no/ifikk/english/research/projects/proiel/) annotation, which guarantees that the AGDT and the PROIEL treebank are to a very large extent compatible. The Prague annotation provides labels for (morpho-)syntactic categories, such as SBJ ("subject") or APOS ("apposition"), which, not being PoS-specific, can be kept out of the SG algorithm and superimposed on it. Moreover, the Prague syntactic layer comprises the annotation of the argument structure of verbs, adjectives, and adverbs, which is displayed in the distinction between OBJs and ADVs (see Section [3](#prg_ann)).

The present guidelines are devised in such a way that the reader is, whenever possible, referred to SG for a detailed definition and examples of a given grammar phenomenon, I focusing on the information that is strictly relevant to the annotation process. Wherever there is a discrepancy between SG and some instruction in the present guidelines, the latter get priority. For a small set of grammatical phenomena, more than one annotation option is licensed: a primary annotation style is kept distinct from a secondary annotation style, which, if chosen, has to be declared.

The language the guidelines focus on is Classical Greek: additions and adaptations for other stages of the language will follow.

In Section [2](#mph_tgs), I describe the morphological tagset. I define the Prague labels accompanied by links to key treebanking examples in Section [3](#prg_ann), which integrates/corrects the already existing guidelines for the [AGDT 1.0](http://nlp.perseus.tufts.edu/syntax/treebank/greek.html). In Section [4](#sg_ann), I deal with the SG algorithm of the advanced syntax layer (also called "semantic layer").

</a> 

<a id="mph_tgs">

### 2. Morphological layer

The morphological tagset consists of 11 categories, most of which can be identified on the basis of their lemmas in the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true). When annotating a PoS, the system allows addition of the lemma (_not word form_) translation for each word form (details, including the formalism, are provided below), in order to enable automatic creation of a gloss according to the [Leipzig Glossing Rules](http://www.eva.mpg.de/lingua/resources/glossing-rules.php) and allow connection with existing computational resources for the English language.

The lemma translation should be _as literal as possible_, _always the same whenever possible_, and _preferably taken from the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true)_ (or _[SG](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1&fromdoc=Perseus%3Atext%3A1999.04.0007)_): this is made easy because, in the [Perseus Digital Library](http://www.perseus.tufts.edu/hopper/collection?collection=Perseus:collection:Greco-Roman), the reader can access the LSJ lemma of a Greek word form contained in a text by clicking on it. Moreover, if that exact word form is quoted in the dictionary, it is showed in bold characters.

In the annotation environment "Arethusa", the morphological annotation of each word is performed using the "morph" tab. The annotator can there choose among the options that are automatically generated or add their own, if the right analysis is not available. It is to be noted that the automatically generated options are the output of the tagger Morpheus (also available in 
[Perseus](http://www.perseus.tufts.edu/hopper/morph?redirect=true&lang=greek)), which can contain inconsistencies or different analyses from the ones required for the present annotation. The annotator has therefore to pay much attention to annotate morphology only according to the present guidelines, without relying uncritically on Morpheus, but being ready to add a right morphologycal analysis, if missing. The PoS tagset is the following:

1.  [article](#art)
2.  [noun(/substantive)](#nou)
3.  [adjective](#adj)
4.  [pronoun](#prn)
5.  [verb](#vrb)
6.  [adverb](#adv)
7.  [adposition](#adp)
8.  [conjunction](#cnj)
9.  [numeral](#nmr)
10.  [interjection](#exc)
11.  [punctuation](#pct)

<a id="art">

#### 2.1 Article

AG has one definite article (SG [1118](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1118&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1189](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1189&fromdoc=Perseus%3Atext%3A1999.04.0007)), inflected and so annotated for gender, number, and case (ὁ, ἡ, τό). Note that in AG the same forms can also be used (_and hence should be accordingly annotated_) as 
[pronouns](#prn) (SG [1105](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1105&fromdoc=Perseus%3Atext%3A1999.04.0007); [1106](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1106&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1117](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1117&fromdoc=Perseus%3Atext%3A1999.04.0007)). The annotator should pay attention here, because the system tends not to suggest the pronominal analysis, which has to be added manually.

The article can have substantive-making power (SG [1153](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1153&fromdoc=Perseus%3Atext%3A1999.04.0007)). However, in phrases such as οἱ ἀμφί τινα or οἱ ἐκεῖ (i.e. when the article/pronoun is associated _with a PP_ or _an adverb_), ὁ is annotated as a pronoun (even though traditional grammar takes them as substantivized PPs and adverbs). This annotation style, which allows us to keep the SG algorithm more constrained, is made possible by analogy with examples such as τὰ τῶν στρατιωτῶν, where τῶν στρατιωτῶν is taken to be dependent on ὁ (and so the latter is a pronoun).

Although the forms τις-τι may have the force of an indefinite article (SG [1267](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1267&fromdoc=Perseus%3Atext%3A1999.04.0007)), they should not be annotated as articles but as [pronouns](#prn).

The lemma translation for article ὁ is `the`, while that for pronoun ὁ `that`.

The article always takes the Prague annotation label ATR; the pronoun takes the same syntactic labels as the [noun](#nou). There is no SG annotation for the article, while the pronoun has access to the algorithm for the [syntax of the case](#snt_cas).

</a>

<a id="nou">

#### 2.2 Noun(/Substantive)

In AG the noun/substantive (henceforth simply "noun") is inflected and so annotated for gender, number, and case (consult the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true)). If an adjective is also used as a noun, but is not lemmatized independently of the adjective lemma (i.e., no separate entry in the dictionary), _it is morphologically categorized as an adjective_.

The lemma translation for the noun should be an English noun (always in its singular form, wherever possible). Some examples are:

*   ὁδόν `way`
*   σωμάτων `body`
*   πολυρριζία `possession.of.many.roots` (when a translation includes more words, they should be joined by a full stop)
*   ποιμένος `shepherd`

The Prague annotation label for the noun can be SBJ, OBJ, ATR, ADV, PNOM, OCOMP, or APOS. The SG tagset allows the annotation of the [syntax of the case](#snt_cas) for each noun.

</a>

<a id="prn">

#### 2.3 Pronoun

The term "pronoun" is used here in its traditional definition, i.e. _as a cover term for both substantive and adjective pronouns_. Pronouns are a set of word forms, which are listed in SG ([325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[340](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&fromdoc=Perseus%3Atext%3A1999.04.0007)). The pronoun is annotated for gender, number, and case. The annotator should pay attention to the options suggested _because for some pronouns the erroneous PoS "adjective" is suggested_. This means that the right analysis as pronoun has to be added manually.

The lemma translation for the pronoun should be an English pronoun. Some examples are:

*   μοι `I`
*   αὐτοῦ `him` or `it` (depending on the genre)
*   αὐτῇ  `her`
*   αὐταί `herself`
*   τοῦδε `this`
*   τούτων `this`
*   ἑαυτῷ `himself`
*   ἐμός `my`
*   ἀλλήλαιν `one.another`

Consult the SG ([325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[340](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&fromdoc=Perseus%3Atext%3A1999.04.0007)) for the lemma translation, especially for correlative pronouns (SG [340](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&fromdoc=Perseus%3Atext%3A1999.04.0007)). Particular attention should be paid to relative and interrogative pronouns (used adjectively or substantively): a form can correspond to different kinds of pronouns: ὅς, ἥ, ὅ can, for example, be a demonstrative or a relative pronoun. In the LSJ different kinds of pronoun having the same form are usually lemmatized together, and the different functions are signalled in different sections with letters or numbers. Since it can be hard/impossible to detect the category "relative" and "interrogative" relying only on the morphological and syntactic annotation here adopted, the lemma field should contain this information. In order to make this task easier (instead of preserving the letters or numbers of the LSJ), the annotator will adopt the following notation in the lemma field:

*   `ὅς.R`
*   `ὅστις.R`
*   `ὅστις.I`

The notations `.R` or `.I` will be added to every lemma which is a relative or interrogative pronoun respectively. Note that the automated morphological annotation provided by the tagger Morpheus does not contain such notations: they have to be added manually.

If the pronoun is a substantive pronoun, one of the Prague annotation labels used for the [noun](#nou) applies, while if it is an adjective pronoun, one of the Prague annotation labels for the [adjective](#adj) in adjective function is used. The SG tagset allows us to specify if the pronoun is a [substantive pronoun](#sbs_prn) or an [adjective pronoun](#adj_prn). In the former case, the SG tagset allows annotation of its [syntax of the case](#snt_cas) (whose categories are the same as those for the [noun](#nou)). In the latter case, no further SG annotation is allowed (as occurs with any other [adjective](#adj) in adjective function).

</a>

<a id="adj">

#### 2.4 Adjective

The adjective is the PoS that is inflected and so annotated for gender, number, case, and degree, and is lemmatized as such in the 
[LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true).

The lemma translation for the adjective should be an English positive adjective (or, if this is not possible, an equivalent expression) or a noun, if appropriate. Some examples are:

*   εὐέλπιδος `hopeful`
*   ἱερός `temple` (when the adjective is substantivized and means "temple")
*   γυιαρκής `strengthening.the.limbs`
*   μακρότερος `small`
*   τάχιστος `quick`
*   πρότερος `former` (there is no positive adjective, so the translation can be a comparative)

The Prague annotation label is usually ATR, PNOM, or OCOMP, if the adjective has adjective function; on the contrary, if it is used as a substantive adjective, one of the Prague annotation labels for the [noun](#nou) is used. The SG tagset allows one to specify whether the adjective is also used as such or as a 
[substantive adjective](#sbs_adj). In the former case, no SG annotation is available; in the latter case, the SG annotation algorithm allows access to the same tagset for the 
[syntax of the case](#snt_cas) 
as that used for the [noun](#nou).

</a>

<a id="vrb">

#### 2.5 Verb

The verb is the PoS annotated for person, number, tense, mood, and voice (and gender and case if the verb is a participle), and is lemmatized as such in the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true). Note that the annotation of the voice of the verb is strictly morphological: the form of the voice is annotated as active, passive, or medio-passive (if the form can be both active and passive), independently of the meaning. It may happen that the Morpheus tagger outputs lemmas followed by a number: they should be deleted in the entry (i.e., lemma field).

The lemma translation for the adjective should be an English verb. A few examples are:

*   ἔρχομαι `come`
*   ἀβουλέω `be.unwilling`

if the verb is in a finite mood, it usually takes the Prague annotation labels PRED (main clause), SBJ or OBJ (substantive clause), ATR (adjective clause proper; if there is a substantivized relative clause, the labels are the same as those for the [noun](#nou)), or ADV (adverb clause). If the verb is a participle it can take the label ATR (attributive participle), ADV (circumstantial participle), OBJ, OCOMP, or PNOM (supplementary participle), or those for the [noun](#nou), if the participle is a substantive participle. Similarly, an infinitive can take the same labels as a noun if it is articular, and SBJ or OBJ (occasionally ADV), if it is "verbal". On the basis of the mood selected, i.e., whether the verb is in the indicative, subjunctive, optative, or imperative mood, i.e. a [finite mood](#fnt_moo), or in the [infinitive](#inf) or [participle](#adj_prt) mood, i.e., non-finite moods, the SG tagset allows annotation of its syntax through a complex algorithm (see Section [4](#sg_ann)).

</a>

<a id="adv1">

#### 2.6 Adverb

The adverb is morphologically defined as the PoS having an invariable form (with the exception of the degree feature; see SG ([341](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+341&fromdoc=Perseus%3Atext%3A1999.04.0007)–[346](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+346&fromdoc=Perseus%3Atext%3A1999.04.0007)) for an introduction on adverbs). Adverbs deriving from adjectives are not lemmatized independently in the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true), but are contained in the adjective lemma: _so the lemma for an adverb should be the corresponding adjective lemma_. There are, however, a great number of adverbs which are not related to an adjective form and so have an independent entry in 
[LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true) (and so, correspondingly, the lemma will be an adverb).

Sentence adverbs, which are labeled as particles in SG ([1094](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1094&fromdoc=Perseus%3Atext%3A1999.04.0007)), should be tagged as adverbs at the morphological level (the label "particle" is however available in the SG annotation). If a certain noun, adjective, or PP has attained the status of an adverb, _it has to be annotated as an adverb_. This occurs, for example, with the so-called adverbial accusative (SG [1606](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1606&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1611](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1611&fromdoc=Perseus%3Atext%3A1999.04.0007)) or the head of PPs such as πρὸ πολλοῦ (πρὸ πολλοῦ ποιεῖσθαι, "to esteem highly") or ἀφ᾽ οὗ ("since"). The annotator has to pay attention here, because the system sometimes suggests a nominal/adjectival analysis, which means that the adverbial analysis has to added manually.

The lemma translation should be an English adjective, if the Greek lemma is an adjective, or an English adverb. For the translation of correlative adverbs, see SG ([346](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+346&fromdoc=Perseus%3Atext%3A1999.04.0007)).

Sentence adverbs (i.e., some of those words that SG ([2769](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2769&fromdoc=Perseus%3Atext%3A1999.04.0007)) defines as particles) are not required to be translated. If the annotator decides to translate them (or some of them), this should be made in a consistent way and declared. Note that conjunctions (both coordinate and subordinate) are here treated as a separate category from particles (see [below](#cnj)).

 The Prague annotation label for the adverb is usually ADV, OBJ, AuxY, or AuxZ. The SG tagset allows specification of the SR expressed by the adverb.

</a>

<a id="adp">

#### 2.7 Adposition

Adposition is a cover term for preposition (SG [1636](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1702](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&fromdoc=Perseus%3Atext%3A1999.04.0007)) and postpositions (SG [1665](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1665&fromdoc=Perseus%3Atext%3A1999.04.0007)). Adpositions are morphologically identifiable by being a set of invariable word forms. Their list can be found in SG ([1636](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1702](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&fromdoc=Perseus%3Atext%3A1999.04.0007)), which includes both proper (SG [1636](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1698](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007)) and improper (SG [1699](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1699&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1702](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&fromdoc=Perseus%3Atext%3A1999.04.0007)) adpositions.

The lemma translation should be an English adposition (or an equivalent expression). Some examples are:

*   πρός `to`
*   πρός `toward`
*   πρός `according.to`
*   ἐν `according.to`
*   πρό `in.defence.of`

 Adpositions always take the Prague annotation label AuxP. There is no SG annotation available for adpositions.

</a>

<a id="cnj">

#### 2.8 Conjunction

The Conjunction is an invariable PoS, which can be morphologically defined as a word form belonging to a set. The list can be found in SG ([2163](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2163&fromdoc=Perseus%3Atext%3A1999.04.0007); _excluding the  inferential, causal, and some of the adversative conjunctions_ (such as _μέντοι_); _these are all treated here as adverbs_) and in SG ([2770](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2770&fromdoc=Perseus%3Atext%3A1999.04.0007)).

The lemma translation should be an English conjunction.

The Prague annotation allows the distinction between coordinating conjunctions (COORD) and subordinating conjunctions (AuxC) (AuxY is used with all conjunctions except the last one in a multi-conjunction [coordination](#coord)). No SG annotation is available for the conjunction.

</a>

<a id="nmr">  

#### 2.9 Numeral

The numeral is a word form belonging to the set defined by SG ([347](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+347&fromdoc=Perseus%3Atext%3A1999.04.0007)-[354](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+354&fromdoc=Perseus%3Atext%3A1999.04.0007)). A numeral is annotated for its type: cardinal, ordinal, or adverb. Cardinal and ordinal numerals are always taken to be [adjectives](#adj) (even when a cardinal is indeclinable), and so annotated for gender, number, and case (if declinable).

The lemma translation should be an English numeral.

Cardinal and ordinal numerals take the Prague annotation labels that [adjectives](#adj) take, while adverbs take the Prague labels reserved for [adverbs](#adv). The SG algorithm allows access to the options for [adjectives](#adj), if the numeral is cardinal or ordinal, or those for [adverbs](#adv), if the numeral is an adverb.

</a>

<a id="exc">  

#### 2.10 Interjection

The interjection is an invariable word form belonging to the set defined in Schwyzer-Debrünner (599-602) (consult also [LSJ](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true)).

The lemma translation should be an English interjection.

The interjection receives the syntactic label ExD. No SG annotation is available for interjections.

</a>

<a id="pct">  

#### 2.11 Punctuation

Punctuation marks are identifiable by being a set of forms (see SG ([188](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+188&fromdoc=Perseus%3Atext%3A1999.04.0007)) and include modern puntuation marks, such as inverted commas for direct speech). They are annotated because they are part of the edition of a text. Their annotation is however to be considered "technical", punctuation not being part of the morphosyntax of a sentence, but rather being able to function as a clue for syntactic phenomena: e.g., apposition is often preceded and followed by a comma.

 The Prague annotation labels for puntuation can be AuxX, AuxY, AuxK, AuxG, COORD (and APOS). There is no available SG annotation for punctuation marks.

</a>
</a>

<a id="prg_ann">

### 3. (Prague) syntactic layer

The syntactic layer allows annotation of traditional syntactic functions, such as the subject or the predicate nominal. Some of the labels, however, are used with a different meaning from the one adopted in traditional grammar. For example, the label ATR is here used to describe not only adjectives modifying nouns, but also any other kind of depend of the noun having the same or similar function (see below); the labels OBJ and ADV are meant to capture the argument structure of verbs, adjectives, and adverbs (see below). In the following, the terms "noun", "adjective", "verb", and "adverb" are sometimes used to mean the corresponding phrases. The following definitions are accompanied by links to key treebanking examples.

<a id="pred">

#### 3.1 PRED

The PRED ("predicate") function is reserved for the verb of the main clause in a sentence ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=1&doc=4971)) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&doc=4971)). Every sentence has one PRED only. Any other verb (finite and non-finite) takes a different label, which shows the function the verb has with respect to its linguistic parent ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=32&doc=4971)).

</a>

<a id="sbj">

#### 3.2 SBJ

The SBJ ("subject") label is attached to every subject (SG [927](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+927&fromdoc=Perseus%3Atext%3A1999.04.0007)–[943](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+943&fromdoc=Perseus%3Atext%3A1999.04.0007)) in a sentence. The subject is typically a noun (or one of its equivalents) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&doc=4971)), including the infinitive, both articular (SG [2025](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2025&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2034](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2034&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=40&doc=4971)) and verbal (SG [1984](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1984&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1985](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1985&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=2&doc=4971)), bearing the nominative case, or the genitive case (in the genitive absolute (SG [2070](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2070&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2075](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2075&fromdoc=Perseus%3Atext%3A1999.04.0007))) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&doc=4971)), or the accusative (in the infinitive clause (SG [1972](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1972&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1981](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1981&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&doc=4971)) or with the supplementary participle (SG [2106](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&fromdoc=Perseus%3Atext%3A1999.04.0007); [2112b](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2115](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&fromdoc=Perseus%3Atext%3A1999.04.0007); [2123](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&doc=4971))). The label SBJ can also apply to a substantive clause (SG [2574](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2574&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2575](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2575&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&doc=4971)) or a substantivized relative clause (SG [2488](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=7&doc=4971), which annotation is the default one, while the one with adjective clause + elliptical node has to be declared ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=34&doc=4971))).

</a>

<a id="obj">

#### 3.3 OBJ

The OBJ ("object") label is attached to any dependent which is taken to be an argument of the verb, adjective, or adverb (excluding, of course, arguments which are captured by other labels, such as SBJ). The concept of argument is notoriously difficult to define. As a broad definition, an OBJ argument is taken to be a constituent which is selected by a specific verb or class of verbs (and hence cannot accur with any other verb/class of verbs). For example, verbs of movement require a constituent meaning direction ("I went _to Rome_"), which cannot be used with any other verb: this is therefore an argument. On the contrary, a constituent meaning (time) simultaneous location ("I ate apples _yesterday_") is not an argument (but an ADV) in that it can virtually modify any kind of verb. If there are doubs, it may be useful to consult [Verbnet](http://verbs.colorado.edu/verb-index/index.php), which shows argument structure for English verbs. An OBJ argument can be a noun (or one of its equivalents) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=8&doc=4971)), a PP ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=9&doc=4971)), or an adverb([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=10&doc=4971)). An infinitive can also receive the label OBJ, both in the infinitive clause (SG [2016](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2016&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2024](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2024&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&doc=4971)) and as a complement of a verb (or an adjective) (SG [1989](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1989&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2007](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2007&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=37&doc=4971)). Similarly, a supplementary participle in indirect discourse (SG [2106](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&fromdoc=Perseus%3Atext%3A1999.04.0007), [2112](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2115](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&fromdoc=Perseus%3Atext%3A1999.04.0007), [2123](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&doc=4971)), a substantive clause (SG [2574](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2574&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2575](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2575&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&doc=4971)), including the εἰ-substantive clause (SG [2247](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2247&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=12&doc=4971)), and a substantivized relative clause (SG [2488](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&fromdoc=Perseus%3Atext%3A1999.04.0007)) can receive the label OBJ. 

</a>

<a id="atr">

#### 3.4 ATR

Any dependent of the noun (or one of its equivalents, excluding the substantive participle and the infinitive when they function as verbs), which is an article ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&doc=4971)), an adjective ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=9&doc=4971)),  or a noun (or one of its equivalents) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=14&doc=4971)) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=15&doc=4971)),  a PP ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=16&doc=4971)), or a relative clause ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&doc=4971)) receives the ATR ("attribute") function.

</a>

<a id="adv_fnc">

#### 3.5 ADV

The ADV ("adverbial") label is attached to any dependent which is taken to be an optional modification of the verb, the adjective, or the adverb. An ADV modification can be a noun (or one of its equivalents) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=18&doc=4971)),  a PP ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&doc=4971)), or an adverb ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&doc=4971)).  Adverb clauses (SG [2191](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2191&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2487](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&doc=4971)),  as well as a substantivized relative clause (SG [2488](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=20&doc=4971),  which annotation is the default one, while the alternative annotation style, i.e., adjective clause + elliptical node is to be declared ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=35&doc=4971))),  the infinitive of purpose and result (SG [2008](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&fromdoc=Perseus%3Atext%3A1999.04.0007)-[2011](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=41&doc=4971)),  and the circumstantial participle (SG [2054](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2054&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2087](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2087&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&doc=4971))  are ADV modifications as well.

</a>

<a id="atvv">

#### 3.6 ATV/AtvV

ATV/AtvV ("verbal attribute") is in the AGDT 1.0 the label for those adjectives agreeing with a subject but functioning as adjuncts. They are annotated as ADV and appended to the governing verb in the AGDT 2.0 ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=7&doc=4971)).  lternatively, according to the annotation style of the AGDT 1.0, they can receive the label ATV/AtvV and be appended to the subject/verb (see the guidelines for the [AGDT 1.0](http://nlp.perseus.tufts.edu/syntax/treebank/greek.html) for more information) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=36&doc=4971)).  This latter annotation style has to be declared.

</a>

<a id="pnom">

#### 3.7 PNOM

The PNOM ("predicate nominal") label applies to every noun ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&doc=4971)) (or one of its equivalents, including the infinitive (especially SG [1982](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1982&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1983](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1983&fromdoc=Perseus%3Atext%3A1999.04.0007))) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=39&doc=4971)) or adjective (including the adjective pronoun and the supplementary participle not in indirect discourse; SG [2094](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2105](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&fromdoc=Perseus%3Atext%3A1999.04.0007); [2123](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=21&doc=4971))) which are dependent on a copulative verb (SG [917](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+917&fromdoc=Perseus%3Atext%3A1999.04.0007)). 

</a>

<a id="ocomp">

#### 3.8 OCOMP

The function OCOMP ("object complement") is reserved for the predicative accusative (SG [1613](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1613&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1618](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1618&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=22&doc=4971)) and, more in general, any predicative complement not agreeing with the subject. It is also used with the supplementary participle not in indirect discourse with verbs of perceiving and finding (SG [2110](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2110&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2115](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&doc=4971)).

</a>

<a id="coord">

#### 3.9 COORD

The function COORD ("coordination") is reserved for coordinate conjunctions (the list can be found in SG [2163](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2163&fromdoc=Perseus%3Atext%3A1999.04.0007), _excluding the  inferential, causal, and some of the adversative conjunctions_ (_such as μέντοι_);_ these are all treated here as _(_sentence_) _adverbs_) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&doc=4971)) and commas coordinating two or more constituents when no conjunction is present (asyndeton) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&doc=4971)). If there are correlative conjunctions (or more coordinating commas without conjunctions), the last one by rule takes the function COORD, while the preceding ones take the technical label AuxY and are attached to the last one ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&doc=4971)). Every coordinated constituent takes the suffix _CO (if function words, such as AuxPs, are coordinated, the suffix is attached to their children).

</a>

<a id="apos">

#### 3.10 APOS

There are two possible annotations for apposition. In the first annotation style, the label APOS ("apposition"/"appositive") is attached to an appositive noun ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=27&doc=4971)) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=28&doc=4971)) (SG [916](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+916&fromdoc=Perseus%3Atext%3A1999.04.0007)) or an equivalent of an appositive noun (including a substantivized relative clause and a substantive or adverb clause (SG [976](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+976&fromdoc=Perseus%3Atext%3A1999.04.0007)–[995](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+995&fromdoc=Perseus%3Atext%3A1999.04.0007))) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=29&doc=4971)) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=30&doc=4971)), and the appositive is annotated as a dependent of the noun it specifies. Note that, according to this anotation style, the appositive is always a noun and annotated in the same way, independently of whether it functions as an attribute or is, for example, descriptive (see SG [976](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+976&fromdoc=Perseus%3Atext%3A1999.04.0007)–[995](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+995&fromdoc=Perseus%3Atext%3A1999.04.0007)). In the second annotation style, used in AGDT 1.0, the label APOS marks the comma separating a noun and its appositive, and the noun and its appositive take the function required within the sentence (with suffix _AP; see the [AGDT 1.0 guidelines](http://nlp.perseus.tufts.edu/syntax/treebank/agdt/1.7/docs/guidelines.pdf)); if the appositive is an attributive noun it is attached to the noun and labeled as ATR. If this second annotation style is adopted, it has to be declared. In the SG annotation (if the first annotation style for apposition is adopted) the analysis of an appositive noun is (technically) the same as that of the governing noun. The annotator should pay attention to the many examples of clauses in apposition to a noun, which have to be fully annotated: [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=52&doc=4971)

</a>

<a id="mwe">

#### 3.11 MWE

The label MWP is reseverd for multiword expressions. When there is an phrase where it is not clear which the function/meaning of the single words are, the head of that phrase takes the function of the phrase as a whole, while the other words are attached to it with the label MWE.

</a>

<a id="auxp">

#### 3.12 AuxP

The function AuxP ("preposition") is reserved for adpositions (whose list is in SG [1636](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1702](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&doc=4971)).

</a>

<a id="auxc">

#### 3.13 AuxC

The function AuxC ("conjunction") is used to label subordinate conjunctions only. Their list is in SG ([2770](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2770&fromdoc=Perseus%3Atext%3A1999.04.0007)) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&doc=4971)).

</a>

<a id="auxx">

#### 3.14 AuxX

AuxX is the label used for commas, unless they function as coodinating commas when no conjunction is present (in which case they take the [COORD](#coord) function ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&doc=4971)); when there is a coordination with conjunctions and commas, see the example in [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&doc=4971)). A non-coordinating comma is appended to its preceding word. If two commas mark a vocative or a parenthetical clause, they are both appended (with label AuxX) to the vocative and the head of the parenthetical clause respectively.

</a>

<a id="auxg">

#### 3.15 AuxG

The label AuxG is used for modern punctuation marks (other than commas) that can be found in an edition of Ancient Greek texts (such as inverted commas introducing direct speech).

</a>

<a id="auxk">

#### 3.16 AuxK

The label AuxK is used for the final punctuation mark of a sentence (which can be a period, a semicolon, or the point above the line). The node is always appended to the ROOT node ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&doc=4971)).

</a>

<a id="auxy">

#### 3.17 AuxY

The AuxY label is used to mark technical nodes (such as correlative conjunctions attached to the last one, which is taken to be the coordinating one: see [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&doc=4971) and [tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&doc=4971)) or for sentence adverbs (i.e., non-conjunction particles in SG ([1094](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1094&fromdoc=Perseus%3Atext%3A1999.04.0007)), but only those whose scope is the whole sentence).

</a>

<a id="auxz">

#### 3.18 AuxZ

The AuxZ label is reserved for logical operators that are adverbs, such as those meaning "not", "even", and "also".

</a>

<a id="exd">

#### 3.19 ExD

The label ExD is used for those constituents that do not syntactically belong to a sentence, such as vocatives and the head of a parenthetical clause. They are appended to the PRED node.

</a>

<a id="suffixes">

#### 3.20 Suffixes

Each syntactic label can be specified by a suffix. There are two main suffixes: _CO and _AP

<a id="_CO">

#### 3.20.1 _CO

The suffix _CO is added to all conjuncts in a coordination.

</a>

<a id="_AP">

#### 3.20.2 _AP

The suffix _AP is used _only_ if the second annotation style for apposition is chosen (which has to be declared). The suffix is attached to a noun and its appositive. There is also the variant _AP_CO, when there are coordinate appositives.

</a>

</a>

</a>

<a id="sg_ann">

### 4. (Smyth's Grammar) Advanced syntax layer / semantic layer

The advanced syntax layer allows annotation of the rich number of categories described by Smyth (1920). In some modern linguistic frameworks, some of these categories are described as morphosyntactic and some others as semantic.

<a id="morphsyn_tagset">  

### 4.1 Morphosyntactic tagset

The morphosyntactic tagset consists of those categories which, on the basis of the part of speech, can be defined if their syntax is also taken into account. I call such categories morphosyntactic. In the following list, the categories of the morphological tagset which give access to the morphosyntactic categories of the SG annotation are given in parentheses (the lack of a nested menu under a morphological tag means that no SG annotation is available). For those PoS having case, the case has to be re-selected at this layer, because the syntactic case can be different from the morphological one (see [below](#snt_cas)).
```
1.  (article)
2.  (noun/substantive)
      *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
3.  (adjective)
      *   [adjective proper](#adj_prp)
      *   [substantive adjective](#sbs_adj)
      *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
      *   [verbal adjective in τος/τεος](#vrb_adj)
      *   [substantive verbal adjective in τος/τεος](#vrb_adj_sbs)
      *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
      *   none of the above
      *   I do not know
4.  (pronoun)
      *   [substantive pronoun](#sbs_prn)
      *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
      *   [adjective pronoun](#adj_prn)
      *   none of the above
      *   I do not know
5.  (verb)
      *   (a finite mood, i.e., indicative, optative, subjunctive, and imperative)
            *   [<span style="font-style:italic">syntax of the finite verb</span>](#fnt_moo)
      *    (participle)
            *   [adjective participle](#adj_prt)
            *   [substantive participle](#sbs_prt)
                  *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
                  *   none of the above
                  *    I do not know
      *   (infinitive)
            *   [<span style="font-style:italic">syntax of the infinitive</span>](#inf)
6.  (adverb)
            *   [<span style="font-style:italic">syntax of the adverb</span>](#adv_snt)
7.  (adposition)
8.  (conjunction)
9.  (numeral)
        *   cardinal
            *   [adjective](#adj_prp)
            *   [substantive](#sbs_adj)
                  *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
                  *   none of the above
                  *   I do not know
         *   ordinal
               *   [adjective](#adj_prp)
               *   [substantive](#sbs_adj)
                     *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
               *   none of the above
               *   I do not know
         *   adverb
               *   [<span style="font-style:italic">syntax of the adverb</span>](#adv_snt)
10.  (interjection)
11.  (punctuation)
```
<a id="snt_cas">  

#### 4.1.1 Syntax of the case

In traditional grammar, the syntax of the case is concerned with the functions of the cases of the noun and 
its syntactic equivalents (the substantive pronoun, the substantive adjective, including the verbal ones in τος/τεος, the substantive participle, the articular infinitive, and the substantivized adjective clause; henceforth I will usually use the term "noun" to mean "noun" plus these syntactic equivalents). It deals with the distinction between, for example, an [accusative of the external object](#acc_aff) and an [accusative of respect](#acc_rsp). In the treebank 2.0, it is possible to fully annotate the syntax of the case by means of an elaborate algorithm. Most of the categories covered by the traditional syntax of the case are today treated under the rubric of semantic roles (in the following, the term "(semantic) function" is sometimes used as a synonym for "semantic role").

After the morphological annotation, the annotator is required to annotate the syntax of a noun, starting from the selection of the noun's syntactic case. Even though the syntactic case of a noun usually corresponds to its morphological case, there are some cases where this does not hold true: the so-called phenomenon of "attraction" of the relative pronoun (SG [2522](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2522&fromdoc=Perseus%3Atext%3A1999.04.0007)), for example, calls for a clear distinction between the morphology and the syntax of a case. Similarly, when a genitive or an accusative are analyzed as subjects or predicate nominals, the syntactic case selected should be the nominative.

The dependent and independent functions of each case are always kept distinct: "dependent" is a case function of a noun which is syntactically governed, while "independent" is a case function of a noun which is not syntactically dependent on any other word in the sentence. A noun with an independent function is very often, but not always, the head of a sentence, syntactic "independency" sometimes corresponding to a technical dependency in the treebank: e.g., a 
[nominativus pendens](#nmn_pnd) is technically attached to a PRED, although it is not syntactically dependent on it.

Following SG, the annotation algorithm distinguishes between main and adpositional functions for each case: e.g., the semantic function encoded by the 
[terminal accusative](#acc_trm) (accusative of direction) is a main function (because it can be expressed by the bare case), while an adpositional function is a semantic function that can be encoded only by a case plus an adposition (e.g., "cause" expressed by 
[διά + accusative](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007), which cannot be expressed by the bare accusative case). A case can sometimes express a main function also in conjunction with an adposition, which can define it more specifically: e.g., "direction" can also be encoded by, for example, 
[εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007) or 
[παρά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&fromdoc=Perseus%3Atext%3A1999.04.0007) + accusative. A main function, whether or not it is specified by an adposition, is _always_ annotated by selecting the relevant main function.

By contrast, a function that is shown as adpositional in the annotation algorithm is a semantic function that is always different from those expressed by the main functions (i.e., they cannot be expressed by the bare case). For the sake of perspicuity/simplicity, however, time and place SRs are all grouped together under the relevant non-adpositional function specific to each case (irrespective of the above criterion), with the exception of the genitive of separation and the terminal accusative, which are kept distinct from the genitive of place and the accusative of extent respectively, being in traditional grammar treated as separate categories.

All the instantiations for the adpositional case are grouped and algorithmically placed on the same level as the main functions, even when a certain adpositional function might have been subsumed under one of the main functions, being clearly derived from it: this is a technical expedient to keep all kinds of the adpositional case together, in that it is not possible to claim for a number of adpositional functions whether/from which main function they are derived. When accompanied by an adposition, the function of a case is technically annotated as belonging to the noun, without a claim that the case is the only bearer of the semantic function expressed by it and its governing adposition.

The annotator is _required_ to annotate the syntax of the case when the noun _only_ depends on 

*   (finite and non-finite) verb
*   verbal adjective in τος/τεος
*   substantive verbal adjective in τος/τεος
*   noun (and its equivalents)
*   an adposition depending on one of the above categories

When a case depends on any other part of speech, the option "none of the above" is to be selected. The latter option is made available because I do not attempt to provide guidelines for the annotation of dependents of the adjective and the adverb, which is, as is known, more controversial and so more difficult to rule. There are cases where the SG annotation of a noun depending on an adjective or an adverb is rather straightforward, but many others where it is not  (SG ([1413](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1413&fromdoc=Perseus%3Atext%3A1999.04.0007)) itself acknowledges this). Providing operational criteria for this latter kind of annotation is outside the scope of the present guidelines. However, the annotation environment "Arethusa" technically allows the annotation of a given SR also when a noun depends on an adjective or adverb: the annotator is free to also annotate it, provided that this is declared and the annotation criteria are documented.

The option "none of the above" is also to be selected when a PP expresses a SR whose annotation is not available (for a selection of SRs can currently be annotated only: see the list below). I have tried to design the algorithm in such a way that it is possible to annotate a certain SR wherever it appears within the clause, independently of its morphosyntactic realization (e.g., "cause" can always be annotated, whether it is expressed by a noun, an adverb, a PP, a participle, or a clause). Note, however, that, following SG and much literature on the subject, the semantics of the adjective, the nominative, and that of some kinds of genitive, dative, and accusative (such as the partitive genitive with verbs or the dative as direct complement of verbs) is not investigated (and so cannot be annotated), there being much less agreement on it. Providing operational criteria for this kind of annotation is outside the scope of the present release of the guidelines.

With the aforementioned limitations, the SRs that can be currently annotated are almost all the ones identified in SG. Greek examples for each SR can be read in the relevant sections in SG. In a few cases the definitions I provide below have been modified from the ones that can be found in SG. In the following table, I list (1) the SRs, (2) their definitions, (3) English examples to illustrate them (often literally taken from SG), (4) references to SG with Greek examples, and (5) additional remarks.

The SG sections referred to are only a few of the ones concerned with a given SR (e.g., there is no reference to sections dealing with PPs or clauses expressing the same SR, which can however be easily found in the rest of the document). My definitions are basically formulated following SG, with an attempt to make them compatible with the ones adopted in [Luraghi 2003](http://www.worldcat.org/title/on-the-meaning-of-prepositions-and-cases-the-expression-of-semantic-roles-in-ancient-greek/oclc/227038149&referer=brief_results), [Haspelmath 1997](https://www.worldcat.org/title/from-space-to-time-temporal-adverbials-in-the-worlds-languages/oclc/37670970&referer=brief_results) (relative to time SRs), and in [Verbnet](http://verbs.colorado.edu/verb-index/VerbNet_Guidelines.pdf). In general, the system of SRs that is lincesed in the present guidelines is more fine-grained than that in Luraghi 2003 and Verbnet. In the following definitions, I use the term "participant" as a cover term for any entity bearing a SR, and "event" as a cover term for any kind of action or state. Although the definitions are compatible with many of those adopted in Verbnet, there is no claim here about a structural hierarchy of SRs.

In the list I do not include the categories 
"divided whole" (SG [1306](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1306&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1319](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1319&fromdoc=Perseus%3Atext%3A1999.04.0007); [1341](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1371](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1371&fromdoc=Perseus%3Atext%3A1999.04.0007)), 
"subjective/objective genitive" (SG [1328](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1328&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1335](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&fromdoc=Perseus%3Atext%3A1999.04.0007)),
"dative of direct complement of verbs" (SG [1460](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1460&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1468](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1468&fromdoc=Perseus%3Atext%3A1999.04.0007); [1471](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1473](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&fromdoc=Perseus%3Atext%3A1999.04.0007)), 
"dative with the participle of inclination or aversion" (SG [1487](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1487&fromdoc=Perseus%3Atext%3A1999.04.0007)), 
"dative of the participle expressing time" (SG [1498](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&fromdoc=Perseus%3Atext%3A1999.04.0007)), 
object affected (SG [1551](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1562](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1562&fromdoc=Perseus%3Atext%3A1999.04.0007)), and
object effected ([1563](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1579](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1579&fromdoc=Perseus%3Atext%3A1999.04.0007)): they are grammatical categories rather than SRs. As stated above, their semantics cannot be annotated in the present version of the guidelines.

<table id="table_SR" style="border:1">
<caption>
              <span style="font-weight: bold">1. Table for semantic roles in AG</span>
            </caption>
<tr>
<th>Semantic role</th>
<th>Definition</th>
<th>English examples</th>
<th>Greek examples from SG</th>
<th>Remarks</th>
</tr>
<tr>
<td>accompaniment</td>
<td>participant that is followed or accompanied by another participant</td>
<td>I follow <span style="font-style: italic">you</span>

I went to Rome <span style="font-style: italic">with him</span>
</td>
<td>[1524](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1524&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1526](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1526&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>

<tr>
<td>accompanying circumstance</td>
<td>abstract participant that denotes the circumstance (but not the manner) accompanying an event</td>
<td/>
<td>[1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR should be selected only when the accompanying circumstance cannot be interpreted as a manner</td>
</tr>

<tr>
<td>advantage</td>
<td>animate participant (or participant composed of animate entities, such as "country") to whose advantage an event occurs</td>
<td>I work <span style="font-style: italic">for you</span>
              </td>
<td>[1481](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1485](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is also known as "beneficiary" in the literature</td>
</tr>

<tr>
<td>disadvantage</td>
<td>animate participant (or participant composed of animate entities, such as "country") to whose disadvantage an event occurs</td>
<td>I work <span style="font-style: italic">against you</span>
              </td>
<td>[1481](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1485](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>

<tr>
<td>agent</td>
<td>participant that causes an event intentionally or consciously</td>
<td>The cake was made <span style="font-style: italic">by him</span>
              </td>
<td>[1488](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1488&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1494](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>Due to the limitations stated above, this SR cannot be annotated when it is expressed by a nominative (the semantics of the nominative not being investigated in this version of the treebank)</td>
</tr>
<tr>
<td>friendly association</td>
<td>participant that is in a friendly relationship of association or intercourse with a (quasi-)symmetrical participant</td>
<td>
He associates <span style="font-style: italic">with you</span>;

He agrees <span style="font-style: italic">with you</span>
</td>
<td>[1523](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>If the verb is of speaking, the semantic role is "recipient or addressee"</td>
</tr>
<tr>
<td>hostile association</td>
<td>participant that is in a hostile relationship of association or intercourse with a (quasi-)symmetrical participant</td>
<td>
He fights <span style="font-style: italic">with you</span>
</td>
<td>[1523](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>If the verb is of speaking, the semantic role is "recipient or addressee"</td>
</tr>
<tr>
<td>cause</td>
<td>participant that is the occasion (external cause) or motive (internal cause) of an event, typically without its consciuosness or intentionality</td>
<td>
I was astonished <span style="font-style: italic">at that</span>;

I admire him <span style="font-style: italic">for</span> his <span style="font-style: italic">bravery</span>
</td>
<td>[1405](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1405&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1408](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&fromdoc=Perseus%3Atext%3A1999.04.0007); [1517](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1517&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1520](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>

<tr>
<td>conformity</td>
<td>participant specifying according to what something occurs</td>
<td>
<span style="font-style: italic">in accordance with</span> the <span style="font-style: italic">laws</span>
</td>
<td>[1688](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1688&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is only adpositional</td>
</tr>

<tr>
<td>connection</td>
<td>participant specifying with respect to what the following clause holds</td>
<td>
<span style="font-style: italic">as regards</span> a <span style="font-style: italic">wife</span>, if she conducts herself ill, etc.
</td>
<td>[1381](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is also used when a genitive expresses the SR of respect. Note that, contrary to SG, if a genitive expresses topic with verbs of saying or thinking (or similar verbs), the SR to be selected is "topic"</td>
</tr>
<tr>
<td>crime and accountability</td>
<td>participant that is the crime a participant is accused of</td>
<td>He was accused <span style="font-style: italic">of robbery</span>
              </td>
<td>[1375](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1375&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1379](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1379&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>(distinction and) comparison</td>
<td>participant to which another participant is compared</td>
<td>he is superior <span style="font-style: italic">to you</span> in eloquence</td>
<td>[1401](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1401&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1404](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1404&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>

<tr>
<td>explanation</td>
<td>participant that specifies by restriction the meaning of another participant</td>
<td>the city <span style="font-style: italic">Rome</span>
              </td>
<td>[1322](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1322&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>instrument or means</td>
<td>participant which is manipulated by an agent and through which an event occurs</td>
<td>he hit me <span style="font-style: italic">with</span> a <span style="font-style: italic">stone</span>
              </td>
<td>[1507](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1507&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1511](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1511&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>manner</td>
<td>participant that specifies how an event occurs</td>
<td>he reads <span style="font-style: italic">wonderfully</span>
              </td>
<td>[1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>SG definition ([1513](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1515](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&fromdoc=Perseus%3Atext%3A1999.04.0007)) of manner is not the one adopted here: SG defines manner as "measure of difference" and "respect", both of which are treated here as distinct SRs. My definition of manner basically coincides with SG definition of accompanying circumstance ([1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007)), excluding all those instances that cannot be strictly interpreted as manner specifications</td>
</tr>
<tr>
<td>material or contents</td>
<td>participant that is the material or contents of another participant</td>
<td>spring <span style="font-style: italic">of water</span>
              </td>
<td>[1323](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1323&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1324](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1324&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>measure</td>
<td>participant specifying the measure of space, time, or degree of a participant</td>
<td>provisions <span style="font-style: italic">of</span> five <span style="font-style: italic">days</span>
              </td>
<td>[1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1327](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&fromdoc=Perseus%3Atext%3A1999.04.0007); [1581](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This kind of SR, when governed by a pronoun, might be confused with the partitive genitive. The latter is more general, while the former only quantifies a measure of space, time, and degree (SG [1317](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1317&fromdoc=Perseus%3Atext%3A1999.04.0007) vs [1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)). Time can be annotated as a measure only within the genitive of measure.</td>
</tr>
<tr>
<td>measure of difference</td>
<td>participant that specifies the degree by which a participant differs from another participant in a comparison</td>
<td>many <span style="font-style: italic">days</span> later</td>
<td>[1513](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1515](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>(place) location</td>
<td>place where an event occurs</td>
<td>He lives <span style="font-style: italic">in Milano</span>
              </td>
<td>[1448](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1449](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&fromdoc=Perseus%3Atext%3A1999.04.0007); [1531](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1538](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&fromdoc=Perseus%3Atext%3A1999.04.0007); [1581](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>(place) path</td>
<td>place through which an event accurs</td>
<td>we moved <span style="font-style: italic">through</span> the <span style="font-style: italic">land</span>
              </td>
<td>[1581](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>(place) separation</td>
<td>place from where an event occurs</td>
<td>He went <span style="font-style: italic">from Austria</span> to Italy</td>
<td>[1392](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1400](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is also known in the literature as "source" or "ablative". In SG the genitive of separation is a broad category including both spatial and non-spatial separation. According to the present scheme, spatial separation is "separation &gt; concrete", while any other kind of metaphorical separation is labeled "sepratation &gt; figurative".</td>
</tr>
<tr>
<td>(place) terminal location/direction</td>
<td>place toward which an event occurs</td>
<td>He went from Austria <span style="font-style: italic">to Italy</span>
              </td>
<td>
[1448](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1449](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&fromdoc=Perseus%3Atext%3A1999.04.0007); 
[1531](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1538](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&fromdoc=Perseus%3Atext%3A1999.04.0007);    
[1588](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1589](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is also known as "goal" or "allative"</td>
</tr>
<tr>
<td>possession or belonging/possessor</td>
<td>participant that possesses or is interested in possessing another participant</td>
<td>
                <span style="font-style: italic">Areistotle's</span> books</td>
<td>[1297](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1297&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1305](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1305&fromdoc=Perseus%3Atext%3A1999.04.0007); [1476](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1476&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1480](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1480&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>The genitive of possession indicates possession, while the dative of possessor interest in possession</td>
</tr>
<tr>
<td>price and value</td>
<td>participant that indicates the price or value of another participant</td>
<td>he bought a table <span style="font-style: italic">for</span> much <span style="font-style: italic">money</span>
              </td>
<td>[1336](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1336&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1337](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&fromdoc=Perseus%3Atext%3A1999.04.0007); [1372](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1372&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1374](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1374&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>purpose</td>
<td>participant that is the aim of an event</td>
<td>He earned money <span style="font-style: italic">for him/that</span>
              </td>
<td>[1408](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>The SR "purpose" is usually inanimate. When the participant is animate, the context can help in distinguishing between purpose and beneficiary.</td>
</tr>
<tr>
<td>quality</td>
<td>participant that denotes a quality</td>
<td>I am <span style="font-style: italic">of</span> the same <span style="font-style: italic">opinion</span>
              </td>
<td>[1320](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1320&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1321](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1321&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>relation</td>
<td>animate participant that limits the meaning of an event</td>
<td>it is safer <span style="font-style: italic">for them</span> to flee</td>
<td>[1495](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR and that of "respect" can be distinguished on the basis of animacy</td>
</tr>
<tr>
<td>recipient or addressee</td>
<td>participant to which an event is directed</td>
<td>he told <span style="font-style: italic">me</span> that he was happy</td>
<td>[1469](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1469&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1470](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1470&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR prototypically depends on verbs of giving (recipient) and saying (addressee)</td>
</tr>
<tr>
<td>reference</td>
<td>participant in whose opinion an event holds good</td>
<td>pitful <span style="font-style: italic">in the eyes of many</span>
              </td>
<td>[1496](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1496&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1497](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1497&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>respect</td>
<td>inanimate participant that delimits the scope of a property or event</td>
<td>harsh <span style="font-style: italic">of voice</span>
              </td>
<td>[1516](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&fromdoc=Perseus%3Atext%3A1999.04.0007); [1600](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1605](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR can be expressed by the dative or the accusative. The SR of connection can be considered as a variant of it.</td>
</tr>
<tr>
<td>feeling</td>
<td>participant who shows participation/interest in an event to an interlocutor</td>
<td>study <span style="font-style: italic">me</span> how to please the eye</td>
<td>[1486](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1486&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>(time) simultaneous location</td>
<td>time at/in/on/during which an event occurs</td>
<td>
                <span style="font-style: italic">in</span> the <span style="font-style: italic">morning</span>

<span style="font-style: italic">at five</span>

<span style="font-style: italic">on</span> the first <span style="font-style: italic">day</span>

<span style="font-style: italic">during</span> that <span style="font-style: italic">day</span>
</td>
<td>[1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1447](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&fromdoc=Perseus%3Atext%3A1999.04.0007); 
[1539](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007);
[1582](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1587](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007)
</td>
<td>More examples and explanation in Haspelmath 1997:102–116</td>
</tr>
<tr>
<td>(time) sequential location</td>
<td>time before or after which an event occurs</td>
<td>
                <span style="font-style: italic">before</span>/<span style="font-style: italic">after</span> the <span style="font-style: italic">meal</span>
              </td>
<td>[1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1447](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>More examples and explanation in Haspelmath 1997:56–63</td>
</tr>
<tr>
<td>(time) sequential-durative</td>
<td>time by/until which an event occurs or since/from which an event has occurred/occurred</td>
<td>
<span style="font-style: italic">until midnight</span>

<span style="font-style: italic">since</span> the <span style="font-style: italic">Middle Ages</span>

<span style="font-style: italic">from now on</span>
</td>
<td>[1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1447](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&fromdoc=Perseus%3Atext%3A1999.04.0007); [1539](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007);
[1582](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1587](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007)
</td>
<td>More examples and explanation in Haspelmath 1997:66–78</td>
</tr>
<tr>
<td>(time) temporal distance</td>
<td>time in which an event occurred; or how long ago an event occurred</td>
<td>(I will return) <span style="font-style: italic">in</span> three <span style="font-style: italic">weeks</span>
 three <span style="font-style: italic">years ago</span>
</td>
<td>[1539](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>More examples and explanation in Haspelmath 1997:80–96</td>
</tr>
<tr>
<td>(time) temporal extent</td>
<td>time for which an event has occurred</td>
<td>
                <span style="font-style: italic">for</span> two <span style="font-style: italic">months</span>

I wrote the letter <span style="font-style: italic">in</span> two <span style="font-style: italic">hours</span>
</td>
<td>[1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1447](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&fromdoc=Perseus%3Atext%3A1999.04.0007);
[1539](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007);
[1582](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1587](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007)
</td>
<td>More examples and explanation in Haspelmath 1997:120–136</td>
</tr>
<tr>
<td>topic</td>
<td>participant that is the topic around which an event of communication or disputing occurs</td>
<td>He talked to me <span style="font-style: italic">about him</span>
              </td>
<td>[1380](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1381](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&fromdoc=Perseus%3Atext%3A1999.04.0007); [1409](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
<tr>
<td>source</td>
<td>participant that indicates the origin or the source of an event</td>
<td>
                <span style="font-style: italic">of Darius</span> and <span style="font-style: italic">Parysatis</span> were born two sons; 

I heard that from him</td>
<td>[1410](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1410&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1411](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td>This SR is also known as "origin" in the literature</td>
</tr>
<tr>
<td>standard of judgment</td>
<td>participant by which another participant is measured or judged</td>
<td>it was plain <span style="font-style: italic">from that</span>
              </td>
<td>[1512](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1512&fromdoc=Perseus%3Atext%3A1999.04.0007)</td>
<td/>
</tr>
</table>

In the following sections I show the algorithms underlying the annotation for each case and their explanation: as for grammar definitions, the reader will constantly be referred to the relevant SG sections.

<a id="nom">

#### 4.1.1.1 Nominative

The nominative is a grammatical case, which can encode different SRs: this is particularly clear if one considers the SR of the nominative of a passive verb, which 
can correspond to an accusative, or a genitive, or a dative depending on the same verb, when it is in the 
[active voice](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1745&fromdoc=Perseus%3Atext%3A1999.04.0007). How many and which SRs the nominative can encode is a controversial issue, and so there is no attempt to annotate them in the treebank 2.0: the annotation for the dependent nominative, either as a subject or a predicate nominal, is therefore empty (nominative &gt; dependent). The nominative should be used also when a genitive, a dative, or an accusative are syntactically equivalent to a nominative (for example, when a genitive is the subject or the predicate nominal in a genitive absolute; see also examples of attraction (SG [1060](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1062](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&fromdoc=Perseus%3Atext%3A1999.04.0007))). The following is the full algorithm for the nominative:

*   [dependent](#nmn_dpn)
*   [independent](#nmn_ind)

        *   [citation](#nmn_ctc)
    *   [nominativus pendens](#nmn_pnd)
    *   [exclamation](#nmn_exc)
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

#### <a id="nmn_dpn">4.1.1.1.1 Dependent</a>

The nominative is dependent if it is grammatically governed by another word in the sentence. In the treebank 2.0, the dependent nominative is annotated only for its syntact function (e.g., whether it is a subject or a predicate nominal), which is possible by using the labels of the Prague syntactic annotation.

#### <a id="nmn_ind">4.1.1.1.2 Independent</a>

Independent is a nominative which does not grammatically depend on another word in the sentence.

#### <a id="nmn_ctc">4.1.1.1.3 Citation</a>

The nominative of citation can occur in titles. It can also occur within a sentence (SG 
[940](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+940&fromdoc=Perseus%3Atext%3A1999.04.0007)), and so be (technically) attached to the word it specifies.

#### <a id="nmn_pnd">4.1.1.1.4 Nominativus pendens</a>

The nominativus pendens (SG 
[941](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+941&fromdoc=Perseus%3Atext%3A1999.04.0007)) is technically annotated as a dependent on the PRED verb.

#### <a id="nmn_exc">4.1.1.1.5 Exclamation</a>

The nominative of exclamation (SG 
[1288](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1288&fromdoc=Perseus%3Atext%3A1999.04.0007)) can be the head of a sentence or be technically dependent of another word when equivalent to a vocative.

</a> <!-- end nominative -->

<a id="gnt">

#### 4.1.1.2 Genitive

Three main functions are acknowledged for the bare genitive: the genitive proper, the ablatival genitive, and the genitive of time and place. Differently from SG, the algorithm for the genitive does not distinguish between genitives governed by a noun from those governed by a verb, because such a piece of information 
is expressed by the dependency annotation, which makes it explicit which the governor of a word is. Note that when the genitive is the subject or a predicate nominal in a genitive absolute, and hence is functionally equivalent to a nominative, the syntactic case selected should be the nominative. The same holds when the genitive is attracted (SG [1060](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1062](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&fromdoc=Perseus%3Atext%3A1999.04.0007)). If the genitive has the function of OCOMP (SG [2112](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&fromdoc=Perseus%3Atext%3A1999.04.0007)), the annotation ends with the selection of the dependent feature. The following is the algorithm for the genitive (with links referring to the SG sections of the noun-dependent and verb-dependent genitive, which distinction is lost at this level, it resulting from the tree structure). 

*   [dependent](#gnt_dpn) (SG [1289](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1289&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1406](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1406&fromdoc=Perseus%3Atext%3A1999.04.0007); [1408](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1449](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&fromdoc=Perseus%3Atext%3A1999.04.0007))

        *   genitive proper (noun: SG [1290](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1290&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1337](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&fromdoc=Perseus%3Atext%3A1999.04.0007); verb: SG [1341](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1390](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1390&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   genitive of possession or belonging (SG [1297](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1297&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1305](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1305&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of the divided whole (noun: SG [1306](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1306&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1319](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1319&fromdoc=Perseus%3Atext%3A1999.04.0007); verb: SG [1341](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1371](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1371&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of quality (SG [1320](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1320&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1321](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1321&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of explanation (SG [1322](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1322&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of material or contents (SG [1323](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1323&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1324](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1324&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   [genitive of measure](#msr) (SG [1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1327](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   time (SG [1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1327](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   space (SG [1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1327](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   degree (SG [1325](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1327](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   subjective/objective genitive (SG [1328](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1328&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1335](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   subjective genitive (SG [1330](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1330&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   objective genitive (SG [1331](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1331&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1335](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   genitive of price and value (noun: SG [1336](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1336&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1337](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&fromdoc=Perseus%3Atext%3A1999.04.0007); verb: SG [1372](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1372&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1374](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1374&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of crime and accountability (SG [1375](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1375&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1379](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1379&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   [genitive of topic](#tpc) (SG [1380](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1381](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&fromdoc=Perseus%3Atext%3A1999.04.0007); [1409](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   [genitive of connection](#cnn) (SG [1380](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1381](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   none of the above
        *   I do not know
    *   ablatival genitive (SG [1391](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1391&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1411](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   [genitive of separation](#spr) (SG [1392](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1400](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   concrete
            *   figurative
            *   none of the above
            *   I do not know
        *   genitive of distinction and comparison (SG [1401](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1401&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1404](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1404&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of cause (SG [1405](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1405&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1407](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1407&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   genitive of purpose (SG [1408](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   [genitive of source](#src) (SG [1410](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1410&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1411](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   none of the above
        *   I do not know
    *   genitive of time and place (SG [1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1449](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   genitive of time (SG [1444](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1447](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   simultaneous location
            *   sequential location
            *   sequential-durative
            *   temporal distance
            *   temporal extent
            *   none of the above
            *   I do not know
        *   genitive of place (SG [1448](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1449](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   location

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   direction

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   path

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know
    *   adpositional genitive

                *   (with [ἀπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),
            [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),           [ἐξ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007)) instrument or means
        *   (with [ἀπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),         [ἐξ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007),            [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007), [ὑπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007),            [παρά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&fromdoc=Perseus%3Atext%3A1999.04.0007)) agent
        *   (with [ἀπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),
            [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),           [ἐξ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007),
            [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007),          [ὑπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyfth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007),          [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) manner
        *   (with [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007)) friendly association
        *   (with [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007)) hostile association
        *   (with [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007), [ὑπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007)) accompaniment
        *   (with [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007), [ὑπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007)) accompanying circumstance
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007), [πρό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1694&fromdoc=Perseus%3Atext%3A1999.04.0007),          [ὑπέρ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1697&fromdoc=Perseus%3Atext%3A1999.04.0007), [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) advantage
        *   (with [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) disadvantage
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) reference
        *   (with [ἀπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),         [ἐξ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007),            [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007)) conformity
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   [independent](#gnt_ind)

        *   exclamation (SG [1407](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1407&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

#### <a id="gnt_dpn">4.1.1.2.1 Dependent</a>

Dependent is the genitive which is syntactically dependent on another word in the sentence.

#### <a id="msr">4.1.1.2.2 Genitive of measure</a>

The genitive of measure specifies the measure of time, space, or degree.

#### <a id="tpc">4.1.1.2.3 Genitive of topic</a>

This kind of genitive specifies the topic with verbs of saying and thinking, which it depends on (note that I deviate from SG here, because this SR corresponds to the first kind of SG genitive of connection (SG [1380](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&fromdoc=Perseus%3Atext%3A1999.04.0007)) and what is treated in SG at [1409](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&fromdoc=Perseus%3Atext%3A1999.04.0007))

#### <a id="cnn">4.1.1.2.4 Genitive of connection</a>

The genitive of connection delimits the scope of the following clause, i.e., prototypically specifies with respect to what the following clause holds. It corresponds only to a part of SG genitive of connection (only SG [1381](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&fromdoc=Perseus%3Atext%3A1999.04.0007)). Such kind of genitive is attached to the main verb of the clause it delimits. More generally, the genitive of connection is used here as an equivalent of the accusative/dative of respect, in that it can also specify in reference to/with respect to what the meaning of a verb (or verb phrase) holds.

#### <a id="spr">4.1.1.2.5 Genitive of separation</a>

The SR of the genitive of separation ("separation") is usually labeled "source" in modern linguistic literature (which term is here and in traditional grammar used to indicate "origin"). Even though in SG the bare genitive of separation is mainly treatead not as a local function, it is in the present guidelines: more precisely, spatial separation corresponds to "separation &gt; concrete", while for verbs meaning "cease", "release", "remove", "lack", etc. (see SG [1392](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1400](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&fromdoc=Perseus%3Atext%3A1999.04.0007)) select "separation &gt; figurative".

#### <a id="src">4.1.1.2.6 Genitive of source</a>

The SR expressed by the genitive of source is sometimes labeled "origin" in linguistic literature. 

#### <a id="gnt_ind">4.1.1.2.7 Independent</a>

A genitive is independent if it does not dependent on any other word, and so is the linguistic head of a sentence.

</a> <!-- end genitive -->

<a id="dtv">

#### 4.1.1.3 Dative

There exist three main kinds of bare dative: the dative proper, the instrumental dative, and the locative dative. When the dative has the function of a PNOM (SG [1060](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1062](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&fromdoc=Perseus%3Atext%3A1999.04.0007)), the syntactic case selected should be the nominative. The following is the algorithm for the dative: 

*   dependent (SG [1450](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1450&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1550](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1550&fromdoc=Perseus%3Atext%3A1999.04.0007))

        *   dative proper (SG [1457](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1457&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1498](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   dative as direct complement of verbs (SG [1460](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1460&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1468](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1468&fromdoc=Perseus%3Atext%3A1999.04.0007); [1471](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1473](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   [dative as indirect complement of verbs](#dat_ind_cmp) (SG [1469](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1469&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1470](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1470&fromdoc=Perseus%3Atext%3A1999.04.0007); [1471](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1473](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   dative of interest (SG [1474](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1474&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1494](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   dative of the possessor (SG [1476](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1476&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1480](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1480&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of advantage (SG [1481](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1485](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of disadvantage (SG [1481](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1485](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of feeling (SG [1486](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1486&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative with participle of inclination or aversion (SG [1487](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1487&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of agent (SG [1488](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1488&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1494](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   dative of relation (SG [1495](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1498](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   dative of relation proper (SG [1495](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of reference (SG [1496](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1496&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1497](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1497&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of the participle expressing time (SG [1498](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know

        *   instrumental dative (SG [1503](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1503&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1529](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1529&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   instrumental dative proper (SG [1506](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1506&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1520](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   dative of instrument or means (SG [1507](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1507&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1511](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1511&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of standard of judgment (SG [1512](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1512&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   [dative of manner](#dtv_mnn)
            *   dative of measure of difference (SG [1513](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1515](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of respect (SG [1516](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of cause (SG [1517](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1517&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1520](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   comitative dative (SG [1521](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1521&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1528](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   dative of friendly association (SG [1523](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of hostile association (SG [1523](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   dative of accompaniment (SG [1524](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1524&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1526](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1526&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   [dative of accompanying circumstance](#dtv_acc_crc) (SG [1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007))
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know

        *   locative dative (SG [1530](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1530&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   dative of place (SG [1531](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1538](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   location

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   direction

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   [path](#dtv_pth)

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   none of the above
            *   I do not know
        *   dative of time (SG [1539](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1543](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   simultaneous location
            *   sequential location
            *   sequential-durative
            *   temporal distance
            *   temporal extent
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know

        *   adpositional dative
            *   (with [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007)) purpose
        *   (with [ἐν](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1687&fromdoc=Perseus%3Atext%3A1999.04.0007),          [συν](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1696&fromdoc=Perseus%3Atext%3A1999.04.0007)) conformity
        *   (with [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007)) price and value
        *   (with [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007)) condition
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

#### <a id="dat_ind_cmp">4.1.1.3.1 Dative as indirect complement of verbs</a>

The dative of indirect complement of verbs is associated with the SR of recipient or addressee (with verbs of saying). Note that if a verb can take a dative as direct or indirect complement of a verb (as described in  SG [1471](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1473](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&fromdoc=Perseus%3Atext%3A1999.04.0007)), the annotator will label the dative  as a direct or an indirect complement according to the actual usage in a given sentence.

#### <a id="dtv_mnn">4.1.1.3.2 Manner</a>

The dative of manner is here meant to cover the SR of manner (according to my definition above), which SG associates with the "dative of accompanying circumstance" (SG [1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007)). In SG the dative of manner corresponds to a dative of measure of difference or dative of respect (see SG [1513](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1516](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&fromdoc=Perseus%3Atext%3A1999.04.0007)), both of which I consider separate categories here.

#### <a id="dtv_acc_crc">4.1.1.3.3 Dative of accompanying circumstance</a>

The dative of accompanying circumstance is to be selected when the SR expressed by the SG "accompanying circumstance" (SG [1527](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&fromdoc=Perseus%3Atext%3A1999.04.0007)) is not of "manner", as here conceived.

#### <a id="dtv_pth">4.1.1.3.4 Path</a>

"Path" partly corresponds here to what is labeled (dative of) "space and time" in SG ([1528](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&fromdoc=Perseus%3Atext%3A1999.04.0007)). Similarly, the dative of time treated in SG as a kind of instrumental/comitative dative (SG [1528](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&fromdoc=Perseus%3Atext%3A1999.04.0007)) has to be simply annotated with one of the categories under "dative of time".

</a> <!-- end dative -->

<a id="acc">

#### 4.1.1.4 Accusative

There are five main kinds of bare accusative: 
[internal object (object effected)](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&fromdoc=Perseus%3Atext%3A1999.04.0007), 
[external object (object affected)](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1590&fromdoc=Perseus%3Atext%3A1999.04.0007), 
[accusative of extent](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1580&fromdoc=Perseus%3Atext%3A1999.04.0007), 
[terminal accusative](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&fromdoc=Perseus%3Atext%3A1999.04.0007), and 
[accusative of respect](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&fromdoc=Perseus%3Atext%3A1999.04.0007). The so-called [adverbial accusative](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1606&fromdoc=Perseus%3Atext%3A1999.04.0007) is treated under the category 'adverb'. The accusative can express (1) one of 
these functions by itself or in conjunction with an adposition, which defines it more precisely, or (2) a new function in conjunction with an adposition (e.g., 'purpose'): in the former case, the function of the accusative is always annotated under one of the main functions, while in the latter case one of the adpositional functions should be used. Note that when the accusative is the subject or the predicate nominal in an infinitive clause, and hence is functionally equivalent to a nominative, the syntactic case selected should be the nominative. When the accusative has the function of OCOMP, the annotation process ends with the selection of the dependent feature (which parallels the annotation of the nominative as PNOM). The adverbial accusative should always be morphologically labeled as an adverb, so this kind of accusative is never annotated as a case. The algorithm for the accusative is the following:

*   [dependent](#acc_dpn) (SG [1551](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1598](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1598&fromdoc=Perseus%3Atext%3A1999.04.0007); [1600](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1635](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1635&fromdoc=Perseus%3Atext%3A1999.04.0007))

        *   [internal object](#acc_eff) (object effected) (SG [1563](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1577](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1577&fromdoc=Perseus%3Atext%3A1999.04.0007); [1619](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1619&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1627](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1627&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   [external object](#acc_aff) (object affected) (SG [1590](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1590&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1598](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1598&fromdoc=Perseus%3Atext%3A1999.04.0007); [1613](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1613&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1633](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1633&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   [accusative of extent](#acc_ext) (SG [1580](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1580&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1587](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   accusative of space (SG [1581](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   location

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   path

                                *   concrete
                *   figurative
                *   none of the above
                *   I do not know
            *   none of the above
            *   I do not know
        *   accusative of time (SG [1582](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1587](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   simultaneous location
            *   sequential location
            *   sequential-durative
            *   temporal distance
            *   temporal extent
            *   none of the above
            *   I do not know
        *   accusative of measure (SG [1581](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007))
        *   none of the above
        *   I do not know
    *   [terminal accusative](#acc_trm) (SG [1588](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1589](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   concrete
        *   figurative
        *   none of the above
        *   I do not know
    *   [accusative of respect](#acc_rsp) (SG [1600](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1605](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   adpositional accusative

                *   (with [ἀνά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1682&fromdoc=Perseus%3Atext%3A1999.04.0007),             [εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007),               [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) manner
        *   (with [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007)) instrument or means
        *   (with [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),             [παρά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&fromdoc=Perseus%3Atext%3A1999.04.0007), [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) cause
        *   (with [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007),             [εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007),               [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007),               [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007),              [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) purpose
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) standard of judgment
        *   (with [παρά](http://www.perseus.txufts.edu/hopper/text?doc=Smyth+grammar+1692&fromdoc=Perseus%3Atext%3A1999.04.0007), [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007), [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)) comparison
        *   advantage
        *   (with [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007),                 [εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007)) disadvantage
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007),                    [εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007)) recipient or addressee
        *   (with [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007),                    [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) conformity
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) friendly association
        *   (with [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)) hostile association
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   [independent](#acc_ipn) (SG [1599](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&fromdoc=Perseus%3Atext%3A1999.04.0007))

        *   elliptical accusative (SG [1599](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

#### <a id="acc_dpn">4.1.1.4.1 Dependent</a>

Dependent is the accusative which is syntactically dependent on another word in the sentence.

#### <a id="acc_eff">4.1.1.4.2 Internal object (object effected)</a>

This accusative is considered to be already contained in the meaning of the verb. An object effected is a noun or one of its equivalents from a similar or the same root as that of the governing verb (SG [1563](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1577](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1577&fromdoc=Perseus%3Atext%3A1999.04.0007)).

#### <a id="acc_aff">4.1.1.4.3 External object (object affected)</a>

The accusative of the affected object is not contained in the verb, and so it is considered to be external. The semantic macro-role is Patient. SG ([1551](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1562](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1562&fromdoc=Perseus%3Atext%3A1999.04.0007)) 
provides some examples of verbs taking an external accusative. The accusative of result (SG [1578](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1578&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1579](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1579&fromdoc=Perseus%3Atext%3A1999.04.0007)) is not annotated, but is subsumed under the external or internal object on the basis of the relationship of the accusative with the verb.

#### <a id="acc_ext">4.1.1.4.4 Accusative of extent</a>

The accusative of extent expresses extension over 
[space](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&fromdoc=Perseus%3Atext%3A1999.04.0007) 
and 
[time](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&fromdoc=Perseus%3Atext%3A1999.04.0007), or measure. The category measure should be used only when concerning space or amounts, not time. The accusative of extent can also be expressed by the accusative in conjunction with many 
[adpositions](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&fromdoc=Perseus%3Atext%3A1999.04.0007).

#### <a id="acc_trm">4.1.1.4.5 Terminal accusative</a>

The terminal accusative expresses place direction (SG [1588](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&fromdoc=Perseus%3Atext%3A1999.04.0007)). While in poetry the simple terminal accusative is common, in prose such an accusative is regularly specified by an adposition (SG [1589](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&fromdoc=Perseus%3Atext%3A1999.04.0007)).

#### <a id="acc_rsp">4.1.1.4.6 Accusative of respect</a>

The accusative of respect (SG [1600](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1605](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&fromdoc=Perseus%3Atext%3A1999.04.0007))
expresses in relation to what the meaning of a verb or adjective is circumscribed. It can also be expressed by an accusative with an adposition (SG [1603](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1603&fromdoc=Perseus%3Atext%3A1999.04.0007)) 
. 

#### <a id="acc_ipn">4.1.1.4.7 Independent</a>

Independent is the accusative which is the head of a sentence, i.e. the elliptical accusative (SG [1599](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&fromdoc=Perseus%3Atext%3A1999.04.0007)).

</a> <!-- end accusative -->

<a id="prp">

#### 4.1.1.5 Adpositions

In the following sections, the annotation of the adpositional case is detailed. I follow the SG list for the meanings/functions of each proper adposition (SG [1681](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1681&fromdoc=Perseus%3Atext%3A1999.04.0007)–[1698](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007); note that some use of a certain preposition might not be covered in SG and hence here). Each function is followed by indication of how to annotate it. Note that "genitive of place/time", "dative of place/time", and "accusative of space/time" are here used as abbreviations to mean that the annotator has to choose, on the basis of the verb governing the case, the right SR that is algorithmically available for each of them (e.g., genitive of place &gt; location). If it is not possible to annotate a semantic funtion (i.e., it is not included in the list), "none of the above" has to be selected. The annotator should try to stick to the lemma translation proposed (if present). Since most prepositions conveying a local meaning can also be used in a figurative sense, the annotation algorithm always requires specification of whether a certain use of a preposition is concrete or figurative (this option is therefore available under any local meaning of a case).

<a>

#### 4.1.1.5.1 [ἀμφί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1681&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   cause ("about", "concerning"): genitive of topic

with dative

*   local: dative of place
*   cause: dative of cause
*   means: dative of instrument or means

with accusative

*   local: accusative of space/terminal accusative
*   temporal: accusative of time
*   number: it depends on the function of the PP in the clause
*   of occupation with an object (i.e., figuratively): accusative of space
*   οἱ ἀμφί τινα (i.e., figuratively): accusative of space

</a>

<a>

#### 4.1.1.5.2 [ἀνά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1682&fromdoc=Perseus%3Atext%3A1999.04.0007)

with dative

*   local: dative of place

with accusative

*   local: terminal accusative/accusative of space
*   time: accusative of time
*   distributively: none of the above
*   manner: adpositional manner

</a>

<a>

#### 4.1.1.5.3 [ἀντί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1683&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   In other meanings ("instead of" or "in return for"): none of the above (for the lemma translation use, according to the meaning, "instead of" or "in return for")
*   in entreaty: adpositional advantage
</a>

<a>

#### 4.1.1.5.4 [ἀπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1684&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of separation
*   figuratively: genitive of separation
*   temporal: genitive of time
*   PPs such as ἀφ᾽ οὗ should be annotated as temporal adverbs
*   origin/source: genitive of source
*   author: adpositional agent
*   cause: genitive of cause
*   means/instrument: adpositional instrument or means
*   manner: adpositional  manner
*   conformity: adpositional conformity

</a>

<a>

#### 4.1.1.5.5 [διά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   figuratively: genitive of place
*   temporal: genitive of time
*   intervals of space or time: genitive of place or time
*   PPs such as διὰ πολλοῦ should be annotated as adverbs of measure
*   means: adpositional instrument or means
*   state or feeling: genitive of quality wherever possible, otherwise "none of the above"
*   manner: adpositional manner

with accusative

*   local: accusative of space
*   cause: adpositional cause
*   purpose: adpositional purpose
*   agency/mediation/means: adpositional instrument or means
</a>

<a>

#### 4.1.1.5.6 [εἰς](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&fromdoc=Perseus%3Atext%3A1999.04.0007), ἐς

with accusative

*   local: terminal accusative/accusative of space
*   "against": adpositional disadvantage
*   "in the presence of": adpositional recipient or addressee (with verbs of speaking)
*   temporal: accusative of time
*   measure and limit with numerals: it depends on the function of the PP in the clause
*   goal, purpose, intention: adpositional purpose
*   relation: accusative of respect
*   manner: adpositional  manner
*   PPs such as ἐς καιρόν should be annotated as adverbs of manner
</a>

<a>

#### 4.1.1.5.7 [ἐν](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1687&fromdoc=Perseus%3Atext%3A1999.04.0007)

with dative

*   local: dative of place
*   of circumstance, occupation (i.e., figuratively): dative of place
*   temporal: dative of time
*   PPs such as ἐν ᾧ should be annotated as temporal adverbs
*   instrument or means: dative of instrument or means
*   cause: dative of cause
*   manner: dative of manner
*   conformity: adpositional conformity

</a>

<a>

#### 4.1.1.5.8 [ἐξ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1688&fromdoc=Perseus%3Atext%3A1999.04.0007), ἐκ

with genitive

*   local: genitive of separation
*   temporal: genitive of time
*   immediate succession or transition: wherever possible, genitive of time
*   origin: genitive of source
*   agent: adpositional agent
*   consequence: genitive of cause
*   cause or ground of judgment: genitive of cause
*   material: genitive of material or contents
*   instrument and means: adpositional instrument or means
*   conformity: adpositional conformity
*   manner: adpositional manner
*   PPs such as ἐκ τοῦ ἴσου should be annotated as adverbs of manner
*   partitive: genitive of the divided whole

</a>

<a>

#### 4.1.1.5.9 [ἐπί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   temporal: genitive of time
*   other relations (figuratively): genitive of place

with dative

*   local: dative of place
*   temporal: dative of time
*   succession, addition: dative of time
*   supervision/dependence (i.e., figuratively): dative of place
*   condition: adpositional condition
*   reason, motive: dative of cause
*   hostility: dative of disadvantage
*   price: adpositional price and value 

with accusative

*   local: terminal accusative/accusative of space
*   temporal: accusative of time
*   quantity, measure: accusative of measure
*   PPs such as ἐπὶ μικρόν should be annotated as adverbs of manner
*   purpose: adpositional purpose
*   hostility: adpositional disadvantage
*   reference: accusative of respect
</a>

<a>

#### 4.1.1.5.10 [κατά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of separation/genitive of place
*   PPs such as κατ᾽ ἄκρας should be annotated as adverbs of manner
*   temporal: genitive of time
*   "against": adpositional disadvantage
*   "with regard to": genitive of connection
*   with verbs of swearing: none of the above

with accusative

*   local: terminal accusative/accusative of space
*   temporal: accusative of time
*   purpose: adpositional purpose
*   conformity: adpositional conformity
*   ground on which an act is based: adpositional cause
*   comparison: adpositional comparison
*   manner: adpositional manner
*   distribution: none of the above
*   approximate number: it depends on the function of the PP in the clause

</a>

<a>

#### 4.1.1.5.11 [μετά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place/adpositional accompaniment
*   accompanying circumstance: adpositional accompanying circurmstance
*   joint efficient cause: genitive of cause
*   conformity: adpositional conformity

with dative

*   local: dative of place  

with accusative

*   local: terminal accusative/accusative of space
*   temporal, "after": accusative of time
*   figuratively: accusative of space   

</a>

<a>

#### 4.1.1.5.12 [παρά](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of separation
*   author, source: genitive of source
*   with passives and intransitives: adpositional agent

with dative

*   local: dative of place
*   possessor: dative of the possessor
*   "of the superior in command" (i.e., figuratively): dative of place
*   of the person judging: dative of reference  

with accusative

*   local: terminal accusative/accusative of space
*   "contrary to": none of the above (lemma translation should be "contrary to")
*   "in addition to": none of the above (lemma translation should be "in addition to")
*   PPs such as παρ᾽ ὀλίγον ("of no account") should be annotated as adverbs of measure
*   temporal: accusative of time
*   cause/dependence: adpositional cause
*   Adverbial PPs such as παρὰ πολύ or παρὰ μικρόν: πολύ and μικρόν are morphologically annotated as adverbs (adverb &gt; measure in SG tab)
*   comparison: adpositional comparison 

</a>

<a>

#### 4.1.1.5.13 [περί](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1693&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   "about", "concerning": genitive of connection/genitive of topic
*   superiority: genitive of distinction and comparison
*   PPs such as περὶ παντός ("above all") should be annotated as adverbs of measure

with dative

*   local: dative of place
*   external cause: dative of cause
*   inner impulse: dative of cause  

with accusative

*   local: terminal accusative/accusative of space
*   of person (i.e., figuratively): accusative of space
*   indefinite statement of time and number: it depends on the function of the PP in the clause
*   occupation (i.e., figuratively): accusative of space
*   relation: accusative of respect 

</a>

<a>

#### 4.1.1.5.14 [πρό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1694&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   temporal: genitive of time
*   defence or care: adpositional advantage
*   preference: none of the above (for the lemma translation use, according to the meaning, "in preference to" or "on behalf of")
*   PPs such as πρὸ πολλοῦ ("highly") should be annotated as adverbs of measure

</a>

<a>

#### 4.1.1.5.15 [πρός](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   local: genitive of place
*   descent: genitive of source
*   characteristic: genitive of quality
*   point of view of a person: adpositional reference
*   agent: adpositional agent
*   "to the advantage of": adpositional advantage
*   in oaths and entreaties: none of the above

with dative

*   local: dative of place
*   occupation: none of the above
*   "in addition to": none of the above (the lemma translation should be "in addition to")
*   "in the presence of": dative as indirect complement of verbs    

with accusative

*   local: terminal accusative
*   temporal: accusative of time
*   friendly or hostile relation: adpositional recipient or addressee (with verbs of speaking) or adpositional association
*   relation in general: accusative of respect
*   purpose: adpositional purpose
*   conformity: adpositional conformity
*   standard of judgment: adpositional standard of judgment
*   comparison: adpositional comparison
*   exchange: none of the above 

</a>

<a>

#### 4.1.1.5.16 [σύν](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1696&fromdoc=Perseus%3Atext%3A1999.04.0007)

with dative

*   "with", "along with", "together with", "including": genitive of association/accompaniment/accompanying circumstance
*   means and instrument: dative of means or instrument
*   manner: dative of manner
*   "in conformity with": adpositional conformity

</a>

<a>

#### 4.1.1.5.17 [ὑπέρ](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1697&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   "from over", "over", "above": genitive of separation/genitive of place
*   "in defence of", "on behalf of": adpositional advantage
*   "in place of", "in the name of": none of the above
*   purpose: genitive of purpose
*   "concerning", "about": genitive of topic / genitive of connection

with accusative

*   local: accusative of space
*   temporal: accusative of time
*   measure: accusative of measure

</a>

<a>

#### 4.1.1.5.18 [ὑπό](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&fromdoc=Perseus%3Atext%3A1999.04.0007)

with genitive

*   "out from under": genitive of separation/genitive of place
*   direct agent/with passive nouns: adpositional agent
*   external/internal cause: genitive of cause
*   external accompaniment: adpositional accompanying circumstance/accompaniment
*   manner: adpositional manner

with dative

*   "under": dative of place
*   agent: dative of agent
*   cooperative cause: dative of cause
*   subjection: none of the above   

with accusative

*   local: terminal accusative/accusative of space
*   temporal: accusative of time
*   subjection: none of the above   

</a>

</a> <!-- end adposition -->

</a>

<a id="adj_prp">

#### 4.1.2 Adjective proper

If an adjective is also syntactically used as such, no further SG annotation is (currently) available.

The Prague annotation labels are usually ATR, PNOM, and OCOM.

</a>

<a id="sbs_adj">

#### 4.1.3 Substantive adjective

A substantive adjective is an adjective lemma in the [LSJ dictionary](http://www.perseus.tufts.edu/hopper/resolveform?redirect=true) which is used as a noun (e.g., Ἀθαναῖος in Ἀθαναῖοι, 'the Athenians'). The SG algorithm allows annotation of its [syntax of the case](#snt_cas) (whose categories are the same as those for the noun).

The Prague annotation label for the substantive adjective are the same as those for the [noun](#nou).

</a>

<a id="vrb_adj">

#### 4.1.4 Verbal adjective in τος/τεος

A verbal adjective in τος/τεος derives from a verb root by the addition of the suffix τος/τεος (see SG [2149](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2149&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2152](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2152&fromdoc=Perseus%3Atext%3A1999.04.0007) for more information). The present option is reserved when the verbal adjective has adjective function only (i.e., is not a substantive). No further SG annotation is available.

The verbal adjective in τος/τεος takes the same Prague annotation labels as the [adjective](#adj) in adjective function.

</a>

<a id="vrb_adj_sbs">

#### 4.1.5 Substantive verbal adjective in τος/τεος

A substantive verbal adjective in τος/τεος is a verbal adjective used as a noun. The SG tagset allows annotation of its [syntax of the case](#snt_cas).

The Prague annotation labels are the same as those for the [noun](#nou).

</a>

<a id="sbs_prn">

#### 4.1.6 Substantive pronoun

A substantive pronoun is a pronoun used as a noun. This option gives access to the annotation of the [syntax of the case](#snt_cas) of the pronoun.

The Prague annotation labels are the same as those for the [noun](#nou).

</a>

<a id="adj_prn">

#### 4.1.7 Adjective pronoun

An adjective pronoun is a pronoun used as an adjective. As occurs with any other [adjective](#adj) in adjective function, no further SG annotation is (currently) avaialble.

The Prague annotation labels are the same as those for the [adjective](#adj) in adjective function.

</a>

<a id="fnt_moo">

#### 4.1.8 Syntax of the finite verb

On the basis of the mood selected at the morphological level, the annotation algorithm gives access to the the following options:

*   [independent](#ind_fnt_vrb) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=1&doc=4971))

    *   statement (SG [2153](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2153&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   assumption (SG [2154](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2154&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   command (SG [2155](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2155&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   wish (SG [2156](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2156&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   question (SG [2157](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2157&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   exclamation (SG [2158](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2158&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   none of the above
    *   I do not know

*   [dependent](#dpn_fnt_vrb)

        *   [substantive clause](#sbs_cls)                                                      ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&doc=4971))                                                        ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=12&doc=4971))

                *   statement (SG [2576](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2576&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2588](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2588&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect discourse
            *   none of the above
            *   I do not know
        *   will or desire (SG [2207](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2207&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2239](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2239&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect discourse
            *   none of the above
            *   I do not know
        *   question (SG [2663](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2663&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2680](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2680&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect discourse
            *   none of the above
            *   I do not know
        *   exclamation (SG [2681](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2681&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2687](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect discourse
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know
    *   [adjective clause](#adj_cls) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&doc=4971))

                *   adjective clause proper

                        *   ordinary relative clause (SG [2553](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2553&fromdoc=Perseus%3Atext%3A1999.04.0007))

                                *   in indirect discourse
                *   not in indirect discourse
                *   none of the above
                *   I do not know
            *   final relative clause (SG [2554](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2554&fromdoc=Perseus%3Atext%3A1999.04.0007))

                                *   in indirect discourse
                *   not in indirect discourse
                *   none of the above
                *   I do not know
            *   cause relative clause (SG [2555](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2555&fromdoc=Perseus%3Atext%3A1999.04.0007))

                                *   in indirect discourse
                *   not in indirect discourse
                *   none of the above
                *   I do not know
            *   consecutive relative clause (SG [2556](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2556&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2559](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2559&fromdoc=Perseus%3Atext%3A1999.04.0007))

                                *   in indirect discourse
                *   not in indirect discourse
                *   none of the above
                *   I do not know
            *   conditional relative clause (SG [2560](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2560&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2573](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2573&fromdoc=Perseus%3Atext%3A1999.04.0007))

                                *   in indirect discourse
                *   not in indirect discourse
                *   none of the above
                *   I do not know
            *   none of the above
            *   I do not know
        *   substantivized adjective clause

                        *   in indirect discourse

                                *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
            *   not in indirect discourse

                                *   [<span style="font-style:italic">syntax of the case</span>](#snt_cas)
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know
    *   adverb clause ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&doc=4971))

                *   final clause (SG [2193](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2193&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2206](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2206&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   causal clause (SG [2240](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2240&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2248](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2248&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   consecutive clause (SG [2249](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2249&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2278](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2278&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   conditional clause (SG [2280](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2280&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2368](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2368&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   concessive clause (SG [2369](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2369&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2382](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2382&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   temporal clause (SG [2383](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2383&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2461](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   simultaneous location

                                *   in indirect discourse
                *   not in indirect speech
                *   none of the above
                *   I do not know
            *   sequential location

                                *   in indirect discourse
                *   not in indirect speech
                *   none of the above
                *   I do not know
            *   sequential-durative

                                *   in indirect discourse
                *   not in indirect speech
                *   none of the above
                *   I do not know
            *   temporal distance

                                *   in indirect discourse
                *   not in indirect speech
                *   none of the above
                *   I do not know
            *   temporal extent

                                *   in indirect discourse
                *   not in indirect speech
                *   none of the above
                *   I do not know
            *   none of the above
            *   I do not know
        *   clause of comparison (SG [2462](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2462&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2487](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&fromdoc=Perseus%3Atext%3A1999.04.0007))

                        *   in indirect discourse
            *   not in indirect speech
            *   none of the above
            *   I do not know
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

<a id="ind_fnt_vrb">

#### 4.1.8.1 Independent

A finite verb form is said to be independent if it is the head of a main clause (simple or coordinated). On the basis of its meaning, the clause can be annotated as a statement (SG [2153](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2153&fromdoc=Perseus%3Atext%3A1999.04.0007)), an assumption 
    (SG [2154](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2154&fromdoc=Perseus%3Atext%3A1999.04.0007)), a command (SG 
    [2155](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2155&fromdoc=Perseus%3Atext%3A1999.04.0007)), a wish (SG 
    [2156](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2156&fromdoc=Perseus%3Atext%3A1999.04.0007)), a question (SG 
    [2157](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2157&fromdoc=Perseus%3Atext%3A1999.04.0007)), or an exclamation (SG
    [2158](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2158&fromdoc=Perseus%3Atext%3A1999.04.0007)).

The finite verb takes the Prague annotation label PRED, OBJ, ADV, or ATR.

</a>

<a id="dpn_fnt_vrb">

#### 4.1.8.2 Dependent

A finite verb form is said to be dependent if it is the head of a subordinate clause.

</a>

<a id="sbs_cls">

#### 4.1.8.3 Substantive clause

A substantive clause is equivalent to a noun with respect to its governing verb (and indeed it could often be replaced with a pronoun such as τόδε). On the basis of its meaning, the clause can be annotated as a statement (SG [2576](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2576&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2588](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2588&fromdoc=Perseus%3Atext%3A1999.04.0007)), will or desire (SG [2207](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2207&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2239](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2239&fromdoc=Perseus%3Atext%3A1999.04.0007)), a question (SG [2663](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2663&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2680](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2680&fromdoc=Perseus%3Atext%3A1999.04.0007)), or an exclamation (SG [2681](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2681&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2687](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&fromdoc=Perseus%3Atext%3A1999.04.0007)).

The head verb of the substantive clause takes the Prague annotation labels SBJ, OBJ, or APOS.

</a>

<a id="adj_cls">

#### 4.1.8.4 Adjective clause

The Adjective clause is a relative clause. Just like an adjective, the relative clause can have the function of an adjective (adjective clause proper) or be substantivized (i.e., when the antecedent is not expressed). There two ways to annotate substantivized relative clauses. The easiest way is to not add an elliptical node for the omitted antecedent. The second option is to add the elliptical node and so treat the relative clause as an adjective clause proper (and so any relative clause is treated as an adjective clause proper, independentely of whether or not the antecedent of the relative pronoun is expressed). The first option is the default one, while the second one has to be declared. The adjective clause proper can be an ordinary relative clause (SG [2553](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2553&fromdoc=Perseus%3Atext%3A1999.04.0007)), a final relative clause (SG [2554](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2554&fromdoc=Perseus%3Atext%3A1999.04.0007)), a cause relative clause (SG [2555](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2555&fromdoc=Perseus%3Atext%3A1999.04.0007)), a consecutive relative clause (SG [2556](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2556&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2559](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2559&fromdoc=Perseus%3Atext%3A1999.04.0007)), or a conditional relative clause (SG [2560](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2560&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2573](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2573&fromdoc=Perseus%3Atext%3A1999.04.0007)), on the basis of its meaning.

The easiest example of relative clause is the one with the antecedent expressed ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=46&doc=4971)). When the antecedent is not expressed, and so the adjective clause it taken to be substantivized, the verb of the relative clause is attached to the governor verb and receives the SG annotation that an antecedent would have received if it were expressed; the relative pronoun is attached to the verb of the relative clause and receives the SG annotation that is required by the governor verb, no matter what the morphology of the relative pronoun is (i.e., the syntactic case can be different from the morphological one of the relative pronoun/adverb): see  [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=20&doc=4971), [tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=49&doc=4971). The possibility to choose a different syntactic case for each word allows also the annotation of examples of incorporation of the ancedent ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=51&doc=4971)). When an adjective clause proper has adverbial function, it has to be appended to its superordinate verb: [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=47&doc=4971).

The Prague annotation labels for the head verb of an adjective clause are the same as those for the [adjective](#adj) or [noun](#noun) (for the substantivized adjective clause).

</a>

<a id="adv_cls">

#### 4.1.8.5 Adverb clause

An adverb clause is a clause functioning as an adverb with respect to its governing verb. On the basis of its meaning it is possible to specify if the adverb clause is a final clause (SG [2193](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2193&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2206](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2206&fromdoc=Perseus%3Atext%3A1999.04.0007)), a causal clause (SG [2240](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2240&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2248](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2248&fromdoc=Perseus%3Atext%3A1999.04.0007)), a consecutive clause (SG [2249](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2249&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2278](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2278&fromdoc=Perseus%3Atext%3A1999.04.0007)), a conditional clause (SG [2280](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2280&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2368](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2368&fromdoc=Perseus%3Atext%3A1999.04.0007)), a concessive clause (SG [2369](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2369&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2382](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2382&fromdoc=Perseus%3Atext%3A1999.04.0007)), a temporal clause (SG [2383](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2383&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2461](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&fromdoc=Perseus%3Atext%3A1999.04.0007)), or a clause of comparison (SG [2462](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2462&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2487](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&fromdoc=Perseus%3Atext%3A1999.04.0007)).

The verb head of an adverb clause takes the Prague annotation label ADV.

</a>

</a>

<a id="adj_prt">

#### 4.1.9 Adjective participle

The participle is a verbal adjective (SG [2039](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2039&fromdoc=Perseus%3Atext%3A1999.04.0007)). Like any other [adjective](#adj), it can have adjective function or be [substantivized](#sbs_prt). In the former case, the SG tagset allows annotation of the following categories:

*   [attributive participle](#att_prt) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=42&doc=4971)) ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=44&doc=4971))
*   [circumstantial participle](#crc_prt)   ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=43&doc=4971))
                                                            ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&doc=4971))

        *   time (SG [2061](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2061&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   simultaneous location
        *   sequential location
        *   sequential-durative
        *   temporal distance
        *   temporal extent
        *   none of the above
        *   I do not know
    *   manner (SG [2062](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2062&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   means (SG [2063](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2063&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   cause (SG [2064](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2064&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   purpose (SG [2065](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2065&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   concession (SG [2066](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2066&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   condition (SG [2067](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2067&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   any attendant circumstance (SG [2068](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2068&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   none of the above
    *   I do not know
*   [supplementary participle](#spp_prt) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=21&doc=4971))
                                                        ([tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&doc=4971))
                                                        ([tree3](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&doc=4971))

        *   in indirect discourse
    *   not in indirect discourse
    *   none of the above
    *   I do not know
*   [periphrastic participle](#prh_prt) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=45&doc=4971))
*   none of the above
*   I do not know

<a id="att_prt">

#### 4.1.9.1 Attributive participle

The attributive participle is the participle having a function similar to that of an attributive adjective (SG [2049](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2049&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2053](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2053&fromdoc=Perseus%3Atext%3A1999.04.0007)), and so is annotated as depending on the noun (or one of its equivalents) which it agrees with. It usually has attributive position (SG [1166](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1166&fromdoc=Perseus%3Atext%3A1999.04.0007)), but can also be in predicate position (SG [2053](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2053&fromdoc=Perseus%3Atext%3A1999.04.0007)):

&gt; ἐπὶ Κόδρου βασιλεύοντος
&gt; 
&gt; 'in the reign of Codrus', Lyc. 84
&gt; 
&gt; Κόδρου (genitive &gt; dependent &gt; genitive of time and place &gt; time &gt; sequential durative)
&gt; 
&gt; βασιλεύοντος (participle &gt; attributive)

The temporal function is annotated as part of the genitive noun, while the participle is annotated as attributive. Another example of attributive participle not being in attributive position is:

&gt; ἐπὶ τὸν Χάλον ποταμόν, ὄντα τὸ εὖρος πλέθρου
&gt; 
&gt; 'to the river Chalus, which is a plethrum in width', X. A. 1.4.9
&gt; 
&gt; ὄντα (participle &gt; attributive &gt; proper)

There are participles that can be taken to be attributive with the force of an improper relative clause  (i.e., a relative clause having the force of a an adverb clause, such as a final clause):

&gt; προπέμψαντες κήρυκα πόλεμον προεροῦντα
&gt; 
&gt; 'having sent a herald in advance to proclaim war', T. 1.29

The participle προεροῦντα can be interpreted as translating a final relative clause. Participles such as these are traditionally considered to be circumstantial and so syntactically dependent on their superordinate verbs, as occurs with circumstantial participles when they are in the nominative case.

All the participles so far discussed take the Prague annotation label ATR when they are attached to a noun or the function ADV if they are equivalent to an adverb clause and are attached to their superordinate verb.

</a>

<a id="crc_prt">

#### 4.1.9.2 Circumstantial participle

The circumstantial participle, according to SG
([2054](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2054&fromdoc=Perseus%3Atext%3A1999.04.0007)),  specifies the circumstance under which the action of the superordinate verb takes place. The annotation algorithm allows us to specify the force of the circumstantial participle:

*   time (SG [2061](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2061&fromdoc=Perseus%3Atext%3A1999.04.0007))

        *   simultaneous location
    *   sequential location
    *   sequential-durative
    *   temporal distance
    *   temporal extent
    *   none of the above
    *   I do not know
*   manner (SG [2062](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2062&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   means (SG [2063](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2063&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   cause (SG [2064](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2064&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   purpose (SG [2065](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2065&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   concession (SG [2066](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2066&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   condition (SG [2067](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2067&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   any attendant circumstance (SG [2068](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2068&fromdoc=Perseus%3Atext%3A1999.04.0007))

It is to be noted that the force of a participle heavily depends on the context, and so ambiguities may sometimes arise (SG ([2069](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2069&fromdoc=Perseus%3Atext%3A1999.04.0007)) well acknowledges this as well): the annotator should choose the most likely label according to his/her interpretation of the participle. Notwithstanding, the meaning of the circumstantial participle is very often signalled clearly by adverbs in the superordinate clause, such as 
ἔπειτα 'thereupon', τότε 'then', ἤδη 'already', etc. (a list can be found in SG 
([2079](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2079&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2087](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2087&fromdoc=Perseus%3Atext%3A1999.04.0007)); note that ἅτε, οἷα, οἷον, ὡς, and ὥσπερ depend on the participles - and not on the superordinate verb of the participle - as AuxZ). 
The label "any attendand circumstance" should be reserved for those participles whose meaning can be rendered in English with a preposition (“ἔχων στρατιὰν ἀφικνεῖται” he arrives with an army” [T. 4.30](http://www.perseus.tufts.edu/hopper/text?doc=Thuc.%204.30&lang=original)) or with a coordinate clause (rather than a subordinate clause).

These kinds of circumstantial participles are labeled as ADV in the Prague annotation.

The genitive absolute and the accusative absolute (SG [2070](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2070&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2078](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2078&fromdoc=Perseus%3Atext%3A1999.04.0007)) are considered to be a kind of circumstantial participle, so there is no difference in their annotation, except that the genitive or the accusative nouns functioning as their subjects are attached to the participle (and receive the Prague annotation label "SBJ") and not to the superordinate verb of the participle.

</a>

<a id="spp_prt">

#### 4.1.9.3 Supplementary participle

The supplementary participle is an argument of the verb. Following SG, two kinds of supplementary participles are distinguished: the one not in indirect discourse (SG 
[2094](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2105](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&fromdoc=Perseus%3Atext%3A1999.04.0007); [2123](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007)) and the one in indirect discourse (SG
[2106](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2115](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&fromdoc=Perseus%3Atext%3A1999.04.0007); [2120](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2120&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007)). The difference lies in the nature of the governing verb, which can allow a participle to be equivalent to a dependent statement according to the principles of indirect discourse (SG [2589](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2589&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2635](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2635&fromdoc=Perseus%3Atext%3A1999.04.0007)):

&gt; οὐ γὰρ ᾔδεσαν αὐτὸν τεθνηκότα (= τέθνηκε)
&gt; 
&gt; 'for they did not know that he was dead', X. A. 1.10.16
&gt; 
&gt; τεθνηκότα (participle &gt; supplementary &gt; indirect discourse)

In the example the participle depends on ᾔδεσαν, and αὐτὸν depends on the participle, being interpreted as its subject. Such participles receive the function OBJ, as in the example, or PNOM, if a personal construction is present (as with δῆλός εἰμι, SG ([2107](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2107&fromdoc=Perseus%3Atext%3A1999.04.0007)); when building the tree, the participle is attached to the adjective). When the supplementary participle is not in indirect discourse, there is no dependent statement according to the principles of indirect discourse:

&gt; διάγουσι μανθάνοντες
&gt; 
&gt; 'they are continually (they spend their time in) learning', X. C. 1.2.6
&gt; 
&gt; τεθνηκότα (participle &gt; supplementary &gt; not in indirect discourse)

 Such participles are attached to the governing verb and their label is PNOM. There may be cases where a supplementary participle agrees with a dative, as in:

&gt; εἰ (αὐτοῖς) πολεμοῦσιν ἄμεινον ἔσται
&gt; 
&gt; '(they asked the god) whether it would be better for them to make war', T. 1.118.

The participle πολεμοῦσιν depends on ἔσται and receives the label SBJ: the accordance with the implied dative of advantage can be explained as a case of attraction (SG 
    [1060](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&fromdoc=Perseus%3Atext%3A1999.04.0007)). A list of verbs allowing a supplementary participle not in indirect discourse can be found in (SG [2094](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2105](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&fromdoc=Perseus%3Atext%3A1999.04.0007)). Verbs of perceiving and finding (SG [2110](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2110&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2115](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&fromdoc=Perseus%3Atext%3A1999.04.0007)) allow participles both in indirect discourse and not in indirect discourse: when the participle is not in indirect discourse, it takes the function OCOMP ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&doc=4971)).
    Some verbs (SG 
 [2123](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2145](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&fromdoc=Perseus%3Atext%3A1999.04.0007)) allow either the participle or the infinitive in indirect discourse or not in indirect discourse.

</a>

<a id="prh_prt">

####  4.1.9.4 Periphrastic participle

In SG, this participle is considered to be a kind of supplementary participle (SG [2091](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2091&fromdoc=Perseus%3Atext%3A1999.04.0007); note that if a participle is substantivized it cannot be taken to be periphrastic). However it seems to be useful to categorize it separately. See SG ([599](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+599&fromdoc=Perseus%3Atext%3A1999.04.0007), 
        [600](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+600&fromdoc=Perseus%3Atext%3A1999.04.0007), 
            [1961](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1961&fromdoc=Perseus%3Atext%3A1999.04.0007)-[1965](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1965&fromdoc=Perseus%3Atext%3A1999.04.0007)) for plenty of examples.

The syntactic label for the periphrastic participle is PNOM.

</a>
</a>

<a id="sbs_prt">

#### 4.1.10 Substantive participle

A substantive participle is a participle which is used as a noun. The SG algorithm allows annotation of its [syntax of the case](#snt_cas) (whose categories are the same as those for the noun).

The Prague annotation labels for the substantive participle are the same as those for the [noun](#nou).

</a>

<a id="inf">

#### 4.1.11 Syntax of the infinitive

The infinitive is a [verbal noun](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1966&fromdoc=Perseus%3Atext%3A1999.04.0007). Its syntactic behavior is due to its partly nominal and partly verbal nature. Although such an "in-between" nature is always present in the infinitive, the articular function and the (for a lack of a better term) verbal function of the infinitive are here distinguished for the purposes of the classification. The algorithm for the infinitive is the following:

*   [dependent](#dpn_inf)

    *   [articular](#art_inf)

            *   nominative
        *   genitive
        *   dative
        *   accusative
        *   none of the above
        *   I do not know

        *   [verbal](#vrl_inf)

            *   as nominative ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=39&doc=4971))

                    *   in indirect discourse

                            *   statement
                *   assumption
                *   command
                *   wish
                *   question
                *   exclamation
                *   none of the above
                *   I do not know
            *   not in indirect discourse

                            *   statement
                *   assumption*   command*   wish
                *   question
                *   exclamation
                *   none of the above
                *   I do not know

                        *   none of the above
            *   I do not know

                *   as accusative ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&doc=4971))

                    *   in indirect discourse
            *   not in indirect discourse
            *   none of the above
            *   I do not know

                *   uncertain case

                    *   [infinitive of purpose (uncertain case)](#vrl_inf) ([tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=41&doc=4971))*   [infinitive of result (uncertain case)](#vrl_inf)
            *   [temporal infinitive (uncertain case)](#vrl_inf)

                                *   simultaneous location
                *   sequential location
                *   sequential-durative
                *   temporal distance
                *   temporal extent
                *   none of the above
                *   I do not know

                        *   none of the above
            *   I do not know

                *   none of the above
        *   I do not know

        *   none of the above
    *   I do not know

*   [independent](#idp_inf)

    *   command (SG [2013](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2013&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   wish (SG [2014](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2014&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   exclamation (SG [2015](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2015&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   absolute infinitive (SG [2012](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2012&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   none of the above
    *   I do not know

*   none of the above
*   I do not know

<a id="dpn_inf">

#### 4.1.11.1 Dependent

An infinitive is said to be "dependent" if it is (linguistically) governed by another word in the sentence.

</a>

<a id="idp_inf">

#### 4.1.11.2 Independent

An infinitive is said to be "independent" if it is the head of a sentence (or linguistically independent, as the absolute infinitive is).

</a>

<a id="art_inf">

#### 4.1.11.3 Articular infinitive

The articular infinitive is the infinitive preceded by the definite article:

*   nominative (articular) (SG [2031](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2031&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   genitive (articular) (SG [2032](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2032&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   dative (articular) (SG [2033](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2033&fromdoc=Perseus%3Atext%3A1999.04.0007))
*   accusative (articular) (SG [2034](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2034&fromdoc=Perseus%3Atext%3A1999.04.0007))

The whole spectrum of possibilities available to annotate the noun is algorithmically made available for the articular infinitive, even though only some them 
    are likely to be found in practice. On the basis of the case selected, the annotator has access to the [syntax of the case](#snt_cas).

The Prague annotation labels are the same as those for the [noun](#nou).

</a>

<a id="vrl_inf">

#### 4.1.11.4 Verbal infinitive

When the infinitive is not articular, it is labeled as "verbal". The following possibilities are available:

*   as nominative

        *   in indirect discourse

                *   statement
        *   assumption*   command*   wish
        *   question
        *   exclamation
        *   none of the above
        *   I do not know
    *   not in indirect discourse
    *   none of the above
    *   I do not know
*   as accusative

        *   in indirect discourse

                *   statement
        *   assumption*   command*   wish
        *   question
        *   exclamation
        *   none of the above
        *   I do not know
    *   not in indirect discourse
    *   none of the above
    *   I do not know
*   uncertain case

        *   infinitive of purpose (uncertain case) (SG [2008](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2010](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2010&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   infinitive of result (uncertain case) (SG [2011](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&fromdoc=Perseus%3Atext%3A1999.04.0007))
    *   temporal infinitive (uncertain case) (SG [2453](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2453&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2461](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&fromdoc=Perseus%3Atext%3A1999.04.0007))

                *   simultaneous location
        *   sequential location
        *   sequential-durative
        *   temporal distance
        *   temporal extent
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   none of the above
*   I do not know

The infinitive, when depending on a verb, bears a syntactic nominative or accusative case on the basis of whether it is the subject or the object of a verb, and can be in indirect discourse (SG
    [2016](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2016&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2024](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2024&fromdoc=Perseus%3Atext%3A1999.04.0007)) or not in indirect discourse (SG 
    [1989](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1989&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2007](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2007&fromdoc=Perseus%3Atext%3A1999.04.0007)). The infinitive can also be used to express purpose (SG [2008](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2010](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2010&fromdoc=Perseus%3Atext%3A1999.04.0007)), result (SG [2011](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&fromdoc=Perseus%3Atext%3A1999.04.0007)), or temporal clauses (SG [2453](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2453&fromdoc=Perseus%3Atext%3A1999.04.0007)–[2461](http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&fromdoc=Perseus%3Atext%3A1999.04.0007)).

The Prague annotation labels are the same as those for the [noun](#nou). When the infinitive is of purpose, result, or temporal, the label is [ADV](#adv_fnc).

</a>

<a id="adv_snt">

#### 4.1.12 Syntax of the adverb

The SG tagset allows the annotation of the following SRs for the adverb:

*   time

        *   simultaneous location
    *   sequential location
    *   sequential-durative
    *   temporal distance
    *   temporal extent
    *   none of the above
    *   I do not know
*   place

        *   location

                *   concrete
        *   figurative
        *   none of the above
        *   I do not know
    *   direction

                *   concrete
        *   figurative
        *   none of the above
        *   I do not know
    *   path

                *   concrete
        *   figurative
        *   none of the above
        *   I do not know
    *   separation

                *   concrete
        *   figurative
        *   none of the above
        *   I do not know
    *   none of the above
    *   I do not know
*   source
*   cause
*   result
*   manner
*   measure (/degree)
*   instrument or means
*   purpose
*   concessive
*   negation
*   [particle](#part)
*   none of the above
*   I do not know

The tagset distinguishes many kinds of time and place adverbs because the annotation aims to preserve the distinctions that are morphologically signaled by the case when the SR is expressed by a noun.

The Prague annotation labels are [OBJ](#obj), [ADV](#adv_fnc) (on the basis of whether or not the adverb is an argument), [AuxZ](#auxz), or [AuxY](#auxy).

<a id="part">

#### 4.1.12.1 Particle

Particle are here defined as those adverbs, typically sentence adverbs, which in AG are usually in pospositive position. The definition in SG, as well as in many traditional grammars, is broader, in that it also includes conjunctions: these, however, have to be always annotated as conjunctions. As is known, the meaning and function of AG particles is very complex to capture. In the following guidelines there is no attempt to provide detailed criteria to annotate particles. The annotator is only required to be able to identify those particle (in the traditional large definition of terms) which are conjunctions, such as:

*   ἀλλά
*   ἀτάρ
*   δέ [tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=51&doc=4971)
*   εἴτε
*   ἤ
*   ἠδέ
*   καί
*   καίτοι
*   οὐδέ
*   οὔτε
*   μηδέ
*   μήτε
*   τε

Some of these particples can of course be adverbs, and so should accordingly be annotated as such. When a particle is a conjunction, it governs other nodes: 

[tree1](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&doc=4971),
[tree2](http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&doc=4971).

Any other particle which is not one of the above conjunctions is attached to the verb of the main clause and receives the AuxY label, if the particle is a sentence adverb, or is attached to the word which it modifies and receives the label AuxZ. In the current version of the treebank it is left to the annotator to decide which of these two options is the right one for each of the non-conjuntion particles.

</a>

</a>

</a>

</a>
</a>
</a>

