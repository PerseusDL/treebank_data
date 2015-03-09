<body>

<a id="guidelines">
<h3 style="text-align: center">GUIDELINES FOR THE ANCIENT GREEK DEPENDENCY TREEBANK 2.0 (beta version)</h3>
<h4 style="text-align: center">Giuseppe G. A. Celano</h4>
<h4 style="text-align: center">Tufts University &amp; Universität Leipzig</h4>

<a id="sum">
	<h3>Summary</h3>
	<ul style="list-style-type:none">
		<li>1. <a href="#int">Introduction</a>
          </li> 
		<li>2. <a href="#mph_tgs">Morphological layer</a>
		<ul style="list-style-type:none">
		<li>2.1<a href="#art"> article</a>
              </li>
		<li>2.2<a href="#nou"> noun(/substantive)</a>
              </li>
		<li>2.3<a href="#adj"> adjective</a>
              </li>
		<li>2.4<a href="#prn"> pronoun</a> 
              </li>
		<li>2.5<a href="#vrb"> verb</a>
              </li>
		<li>2.6<a href="#adv"> adverb</a>
              </li>
		<li>2.7<a href="#adp"> adposition</a>
              </li>
		<li>2.8<a href="#cnj"> conjunction</a>
              </li>
		<li>2.9<a href="#nmr"> numeral</a>
              </li>
		<li>2.10<a href="#exc"> interjection</a>
              </li>
		<li>2.11<a href="#pct"> punctuation</a>
              </li>
		</ul>
		</li>
		<li>3.<a href="#prg_ann"> Syntactic layer</a>
		<ul style="list-style-type:none">
		<li>3.1<a href="#pred"> PRED</a>
              </li>
		<li>3.2<a href="#sbj"> SBJ</a>
              </li>
		<li>3.3<a href="#obj"> OBJ</a>
              </li>
		<li>3.4<a href="#atr"> ATR</a>
              </li>
		<li>3.5<a href="#adv_fnc"> ADV</a>
              </li>
		<li>3.6<a href="#atv"> ATV/atvV</a>
              </li>
		<li>3.7<a href="#pnom"> PNOM</a>
              </li>
		<li>3.8<a href="#ocomp"> OCOMP</a>
              </li>
		<li>3.9<a href="#coord"> COORD</a>
              </li>
		<li>3.10<a href="#apos"> APOS</a>
              </li>
		<li>3.11<a href="#apos"> MWE</a>
              </li>
		<li>3.12<a href="#auxp"> AuxP</a>
              </li>
		<li>3.13<a href="#auxc"> AuxC</a>
              </li>
		<li>3.14<a href="#auxx"> AuxX</a>
              </li>
		<li>3.15<a href="#auxg"> AuxG</a>
              </li>
		<li>3.16<a href="#auxk"> AuxK</a>
              </li>
		<li>3.17<a href="#auxy"> AuxY</a>
              </li>
		<li>3.18<a href="#auxz"> AuxZ</a>
              </li>
		<li>3.19<a href="#exd"> ExD</a>
              </li>
		<li>3.20<a href="#suffixes"> Suffixes</a>
		<ul>
			<li>3.20.1 <a href="#_CO">_CO</a>
                  </li>
			<li>3.20.2 <a href="#_AP">_AP</a>
                  </li>
		</ul>
		</li>
		</ul>
		</li>
		<li>4.<a href="#sg_ann"> Advanced syntactic layer / semantic layer</a>
		<ul style="list-style-type:none">
		<li>4.1<a href="#morphsyn_tagset"> Morphosyntactic tagset</a>
		<ul style="list-style-type:none">
			<li>4.1.1<a href="#snt_cas"> Syntax of the case</a>
			<ul style="list-style-type:none">
				<li>4.1.1.1<a href="#nom"> Nominative</a>
				<ul>
					<li>4.1.1.1.1 <a href="#nmn_dpn">Dependent</a>
                          </li>
					<li>4.1.1.1.2 <a href="#nmn_ind">Independent</a>
                          </li>
					<li>4.1.1.1.3 <a href="#nmn_ctc">Citation</a>
                          </li>
					<li>4.1.1.1.4 <a href="#nmn_pnd">Nominativus pendens</a>
                          </li>
					<li>4.1.1.1.5 <a href="#nmn_exc">Exclamation</a>
                          </li>
				</ul>
				</li>
				<li>4.1.1.2<a href="#gnt"> Genitive</a>
                      </li>
				<li>4.1.1.3<a href="#dtv"> Dative</a>
                      </li>
				<li>4.1.1.4<a href="#acc"> Accusative</a>
                      </li>
				<li>4.1.1.5<a href="#prp"> Adposition</a>
                      </li>
			</ul>
			</li>
			<li>4.1.2<a href="#adj_prp"> Adjective proper</a>
                  </li>
			<li>4.1.3<a href="#sbs_adj"> Substantive adjective</a>
                  </li>
			<li>4.1.4<a href="#vrb_adj"> Verbal adjective in τος/τεος</a>
                  </li>
			<li>4.1.5<a href="#vrb_adj_sbs"> Substantive verbal adjective in τος/τεος</a>
                  </li>
			<li>4.1.6<a href="#sbs_prn"> Substantive pronoun</a>
                  </li>
			<li>4.1.7<a href="#adj_prn"> Adjective pronoun</a>
                  </li>
			<li>4.1.8<a href="#fnt_moo"> Syntax of the finite verb</a>
                  </li>
			<li>4.1.9<a href="#adj_prt"> Adjective participle</a>
                  </li>
			<li>4.1.10<a href="#sbs_prt"> Substantive participle</a>
                  </li>
			<li>4.1.11<a href="#inf"> Syntax of the infinitive</a>
				<ul>
					<li>4.1.11.1 <a href="#dpn_inf">Dependent</a>
                      </li>
					<li>4.1.11.2 <a href="#idp_inf">Independent</a>
                      </li>
					<li>4.1.11.3 <a href="#art_inf">Articular infinitive</a>
                      </li>
					<li>4.1.11.4 <a href="#vrl_inf">Verbal infinitive</a>
                      </li>
				</ul>
			</li>
			<li>4.1.12<a href="#adv_snt"> Syntax of the adverb</a>
				<ul>
                      <li>4.1.12.1 <a href="#part">Particles</a>
                      </li>
                    </ul>
			</li>
		</ul>
		</li>
		</li>
		</ul>
		</li>
	</ul>
</a>




<a id="int">
<h3>1. Introduction</h3>

<p>The Ancient Greek Dependency Treebank 2.0 (AGDT 2.0) is an extension of the <a href="http://nlp.perseus.tufts.edu/syntax/treebank/greek.html" target="_blank">Ancient Greek Dependency Treebank 1.0</a> (AGDT 1.0), which subsumes and integrates the morphosyntactic analysis available in the AGDT 1.0 with a more fine-grained annotation based on the categories identified in <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">H. W. Smyth's Greek Grammar for Colleges</a> (SG).</p>

<p>Despite having being published at the beginning of the 20th century, SG turns out to be, in its foundations, a highly valuable compendium of Ancient Greek grammar, which is still widely used and consulted in the Anglo-Saxon world to study the Greek language. Because of its intermediate nature/size between a school grammar and a reference grammar, SG is particularly well suited to provide the framework which a computational model for Ancient Greek (AG) grammar can be built on. Such a computional model, which is outlined in the present guidelines, introduces modifications and integrations to SG to make it fully coherent, and consistent with more recent linguistic literature.</p> 

<p>
The AGDT 2.0 is organized into three layers: the morphological layer, the (Prague) syntactic layer, and the (SG) advanced syntax layer (which someone may want to call "semantic layer"). The first and the second layer were already present in the AGDT 1.0: they have been incorporated into the AGDT 2.0, even though modifications and corrections have been introduced, which are detailed in Section <a href="#mph_tgs">2</a> and <a href="#prg_ann">3</a>.
</p>

<p>The advanced syntax layer allows, by means of a complex algorithm relying on morphosyntax, the (guided) annotation of the syntax of the sentence as described by SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+900&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">900</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2687</a>): this includes semantic roles (SRs) (such as "location", expressed, e.g., by the SG "genitive of place" or "dative of place"; see also <a href="http://www.worldcat.org/title/on-the-meaning-of-prepositions-and-cases-the-expression-of-semantic-roles-in-ancient-greek/oclc/227038149&amp;referer=brief_results" target="_blank">Luraghi 2003</a>) and the various types of subordinate clause. In the present guidelines, I will use the term "(morpho-)syntax" in Smyth's terms, i.e. to also include the analysis of what is usually described in some theoretical frameworks as belonging to a semantic layer. This is in accordance with the view that grammar consists of pairings of form and meaning, and not separate components (see, among others, <a href="http://www.worldcat.org/title/foundations-of-cognitive-grammar/oclc/13859017&amp;referer=brief_results" target="_blank">Langacker 1981-1991</a>). The SG annotation algorithm has been written in such a way that a certain SR can always be annotated at every grammar level (i.e., although "manner" can be expressed by a dative or an adverb or a PP, it is possible to label it in each case).</p>

<p>The advanced syntax annotation (also referred to, for convenience, as "SG annotation") is designed to complement the annotation of the Prague syntactic layer, i.e., a revised version of the analytical layer of the Prague Dependency Treebank 2.0, already adopted in the AGDT 1.0 (henceforth "Prague annotation"). The Prague analytical layer also informs the syntactic layer adopted in the <a href="http://www.hf.uio.no/ifikk/english/research/projects/proiel/" target="_blank">PROIEL</a> annotation, which guarantees that the AGDT and the PROIEL treebank are to a very large extent compatible. The Prague annotation provides labels for (morpho-)syntactic categories, such as SBJ ("subject") or APOS ("apposition"), which, not being PoS-specific, can be kept out of the SG algorithm and superimposed on it. Moreover, the Prague syntactic layer comprises the annotation of the argument structure of verbs, adjectives, and adverbs, which is displayed in the distinction between OBJs and ADVs (see Section <a href="#prg_ann">3</a>).</p>

<p>The present guidelines are devised in such a way that the reader is, whenever possible, referred to SG for a detailed definition and examples of a given grammar phenomenon, I focusing on the information that is strictly relevant to the annotation process. Wherever there is a discrepancy between SG and some instruction in the present guidelines, the latter get priority. For a small set of grammatical phenomena, more than one annotation option is licensed: a primary annotation style is kept distinct from a secondary annotation style, which, if chosen, has to be declared.</p>

<p>The language the guidelines focus on is Classical Greek: additions and adaptations for other stages of the language will follow.</p>

<p>In Section <a href="#mph_tgs">2</a>, I describe the morphological tagset. I define the Prague labels accompanied by links to key treebanking examples in Section <a href="#prg_ann">3</a>, which integrates/corrects the already existing guidelines for the <a href="http://nlp.perseus.tufts.edu/syntax/treebank/greek.html" target="_blank">AGDT 1.0</a>. In Section <a href="#sg_ann">4</a>, I deal with the SG algorithm of the advanced syntax layer (also called "semantic layer").</p>
</a> 

<a id="mph_tgs">
<h3>2. Morphological layer</h3>

<p>
The morphological tagset consists of 11 categories, most of which can be identified on the basis of their lemmas in the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>. When annotating a PoS, the system allows addition of the lemma (<em>not word form</em>) translation for each word form (details, including the formalism, are provided below), in order to enable automatic creation of a gloss according to the <a href="http://www.eva.mpg.de/lingua/resources/glossing-rules.php" target="_blank">Leipzig Glossing Rules</a> and allow connection with existing computational resources for the English language.</p>

<p>The lemma translation should be <em>as literal as possible</em>, <em>always the same whenever possible</em>, and <em>preferably taken from the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>
          </em> (or <em>
            <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">SG</a>
          </em>): this is made easy because, in the <a href="http://www.perseus.tufts.edu/hopper/collection?collection=Perseus:collection:Greco-Roman" target="_blank">Perseus Digital Library</a>, the reader can access the LSJ lemma of a Greek word form contained in a text by clicking on it. Moreover, if that exact word form is quoted in the dictionary, it is showed in bold characters.</p>


<p>
In the annotation environment "Arethusa", the morphological annotation of each word is performed using the "morph" tab. The annotator can there choose among the options that are automatically generated or add their own, if the right analysis is not available. It is to be noted that the automatically generated options are the output of the tagger Morpheus (also available in 
<a href="http://www.perseus.tufts.edu/hopper/morph?redirect=true&amp;lang=greek" target="_blank">Perseus</a>), which can contain inconsistencies or different analyses from the ones required for the present annotation. The annotator has therefore to pay much attention to annotate morphology only according to the present guidelines, without relying uncritically on Morpheus, but being ready to add a right morphologycal analysis, if missing. The PoS tagset is the following:
</p>


<ol>
<li>
            <a href="#art">article</a>
          </li>
<li>
            <a href="#nou">noun(/substantive)</a>
          </li>
<li>
            <a href="#adj">adjective</a>
          </li>
<li>
            <a href="#prn">pronoun</a>
          </li>
<li>
            <a href="#vrb">verb</a>
          </li>
<li>
            <a href="#adv">adverb</a>
          </li>
<li>
            <a href="#adp">adposition</a>
          </li>
<li>
            <a href="#cnj">conjunction</a>
          </li>
<li>
            <a href="#nmr">numeral</a>
          </li>
<li>
            <a href="#exc">interjection</a>
          </li>
<li>
            <a href="#pct">punctuation</a>
          </li>
</ol>

<a id="art">
<h4>2.1 Article</h4>

<p>
AG has one definite article (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1118&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1118</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1189&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1189</a>), inflected and so annotated for gender, number, and case (ὁ, ἡ, τό). Note that in AG the same forms can also be used (<em>and hence should be accordingly annotated</em>) as 
<a href="#prn">pronouns</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1105&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1105</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1106&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1106</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1117&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1117</a>). The annotator should pay attention here, because the system tends not to suggest the pronominal analysis, which has to be added manually.</p>

<p>
The article can have substantive-making power (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1153&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1153</a>). However, in phrases such as οἱ ἀμφί τινα or οἱ ἐκεῖ (i.e. when the article/pronoun is associated <em>with a PP</em> or <em>an adverb</em>), ὁ is annotated as a pronoun (even though traditional grammar takes them as substantivized PPs and adverbs). This annotation style, which allows us to keep the SG algorithm more constrained, is made possible by analogy with examples such as τὰ τῶν στρατιωτῶν, where τῶν στρατιωτῶν is taken to be dependent on ὁ (and so the latter is a pronoun).
</p>

<p>
Although the forms τις-τι may have the force of an indefinite article (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1267&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1267</a>), they should not be annotated as articles but as <a href="#prn">pronouns</a>.</p>

<p>The lemma translation for article ὁ is <code>the</code>, while that for pronoun ὁ <code>that</code>.</p>

<p>The article always takes the Prague annotation label ATR; the pronoun takes the same syntactic labels as the <a href="#nou">noun</a>. There is no SG annotation for the article, while the pronoun has access to the algorithm for the <a href="#snt_cas">syntax of the case</a>.</p>
</a>

<a id="nou">
<h4>2.2 Noun(/Substantive)</h4>

<p>In AG the noun/substantive (henceforth simply "noun") is inflected and so annotated for gender, number, and case (consult the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>). If an adjective is also used as a noun, but is not lemmatized independently of the adjective lemma (i.e., no separate entry in the dictionary), <em>it is morphologically categorized as an adjective</em>.</p>

<p>The lemma translation for the noun should be an English noun (always in its singular form, wherever possible). Some examples are:</p>

<ul>
<li>ὁδόν <code>way</code>
            </li>
<li>σωμάτων <code>body</code>
            </li>
<li>πολυρριζία <code>possession.of.many.roots</code> (when a translation includes more words, they should be joined by a full stop)</li>
<li>ποιμένος <code>shepherd</code>
            </li>
</ul>
	
<p>The Prague annotation label for the noun can be SBJ, OBJ, ATR, ADV, PNOM, OCOMP, or APOS. The SG tagset allows the annotation of the <a href="#snt_cas">syntax of the case</a> for each noun.</p>  
</a>

<a id="prn">
<h4>2.3 Pronoun</h4>

<p>The term "pronoun" is used here in its traditional definition, i.e. <em>as a cover term for both substantive and adjective pronouns</em>. Pronouns are a set of word forms, which are listed in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">340</a>). The pronoun is annotated for gender, number, and case. The annotator should pay attention to the options suggested <em>because for some pronouns the erroneous PoS "adjective" is suggested</em>. This means that the right analysis as pronoun has to be added manually.</p>

<p>The lemma translation for the pronoun should be an English pronoun. Some examples are:</p>

<ul>
<li>μοι <code>I</code>
            </li>
<li>αὐτοῦ <code>him</code> or <code>it</code> (depending on the genre)</li>
<li>αὐτῇ  <code>her</code>
            </li>
<li>αὐταί <code>herself</code>
            </li>
<li>τοῦδε <code>this</code>
            </li>	
<li>τούτων <code>this</code>
            </li>	
<li>ἑαυτῷ <code>himself</code>
            </li>
<li>ἐμός <code>my</code>
            </li>
<li>ἀλλήλαιν <code>one.another</code>
            </li>
</ul>

<p>Consult the SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">340</a>) for the lemma translation, especially for correlative pronouns (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+340&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">340</a>). Particular attention should be paid to relative and interrogative pronouns (used adjectively or substantively): a form can correspond to different kinds of pronouns: ὅς, ἥ, ὅ can, for example, be a demonstrative or a relative pronoun. In the LSJ different kinds of pronoun having the same form are usually lemmatized together, and the different functions are signalled in different sections with letters or numbers. Since it can be hard/impossible to detect the category "relative" and "interrogative" relying only on the morphological and syntactic annotation here adopted, the lemma field should contain this information. In order to make this task easier (instead of preserving the letters or numbers of the LSJ), the annotator will adopt the following notation in the lemma field:</p>

<ul>
<li>
              <code>ὅς.R</code>
            </li>
<li>
              <code>ὅστις.R</code>
            </li>
<li>
              <code>ὅστις.I</code>
            </li>
</ul>

<p>The notations <code>.R</code> or <code>.I</code> will be added to every lemma which is a relative or interrogative pronoun respectively. Note that the automated morphological annotation provided by the tagger Morpheus does not contain such notations: they have to be added manually.</p>

<p>If the pronoun is a substantive pronoun, one of the Prague annotation labels used for the <a href="#nou">noun</a> applies, while if it is an adjective pronoun, one of the Prague annotation labels for the <a href="#adj">adjective</a> in adjective function is used. The SG tagset allows us to specify if the pronoun is a <a href="#sbs_prn">substantive pronoun</a> or an <a href="#adj_prn">adjective pronoun</a>. In the former case, the SG tagset allows annotation of its <a href="#snt_cas">syntax of the case</a> (whose categories are the same as those for the <a href="#nou">noun</a>). In the latter case, no further SG annotation is allowed (as occurs with any other <a href="#adj">adjective</a> in adjective function).</p>  
</a>

<a id="adj">
<h4>2.4 Adjective</h4>

<p>The adjective is the PoS that is inflected and so annotated for gender, number, case, and degree, and is lemmatized as such in the 
<a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>.</p>

<p>The lemma translation for the adjective should be an English positive adjective (or, if this is not possible, an equivalent expression) or a noun, if appropriate. Some examples are:</p>
<ul>
<li>εὐέλπιδος <code>hopeful</code>
            </li>
<li>ἱερός <code>temple</code> (when the adjective is substantivized and means "temple")</li>
<li>γυιαρκής <code>strengthening.the.limbs</code>
            </li>
<li>μακρότερος <code>small</code>
            </li>
<li>τάχιστος <code>quick</code>
            </li>
<li>πρότερος <code>former</code> (there is no positive adjective, so the translation can be a comparative)</li>
</ul>

<p>The Prague annotation label is usually ATR, PNOM, or OCOMP, if the adjective has adjective function; on the contrary, if it is used as a substantive adjective, one of the Prague annotation labels for the <a href="#nou">noun</a> is used. The SG tagset allows one to specify whether the adjective is also used as such or as a 
<a href="#sbs_adj">substantive adjective</a>. In the former case, no SG annotation is available; in the latter case, the SG annotation algorithm allows access to the same tagset for the 
<a href="#snt_cas">syntax of the case</a> 
as that used for the <a href="#nou">noun</a>.</p>
</a>

<a id="vrb">
<h4>2.5 Verb</h4>

<p>
The verb is the PoS annotated for person, number, tense, mood, and voice (and gender and case if the verb is a participle), and is lemmatized as such in the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>. Note that the annotation of the voice of the verb is strictly morphological: the form of the voice is annotated as active, passive, or medio-passive (if the form can be both active and passive), independently of the meaning. It may happen that the Morpheus tagger outputs lemmas followed by a number: they should be deleted in the entry (i.e., lemma field).</p>

<p>The lemma translation for the adjective should be an English verb. A few examples are:</p>

<ul>
<li>ἔρχομαι <code>come</code>
            </li>
<li>ἀβουλέω <code>be.unwilling</code>
            </li>
</ul>

<p>if the verb is in a finite mood, it usually takes the Prague annotation labels PRED (main clause), SBJ or OBJ (substantive clause), ATR (adjective clause proper; if there is a substantivized relative clause, the labels are the same as those for the <a href="#nou">noun</a>), or ADV (adverb clause). If the verb is a participle it can take the label ATR (attributive participle), ADV (circumstantial participle), OBJ, OCOMP, or PNOM (supplementary participle), or those for the <a href="#nou">noun</a>, if the participle is a substantive participle. Similarly, an infinitive can take the same labels as a noun if it is articular, and SBJ or OBJ (occasionally ADV), if it is "verbal". On the basis of the mood selected, i.e., whether the verb is in the indicative, subjunctive, optative, or imperative mood, i.e. a <a href="#fnt_moo">finite mood</a>, or in the <a href="#inf">infinitive</a> or <a href="#adj_prt">participle</a> mood, i.e., non-finite moods, the SG tagset allows annotation of its syntax through a complex algorithm (see Section <a href="#sg_ann">4</a>).
</p>
</a>

<a id="adv1">
<h4 id="adv">2.6 Adverb</h4>
<p>
The adverb is morphologically defined as the PoS having an invariable form (with the exception of the degree feature; see SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+341&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">341</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+346&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">346</a>) for an introduction on adverbs). Adverbs deriving from adjectives are not lemmatized independently in the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a>, but are contained in the adjective lemma: <em>so the lemma for an adverb should be the corresponding adjective lemma</em>. There are, however, a great number of adverbs which are not related to an adjective form and so have an independent entry in 
<a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a> (and so, correspondingly, the lemma will be an adverb).</p> 

<p>Sentence adverbs, which are labeled as particles in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1094&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1094</a>), should be tagged as adverbs at the morphological level (the label "particle" is however available in the SG annotation). If a certain noun, adjective, or PP has attained the status of an adverb, <em>it has to be annotated as an adverb</em>. This occurs, for example, with the so-called adverbial accusative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1606&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1606</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1611&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1611</a>) or the head of PPs such as πρὸ πολλοῦ (πρὸ πολλοῦ ποιεῖσθαι, "to esteem highly") or ἀφ᾽ οὗ ("since"). The annotator has to pay attention here, because the system sometimes suggests a nominal/adjectival analysis, which means that the adverbial analysis has to added manually.</p>

<p>The lemma translation should be an English adverb. For the translation of correlative adverbs, see SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+346&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">346</a>).</p>

<p>Sentence adverbs (i.e., some of those words that SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2769&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2769</a>) defines as particles) are not required to be translated. If the annotator decides to translate them (or some of them), this should be made in a consistent way and declared. Note that conjunctions (both coordinate and subordinate) are here treated as a separate category from particles (see <a href="#cnj">below</a>).</p>

<p> The Prague annotation label for the adverb is usually ADV, OBJ, AuxY, or AuxZ. The SG tagset allows specification of the SR expressed by the adverb.
</p>
</a>

<a id="adp">
<h4>2.7 Adposition</h4>
<p>
Adposition is a cover term for preposition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1636</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1702</a>) and postpositions (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1665&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1665</a>). Adpositions are morphologically identifiable by being a set of invariable word forms. Their list can be found in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1636</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1702</a>), which includes both proper (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1636</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1698</a>) and improper (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1699&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1699</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1702</a>) adpositions.</p>

<p>The lemma translation should be an English adposition (or an equivalent expression). Some examples are:</p>

<ul>
<li>πρός <code>to</code>
            </li>
<li>πρός <code>toward</code>
            </li>
<li>πρός <code>according.to</code>
            </li>
<li>ἐν <code>according.to</code>
            </li>
<li>πρό <code>in.defence.of</code>
            </li>
</ul>

<p> Adpositions always take the Prague annotation label AuxP. There is no SG annotation available for adpositions.
</p>
</a>

<a id="cnj">
<h4>2.8 Conjunction</h4>
<p>
The Conjunction is an invariable PoS, which can be morphologically defined as a word form belonging to a set. The list can be found in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2163&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2163</a>; <em>excluding the  inferential, causal, and some of the adversative conjunctions</em> (such as <em>μέντοι</em>); <em>these are all treated here as adverbs</em>) and in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2770&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2770</a>).</p>

<p>The lemma translation should be an English conjunction.</p>

<p>The Prague annotation allows the distinction between coordinating conjunctions (COORD) and subordinating conjunctions (AuxC) (AuxY is used with all conjunctions except the last one in a multi-conjunction <a href="#coord">coordination</a>). No SG annotation is available for the conjunction.
</p>
</a>

<a id="nmr">	
<h4>2.9 Numeral</h4>

<p>
The numeral is a word form belonging to the set defined by SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+347&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">347</a>-<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+354&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">354</a>). A numeral is annotated for its type: cardinal, ordinal, or adverb. Cardinal and ordinal numerals are always taken to be <a href="#adj">adjectives</a> (even when a cardinal is indeclinable), and so annotated for gender, number, and case (if declinable).</p>

<p>The lemma translation should be an English numeral.</p>

<p>
Cardinal and ordinal numerals take the Prague annotation labels that <a href="#adj">adjectives</a> take, while adverbs take the Prague labels reserved for <a href="#adv">adverbs</a>. The SG algorithm allows access to the options for <a href="#adj">adjectives</a>, if the numeral is cardinal or ordinal, or those for <a href="#adv">adverbs</a>, if the numeral is an adverb.
</p>
</a>

<a id="exc">	
<h4>2.10 Interjection</h4>

<p>
The interjection is an invariable word form belonging to the set defined in Schwyzer-Debrünner (599-602) (consult also <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ</a>).
</p>

<p>The lemma translation should be an English interjection.</p>

<p>The interjection receives the syntactic label ExD. No SG annotation is available for interjections.</p>

</a>


<a id="pct">	
<h4>2.11 Punctuation</h4>

<p>
Punctuation marks are identifiable by being a set of forms (see SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+188&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">188</a>) and include modern puntuation marks, such as inverted commas for direct speech). They are annotated because they are part of the edition of a text. Their annotation is however to be considered "technical", punctuation not being part of the morphosyntax of a sentence, but rather being able to function as a clue for syntactic phenomena: e.g., apposition is often preceded and followed by a comma.</p>

<p> The Prague annotation labels for puntuation can be AuxX, AuxY, AuxK, AuxG, COORD (and APOS). There is no available SG annotation for punctuation marks.
</p>
</a>
</a>

<a id="prg_ann">
<h3>3. (Prague) syntactic layer</h3>
<p>
The syntactic layer allows annotation of traditional syntactic functions, such as the subject or the predicate nominal. Some of the labels, however, are used with a different meaning from the one adopted in traditional grammar. For example, the label ATR is here used to describe not only adjectives modifying nouns, but also any other kind of depend of the noun having the same or similar function (see below); the labels OBJ and ADV are meant to capture the argument structure of verbs, adjectives, and adverbs (see below). In the following, the terms "noun", "adjective", "verb", and "adverb" are sometimes used to mean the corresponding phrases. The following definitions are accompanied by links to key treebanking examples.
</p>

<a id="pred">
<h4>3.1 PRED</h4>
<p>The PRED ("predicate") function is reserved for the verb of the main clause in a sentence 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=1&amp;doc=4971" target="_blank">tree1</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&amp;doc=4971" target="_blank">tree2</a>). 
	
	Every sentence has one PRED only. Any other verb (finite and non-finite) takes a different label, which shows the function the verb has with respect to its linguistic parent
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=32&amp;doc=4971" target="_blank">tree1</a>).</p>	


</a>

<a id="sbj">
<h4>3.2 SBJ</h4>
<p>The SBJ ("subject") label is attached to every subject (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+927&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">927</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+943&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">943</a>) in a sentence. The subject is typically a noun (or one of its equivalents)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&amp;doc=4971" target="_blank">tree1</a>), 
	
	including the infinitive, both articular (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2025&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2025</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2034&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2034</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=40&amp;doc=4971" target="_blank">tree1</a>)
	
	and verbal (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1984&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1984</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1985&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1985</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=2&amp;doc=4971" target="_blank">tree1</a>), 
	
	 bearing the nominative case, or the genitive case (in the genitive absolute (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2070&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2070</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2075&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2075</a>)) (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&amp;doc=4971" target="_blank">tree1</a>), or the accusative (in the infinitive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1972&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1972</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1981&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1981</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&amp;doc=4971" target="_blank">tree1</a>)
	
	or with the supplementary participle (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2106</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2112b</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2115</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2123</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&amp;doc=4971" target="_blank">tree1</a>)). 
	
	The label SBJ can also apply to a substantive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2574&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2574</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2575&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2575</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&amp;doc=4971" target="_blank">tree1</a>) 
	
	or a substantivized relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2488</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=7&amp;doc=4971" target="_blank">tree1</a>, which annotation is the default one, while the one with adjective clause + elliptical node has to be declared 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=34&amp;doc=4971" target="_blank">tree2</a>)) 
	
	.</p>

</a>

<a id="obj">
<h4>3.3 OBJ</h4>
<p>The OBJ ("object") label is attached to any dependent which is taken to be an argument of the verb, adjective, or adverb (excluding, of course, arguments which are captured by other labels, such as SBJ). The concept of argument is notoriously difficult to define. As a broad definition, an OBJ argument is taken to be a constituent which is selected by a specific verb or class of verbs (and hence cannot accur with any other verb/class of verbs). For example, verbs of movement require a constituent meaning direction ("I went <em>to Rome</em>"), which cannot be used with any other verb: this is therefore an argument. On the contrary, a constituent meaning (time) simultaneous location ("I ate apples <em>yesterday</em>") is not an argument (but an ADV) in that it can virtually modify any kind of verb. If there are doubs, it may be useful to consult <a href="http://verbs.colorado.edu/verb-index/index.php" target="_blank">Verbnet</a>, which shows argument structure for English verbs.</p>
	
<p>	
	An OBJ argument can be a noun (or one of its equivalents)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=8&amp;doc=4971" target="_blank">tree1</a>), 
	
	a PP
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=9&amp;doc=4971" target="_blank">tree1</a>), 
	
	or an adverb
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=10&amp;doc=4971" target="_blank">tree1</a>). 
	
	 An infinitive can also receive the label OBJ, both in the infinitive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2016&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2016</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2024&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2024</a>) 
	 
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&amp;doc=4971" target="_blank">tree1</a>)
	 
	 and as a complement of a verb (or an adjective) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1989&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1989</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2007&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2007</a>)
	 
	 (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=37&amp;doc=4971" target="_blank">tree1</a>). 
	 
	 Similarly, a supplementary participle in indirect discourse (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2106</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2112</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2115</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2123</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>)
	 
	 (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&amp;doc=4971" target="_blank">tree1</a>), 
	 
	 a substantive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2574&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2574</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2575&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2575</a>)
	 
	 (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&amp;doc=4971" target="_blank">tree1</a>),
	 
	 including the εἰ-substantive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2247&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2247</a>)
	 
	 (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=12&amp;doc=4971" target="_blank">tree1</a>),
	 
	 and a substantivized relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2488</a>) 
	 
	 can receive the label OBJ. </p>	
</a>

<a id="atr">
<h4>3.4 ATR</h4>
<p>Any dependent of the noun (or one of its equivalents, excluding the substantive participle and the infinitive when they function as verbs), which is an article
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&amp;doc=4971" target="_blank">tree1</a>), 
	
	an adjective
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=9&amp;doc=4971" target="_blank">tree1</a>), 
	
	or a noun (or one of its equivalents)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=14&amp;doc=4971" target="_blank">tree1</a>) (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=15&amp;doc=4971" target="_blank">tree2</a>), 
	
	a PP
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=16&amp;doc=4971" target="_blank">tree1</a>),
	
	or a relative clause 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&amp;doc=4971" target="_blank">tree1</a>)
	
	receives the ATR ("attribute") function.</p>	
</a>

<a id="adv_fnc">
<h4>3.5 ADV</h4>
<p>The ADV ("adverbial") label is attached to any dependent which is taken to be an optional modification of the verb, the adjective, or the adverb. An ADV modification can be a noun (or one of its equivalents) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=18&amp;doc=4971" target="_blank">tree1</a>), 
	
	a PP
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&amp;doc=4971" target="_blank">tree1</a>),
	
	or an adverb
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&amp;doc=4971" target="_blank">tree1</a>). 
	
	Adverb clauses (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2191&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2191</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2487</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&amp;doc=4971" target="_blank">tree1</a>), 
	
	as well as a substantivized relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2488&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2488</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=20&amp;doc=4971" target="_blank">tree1</a>, 
	
	which annotation is the default one, while the alternative annotation style, i.e., adjective clause + elliptical node is to be declared
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=35&amp;doc=4971" target="_blank">tree1</a>)), 
	
	the infinitive of purpose and result (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2008</a>-<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2011</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=41&amp;doc=4971" target="_blank">tree1</a>), 
	
	and the circumstantial participle (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2054&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2054</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2087&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2087</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&amp;doc=4971" target="_blank">tree1</a>) 
	
	are ADV modifications as well.</p>	
</a>

<a id="atvv">
<h4>3.6 ATV/AtvV</h4>
<p>ATV/AtvV ("verbal attribute") is in the AGDT 1.0 the label for those adjectives agreeing with a subject but functioning as adjuncts. They are annotated as ADV and appended to the governing verb in the AGDT 2.0
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=7&amp;doc=4971" target="_blank">tree1</a>). 
	
	Alternatively, according to the annotation style of the AGDT 1.0, they can receive the label ATV/AtvV and be appended to the subject/verb (see the guidelines for the <a href="http://nlp.perseus.tufts.edu/syntax/treebank/greek.html" target="_blank">AGDT 1.0</a> for more information)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=36&amp;doc=4971" target="_blank">tree1</a>). 
	
	This latter annotation style has to be declared.</p>	
</a>

<a id="pnom">
<h4>3.7 PNOM</h4>
<p>The PNOM ("predicate nominal") label applies to every noun 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&amp;doc=4971" target="_blank">tree1</a>)
	
	(or one of its equivalents, including the infinitive (especially SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1982&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1982</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1983&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1983</a>)) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=39&amp;doc=4971" target="_blank">tree1</a>)
	
	or adjective (including the adjective pronoun and the supplementary participle not in indirect discourse; SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2094</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2105</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2123</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=21&amp;doc=4971" target="_blank">tree2</a>))
	
	which are dependent on a copulative verb (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+917&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">917</a>). </p>	
</a>

<a id="ocomp">
<h4>3.8 OCOMP</h4>
<p>The function OCOMP ("object complement") is reserved for the predicative accusative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1613&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1613</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1618&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1618</a>) 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=22&amp;doc=4971" target="_blank">tree1</a>) 
	
	and, more in general, any predicative complement not agreeing with the subject. It is also used with the supplementary participle not in indirect discourse with verbs of perceiving and finding (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2110&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2110</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2115</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&amp;doc=4971" target="_blank">tree1</a>).</p>	
</a>

<a id="coord">
<h4>3.9 COORD</h4>
<p>The function COORD ("coordination") is reserved for coordinate conjunctions (the list can be found in SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2163&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2163</a>, <em>excluding the  inferential, causal, and some of the adversative conjunctions</em> (<em>such as μέντοι</em>);<em> these are all treated here as </em>(<em>sentence</em>) <em>adverbs</em>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&amp;doc=4971" target="_blank">tree1</a>)
	
	and commas coordinating two or more constituents when no conjunction is present (asyndeton)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&amp;doc=4971" target="_blank">tree1</a>). 
	
	If there are correlative conjunctions (or more coordinating commas without conjunctions), the last one by rule takes the function COORD, while the preceding ones take the technical label AuxY and are attached to the last one
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&amp;doc=4971" target="_blank">tree1</a>). Every coordinated constituent takes the suffix _CO (if function words, such as AuxPs, are coordinated, the suffix is attached to their children).</p>	
</a>

<a id="apos">
<h4>3.10 APOS</h4>
<p>There are two possible annotations for apposition. In the first annotation style, the label APOS ("apposition"/"appositive") is attached to an appositive noun 
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=27&amp;doc=4971" target="_blank">tree1</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=28&amp;doc=4971" target="_blank">tree2</a>)
	
	(SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+916&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">916</a>) or an equivalent of an appositive noun (including a substantivized relative clause and a substantive or adverb clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+976&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">976</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+995&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">995</a>))
	
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=29&amp;doc=4971" target="_blank">tree1</a>)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=30&amp;doc=4971" target="_blank">tree2</a>), 
	
	and the appositive is annotated as a dependent of the noun it specifies. 
	
	Note that, according to this anotation style, the appositive is always a noun and annotated in the same way, independently of whether it functions as an attribute or is, for example, descriptive (see SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+976&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">976</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+995&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">995</a>). In the second annotation style, used in AGDT 1.0, the label APOS marks the comma separating a noun and its appositive, and the noun and its appositive take the function required within the sentence (with suffix _AP; see the <a href="http://nlp.perseus.tufts.edu/syntax/treebank/agdt/1.7/docs/guidelines.pdf" target="_blank">AGDT 1.0 guidelines</a>); if the appositive is an attributive noun it is attached to the noun and labeled as ATR. If this second annotation style is adopted, it has to be declared.</p>
	
<p>In the SG annotation (if the first annotation style for apposition is adopted) the analysis of an appositive noun is (technically) the same as that of the governing noun. The annotator should pay attention to the many examples of clauses in apposition to a noun, which have to be fully annotated: <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=52&amp;doc=4971" target="_blank">tree1</a>
          </p>
</a>

<a id="mwe">
<h4>3.11 MWE</h4>	
<p>
The label MWE is reseverd for multiword expressions. When there is an phrase where it is not clear which the function/meaning of the single words are, the head of that phrase takes the function of the phrase as a whole, while the other words are attached to it with the label MWE.
</p>
</a>

<a id="auxp">
<h4>3.12 AuxP</h4>
<p>The function AuxP ("preposition") is reserved for adpositions (whose list is in SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1636&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1636</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1702&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1702</a>)
	
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=6&amp;doc=4971" target="_blank">tree1</a>).</p>	
</a>

<a id="auxc">
<h4>3.13 AuxC</h4>
<p>The function AuxC ("conjunction") is used to label subordinate conjunctions only. Their list is in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2770&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2770</a>, excluding the local ones, which have to be treated as relative pronouns/adverbs)
	
	(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&amp;doc=4971" target="_blank">tree1</a>).</p>
		
</a>

<a id="auxx">
<h4>3.14 AuxX</h4>
<p>AuxX is the label used for commas, unless they function as coodinating commas when no conjunction is present (in which case they take the <a href="#coord">COORD</a> function (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&amp;doc=4971" target="_blank">tree1</a>); when there is a coordination with conjunctions and commas, see the example in <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&amp;doc=4971" target="_blank">tree1</a>). A non-coordinating comma is appended to its preceding word. If two commas mark a vocative or a parenthetical clause, they are both appended (with label AuxX) to the vocative and the head of the parenthetical clause respectively.</p>
</a>

<a id="auxg">
<h4>3.15 AuxG</h4>
<p>The label AuxG is used for modern punctuation marks (other than commas) that can be found in an edition of Ancient Greek texts (such as inverted commas introducing direct speech).</p>	
</a>

<a id="auxk">
<h4>3.16 AuxK</h4>
<p>The label AuxK is used for the final punctuation mark of a sentence (which can be a period, a semicolon, or the point above the line). The node is always appended to the ROOT node (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=31&amp;doc=4971" target="_blank">tree1</a>).</p>	
</a>

<a id="auxy">
<h4>3.17 AuxY</h4>
<p>The AuxY label is used to mark technical nodes (such as correlative conjunctions attached to the last one, which is taken to be the coordinating one: see <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&amp;doc=4971" target="_blank">tree1</a> and <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=25&amp;doc=4971" target="_blank">tree2</a>) or for sentence adverbs (i.e., non-conjunction particles in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1094&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1094</a>), but only those whose scope is the whole sentence).</p>	
</a>

<a id="auxz">
<h4>3.18 AuxZ</h4>
<p>The AuxZ label is reserved for logical operators that are adverbs, such as those meaning "not", "even", and "also".</p>	
</a>

<a id="exd">
<h4>3.19 ExD</h4>
<p>The label ExD is used for those constituents that do not syntactically belong to a sentence, such as vocatives and the head of a parenthetical clause. They are appended to the PRED node.</p>	
</a>

<a id="suffixes">
<h4>3.20 Suffixes</h4>
<p>Each syntactic label can be specified by a suffix. There are two main suffixes: _CO and _AP</p>

<a id="_CO">
<h4>3.20.1 _CO</h4>
<p>The suffix _CO is added to all conjuncts in a coordination.</p>
</a>

<a id="_AP">
<h4>3.20.2 _AP</h4>
<p>The suffix _AP is used <em>only</em> if the second annotation style for apposition is chosen (which has to be declared). The suffix is attached to a noun and its appositive. There is also the variant _AP_CO, when there are coordinate appositives.</p>
</a>


</a>


</a>

<a id="sg_ann">
<h3>4. (Smyth's Grammar) Advanced syntax layer / semantic layer</h3>

<p>
The advanced syntax layer allows annotation of the rich number of categories described by Smyth (1920). In some modern linguistic frameworks, some of these categories are described as morphosyntactic and some others as semantic.
</p>

<a id="morphsyn_tagset">	
<h3>4.1 Morphosyntactic tagset</h3>

<p>
The morphosyntactic tagset consists of those categories which, on the basis of the part of speech, can be defined if their syntax is also taken into account. I call such categories morphosyntactic. In the following list, the categories of the morphological tagset which give access to the morphosyntactic categories of the SG annotation are given in parentheses (the lack of a nested menu under a morphological tag means that no SG annotation is available). For those PoS having case, the case has to be re-selected at this layer, because the syntactic case can be different from the morphological one (see <a href="#snt_cas">below</a>).
</p>

<ol>
	<li>(article)</li>

	<li>(noun/substantive)
		<ul>
			<li>
                  <a href="#snt_cas">
                    <span style="font-style:italic">syntax of the case</span>
                  </a>
                </li>
		</ul>
	</li>

	<li>(adjective)
		<ul>
			<li>
                  <a href="#adj_prp">adjective proper</a>
                </li>	
			<li>
                  <a href="#sbs_adj">substantive adjective</a>
				<ul>
					<li>
                      <a href="#snt_cas">
                        <span style="font-style:italic">syntax of the case</span>
                      </a>
                    </li>
				</ul>
			</li>
			<li>
                  <a href="#vrb_adj">verbal adjective in τος/τεος</a>
                </li>
			<li>
                  <a href="#vrb_adj_sbs">substantive verbal adjective in τος/τεος</a>
				<ul>
					<li>
                      <a href="#snt_cas">
                        <span style="font-style:italic">syntax of the case</span>
                      </a>
                    </li>
				</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>
	
	<li>(pronoun)
		<ul>
			<li>
                  <a href="#sbs_prn">substantive pronoun</a>
				<ul>
					<li>
                      <a href="#snt_cas">
                        <span style="font-style:italic">syntax of the case</span>
                      </a>
                    </li>
				</ul>
			</li>
			<li>
                  <a href="#adj_prn">adjective pronoun</a>
                </li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>

	<li>(verb)
		<ul>
			<li>(a finite mood, i.e., indicative, optative, subjunctive, and imperative)
				<ul>
					<li>
                      <a href="#fnt_moo">
                        <span style="font-style:italic">syntax of the finite verb</span>
                      </a>
                    </li>
				</ul>
			</li>
			<li>(participle)
				<ul>
					<li>
                      <a href="#adj_prt">adjective participle</a>
                    </li>
					<li>
                      <a href="#sbs_prt">substantive participle</a>
						<ul>
							<li>
                          <a href="#snt_cas">
                            <span style="font-style:italic">syntax of the case</span>
                          </a>
                        </li>
						</ul>
					</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
			</li>
			<li>(infinitive)
				<ul>
					<li>
                      <a href="#inf">
                        <span style="font-style:italic">syntax of the infinitive</span>
                      </a>
                    </li>
				</ul>
			</li>
		</ul>
	</li>
	<li>(adverb)
		<ul>
			<li>
                  <a href="#adv_snt">
                    <span style="font-style:italic">syntax of the adverb</span>
                  </a>
                </li>
		</ul>
	</li>	
	<li>(adposition)</li>
	<li>(conjunction)</li>
	<li>(numeral)
		<ul>
			<li>cardinal
				<ul>
					<li>
                      <a href="#adj_prp">adjective</a>
                    </li>	
					<li>
                      <a href="#sbs_adj">substantive</a>
						<ul>
							<li>
                          <a href="#snt_cas">
                            <span style="font-style:italic">syntax of the case</span>
                          </a>
                        </li>
						</ul>
					</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
			</li>
			<li>ordinal
				<ul>
					<li>
                      <a href="#adj_prp">adjective</a>
                    </li>	
					<li>
                      <a href="#sbs_adj">substantive</a>
						<ul>
							<li>
                          <a href="#snt_cas">
                            <span style="font-style:italic">syntax of the case</span>
                          </a>
                        </li>
						</ul>
					</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
			</li>
			<li>adverb
				<ul>
					<li>
                      <a href="#adv_snt">
                        <span style="font-style:italic">syntax of the adverb</span>
                      </a>
                    </li>
				</ul>
			</li>
		</ul>
	</li>
	<li>(interjection)</li>
	<li>(punctuation)</li>
</ol>


<a id="snt_cas">	
<h4>4.1.1 Syntax of the case</h4>

<p>
In traditional grammar, the syntax of the case is concerned with the functions of the cases of the noun and 
its syntactic equivalents (the substantive pronoun, the substantive adjective, including the verbal ones in τος/τεος, the substantive participle, the articular infinitive, and the substantivized adjective clause; henceforth I will usually use the term "noun" to mean "noun" plus these syntactic equivalents). It deals with the distinction between, for example, an <a href="#acc_aff">accusative of the external object</a> and an <a href="#acc_rsp">accusative of respect</a>. In the treebank 2.0, it is possible to fully annotate the syntax of the case by means of an elaborate algorithm. Most of the categories covered by the traditional syntax of the case are today treated under the rubric of semantic roles (in the following, the term "(semantic) function" is sometimes used as a synonym for "semantic role").
</p>

<p>
After the morphological annotation, the annotator is required to annotate the syntax of a noun, starting from the selection of the noun's syntactic case. Even though the syntactic case of a noun usually corresponds to its morphological case, there are some cases where this does not hold true: the so-called phenomenon of "attraction" of the relative pronoun (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2522&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2522</a>), for example, calls for a clear distinction between the morphology and the syntax of a case. Similarly, when a genitive or an accusative are analyzed as subjects or predicate nominals, the syntactic case selected should be the nominative.</p>

<p>The dependent and independent functions of each case are always kept distinct: "dependent" is a case function of a noun which is syntactically governed, while "independent" is a case function of a noun which is not syntactically dependent on any other word in the sentence. A noun with an independent function is very often, but not always, the head of a sentence, syntactic "independency" sometimes corresponding to a technical dependency in the treebank: e.g., a 
<a href="#nmn_pnd">nominativus pendens</a> is technically attached to a PRED, although it is not syntactically dependent on it.
</p>

<p>
Following SG, the annotation algorithm distinguishes between main and adpositional functions for each case: e.g., the semantic function encoded by the 
<a href="#acc_trm">terminal accusative</a> (accusative of direction) is a main function (because it can be expressed by the bare case), while an adpositional function is a semantic function that can be encoded only by a case plus an adposition (e.g., "cause" expressed by 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά + accusative</a>, which cannot be expressed by the bare accusative case). A case can sometimes express a main function also in conjunction with an adposition, which can define it more specifically: e.g., "direction" can also be encoded by, for example, 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a> or 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">παρά</a> + accusative. A main function, whether or not it is specified by an adposition, is <em>always</em> annotated by selecting the relevant main function.</p>

<p>By contrast, a function that is shown as adpositional in the annotation algorithm is a semantic function that is always different from those expressed by the main functions (i.e., they cannot be expressed by the bare case). For the sake of perspicuity/simplicity, however, time and place SRs are all grouped together under the relevant non-adpositional function specific to each case (irrespective of the above criterion), with the exception of the genitive of separation and the terminal accusative, which are kept distinct from the genitive of place and the accusative of extent respectively, being in traditional grammar treated as separate categories.</p>

<p>All the instantiations for the adpositional case are grouped and algorithmically placed on the same level as the main functions, even when a certain adpositional function might have been subsumed under one of the main functions, being clearly derived from it: this is a technical expedient to keep all kinds of the adpositional case together, in that it is not possible to claim for a number of adpositional functions whether/from which main function they are derived. When accompanied by an adposition, the function of a case is technically annotated as belonging to the noun, without a claim that the case is the only bearer of the semantic function expressed by it and its governing adposition.
</p>
<p>
The annotator is <em>required</em> to annotate the syntax of the case when the noun <em>only</em> depends on 
</p>

<ul>
<li>(finite and non-finite) verb</li>
<li>verbal adjective in τος/τεος</li>
<li>substantive verbal adjective in τος/τεος</li> 
<li>noun (and its equivalents)</li>
<li>an adposition depending on one of the above categories</li>
</ul>

<p>
When a case depends on any other part of speech, the option "none of the above" is to be selected. The latter option is made available because I do not attempt to provide guidelines for the annotation of dependents of the adjective and the adverb, which is, as is known, more controversial and so more difficult to rule. There are cases where the SG annotation of a noun depending on an adjective or an adverb is rather straightforward, but many others where it is not  (SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1413&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1413</a>) itself acknowledges this). Providing operational criteria for this latter kind of annotation is outside the scope of the present guidelines. However, the annotation environment "Arethusa" technically allows the annotation of a given SR also when a noun depends on an adjective or adverb: the annotator is free to also annotate it, provided that this is declared and the annotation criteria are documented.</p> 

<p>The option "none of the above" is also to be selected when a PP expresses a SR whose annotation is not available (for a selection of SRs can currently be annotated only: see the list below). I have tried to design the algorithm in such a way that it is possible to annotate a certain SR wherever it appears within the clause, independently of its morphosyntactic realization (e.g., "cause" can always be annotated, whether it is expressed by a noun, an adverb, a PP, a participle, or a clause). Note, however, that, following SG and much literature on the subject, the semantics of the adjective, the nominative, and that of some kinds of genitive, dative, and accusative (such as the partitive genitive with verbs or the dative as direct complement of verbs) is not investigated (and so cannot be annotated), there being much less agreement on it. Providing operational criteria for this kind of annotation is outside the scope of the present release of the guidelines.
</p>

<p>
With the aforementioned limitations, the SRs that can be currently annotated are almost all the ones identified in SG. Greek examples for each SR can be read in the relevant sections in SG. In a few cases the definitions I provide below have been modified from the ones that can be found in SG. In the following table, I list (1) the SRs, (2) their definitions, (3) English examples to illustrate them (often literally taken from SG), (4) references to SG with Greek examples, and (5) additional remarks.</p>

<p>The SG sections referred to are only a few of the ones concerned with a given SR (e.g., there is no reference to sections dealing with PPs or clauses expressing the same SR, which can however be easily found in the rest of the document). My definitions are basically formulated following SG, with an attempt to make them compatible with the ones adopted in <a href="http://www.worldcat.org/title/on-the-meaning-of-prepositions-and-cases-the-expression-of-semantic-roles-in-ancient-greek/oclc/227038149&amp;referer=brief_results" target="_blank">Luraghi 2003</a>, <a href="https://www.worldcat.org/title/from-space-to-time-temporal-adverbials-in-the-worlds-languages/oclc/37670970&amp;referer=brief_results" target="_blank">Haspelmath 1997</a> (relative to time SRs), and in <a href="http://verbs.colorado.edu/verb-index/VerbNet_Guidelines.pdf" target="_blank">Verbnet</a>. In general, the system of SRs that is lincesed in the present guidelines is more fine-grained than that in Luraghi 2003 and Verbnet. In the following definitions, I use the term "participant" as a cover term for any entity bearing a SR, and "event" as a cover term for any kind of action or state. Although the definitions are compatible with many of those adopted in Verbnet, there is no claim here about a structural hierarchy of SRs.</p> 

<p>
In the list I do not include the categories 
"divided whole" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1306&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1306</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1319&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1319</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1341</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1371&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1371</a>), 
"subjective/objective genitive" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1328&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1328</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1335</a>),
"dative of direct complement of verbs" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1460&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1460</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1468&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1468</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1471</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1473</a>), 
"dative with the participle of inclination or aversion" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1487&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1487</a>), 
"dative of the participle expressing time" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1498</a>), 
object affected (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1551</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1562&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1562</a>), and
object effected (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1563</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1579&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1579</a>): they are grammatical categories rather than SRs. As stated above, their semantics cannot be annotated in the present version of the guidelines.
</p>


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
                  <br/>
I went to Rome <span style="font-style: italic">with him</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1524&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1524</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1526&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1526</a>
                </td>
<td/>
</tr>

<tr>
<td>accompanying circumstance</td>
<td>abstract participant that denotes the circumstance (but not the manner) accompanying an event</td>
<td/>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>
                </td>
<td>This SR should be selected only when the accompanying circumstance cannot be interpreted as a manner</td>
</tr>

<tr>
<td>advantage</td>
<td>animate participant (or participant composed of animate entities, such as "country") to whose advantage an event occurs</td>
<td>I work <span style="font-style: italic">for you</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1481</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1485</a>
                </td>
<td>This SR is also known as "beneficiary" in the literature</td>
</tr>

<tr>
<td>disadvantage</td>
<td>animate participant (or participant composed of animate entities, such as "country") to whose disadvantage an event occurs</td>
<td>I work <span style="font-style: italic">against you</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1481</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1485</a>
                </td>
<td/>
</tr>

<tr>
<td>agent</td>
<td>participant that causes an event intentionally or consciously</td>
<td>The cake was made <span style="font-style: italic">by him</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1488&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1488</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1494</a>
                </td>
<td>Due to the limitations stated above, this SR cannot be annotated when it is expressed by a nominative (the semantics of the nominative not being investigated in this version of the treebank)</td>
</tr>
<tr>
<td>friendly association</td>
<td>participant that is in a friendly relationship of association or intercourse with a (quasi-)symmetrical participant</td>
<td>
He associates <span style="font-style: italic">with you</span>;<br/>
He agrees <span style="font-style: italic">with you</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1523</a>
                </td>
<td>If the verb is of speaking, the semantic role is "recipient or addressee"</td>
</tr>
<tr>
<td>hostile association</td>
<td>participant that is in a hostile relationship of association or intercourse with a (quasi-)symmetrical participant</td>
<td>
He fights <span style="font-style: italic">with you</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1523</a>
                </td>
<td>If the verb is of speaking, the semantic role is "recipient or addressee"</td>
</tr>
<tr>
<td>cause</td>
<td>participant that is the occasion (external cause) or motive (internal cause) of an event, typically without its consciuosness or intentionality</td>
<td>
I was astonished <span style="font-style: italic">at that</span>;<br/>
I admire him <span style="font-style: italic">for</span> his <span style="font-style: italic">bravery</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1405&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1405</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1408</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1517&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1517</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1520</a>
                </td>
<td/>
</tr>

<tr>
<td>conformity</td>
<td>participant specifying according to what something occurs</td>
<td>
<span style="font-style: italic">in accordance with</span> the <span style="font-style: italic">laws</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1688&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1688</a>
                </td>
<td>This SR is only adpositional</td>
</tr>

<tr>
<td>connection</td>
<td>participant specifying with respect to what the following clause holds</td>
<td>
<span style="font-style: italic">as regards</span> a <span style="font-style: italic">wife</span>, if she conducts herself ill, etc.
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1381</a>
                </td>
<td>This SR is also used when a genitive expresses the SR of respect. Note that, contrary to SG, if a genitive expresses topic with verbs of saying or thinking (or similar verbs), the SR to be selected is "topic"</td>
</tr>
<tr>
<td>crime and accountability</td>
<td>participant that is the crime a participant is accused of</td>
<td>He was accused <span style="font-style: italic">of robbery</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1375&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1375</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1379&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1379</a>
                </td>
<td/>
</tr>
<tr>
<td>(distinction and) comparison</td>
<td>participant to which another participant is compared</td>
<td>he is superior <span style="font-style: italic">to you</span> in eloquence</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1401&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1401</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1404&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1404</a>
                </td>
<td/>
</tr>

<tr>
<td>explanation</td>
<td>participant that specifies by restriction the meaning of another participant</td>
<td>the city <span style="font-style: italic">Rome</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1322&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1322</a>
                </td>
<td/>
</tr>
<tr>
<td>instrument or means</td>
<td>participant which is manipulated by an agent and through which an event occurs</td>
<td>he hit me <span style="font-style: italic">with</span> a <span style="font-style: italic">stone</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1507&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1507</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1511&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1511</a>
                </td>
<td/>
</tr>
<tr>
<td>manner</td>
<td>participant that specifies how an event occurs</td>
<td>he reads <span style="font-style: italic">wonderfully</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>
                </td>
<td>SG definition (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1513</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1515</a>) of manner is not the one adopted here: SG defines manner as "measure of difference" and "respect", both of which are treated here as distinct SRs. My definition of manner basically coincides with SG definition of accompanying circumstance (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>), excluding all those instances that cannot be strictly interpreted as manner specifications</td>
</tr>
<tr>
<td>material or contents</td>
<td>participant that is the material or contents of another participant</td>
<td>spring <span style="font-style: italic">of water</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1323&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1323</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1324&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1324</a>
                </td>
<td/>
</tr>
<tr>
<td>measure</td>
<td>participant specifying the measure of space, time, or degree of a participant</td>
<td>provisions <span style="font-style: italic">of</span> five <span style="font-style: italic">days</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1327</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1581</a>
                </td>
<td>This kind of SR, when governed by a pronoun, might be confused with the partitive genitive. The latter is more general, while the former only quantifies a measure of space, time, and degree (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1317&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1317</a> vs <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>). Time can be annotated as a measure only within the genitive of measure.</td>
</tr>
<tr>
<td>measure of difference</td>
<td>participant that specifies the degree by which a participant differs from another participant in a comparison</td>
<td>many <span style="font-style: italic">days</span> later</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1513</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1515</a>
                </td>
<td/>
</tr>
<tr>
<td>(place) location</td>
<td>place where an event occurs</td>
<td>He lives <span style="font-style: italic">in Milano</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1448</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1449</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1531</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1538</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1581</a>
                </td>
<td/>
</tr>
<tr>
<td>(place) path</td>
<td>place through which an event accurs</td>
<td>we moved <span style="font-style: italic">through</span> the <span style="font-style: italic">land</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1581</a>
                </td>
<td/>
</tr>
<tr>
<td>(place) separation</td>
<td>place from where an event occurs</td>
<td>He went <span style="font-style: italic">from Austria</span> to Italy</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1392</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1400</a>
                </td>
<td>This SR is also known in the literature as "source" or "ablative". In SG the genitive of separation is a broad category including both spatial and non-spatial separation. According to the present scheme, spatial separation is "separation &gt; concrete", while any other kind of metaphorical separation is labeled "sepratation &gt; figurative".</td>
</tr>
<tr>
<td>(place) terminal location/direction</td>
<td>place toward which an event occurs</td>
<td>He went from Austria <span style="font-style: italic">to Italy</span>
                </td>
<td>
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1448</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1449</a>; 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1531</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1538</a>;	
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1588</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1589</a>
                </td>
<td>This SR is also known as "goal" or "allative"</td>
</tr>
<tr>
<td>possession or belonging/possessor</td>
<td>participant that possesses or is interested in possessing another participant</td>
<td>
                  <span style="font-style: italic">Areistotle's</span> books</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1297&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1297</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1305&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1305</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1476&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1476</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1480&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1480</a>
                </td>
<td>The genitive of possession indicates possession, while the dative of possessor interest in possession</td>
</tr>
<tr>
<td>price and value</td>
<td>participant that indicates the price or value of another participant</td>
<td>he bought a table <span style="font-style: italic">for</span> much <span style="font-style: italic">money</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1336&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1336</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1337</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1372&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1372</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1374&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1374</a>
                </td>
<td/>
</tr>
<tr>
<td>purpose</td>
<td>participant that is the aim of an event</td>
<td>He earned money <span style="font-style: italic">for him/that</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1408</a>
                </td>
<td>The SR "purpose" is usually inanimate. When the participant is animate, the context can help in distinguishing between purpose and beneficiary.</td>
</tr>
<tr>
<td>quality</td>
<td>participant that denotes a quality</td>
<td>I am <span style="font-style: italic">of</span> the same <span style="font-style: italic">opinion</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1320&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1320</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1321&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1321</a>
                </td>
<td/>
</tr>
<tr>
<td>relation</td>
<td>animate participant that limits the meaning of an event</td>
<td>it is safer <span style="font-style: italic">for them</span> to flee</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1495</a>
                </td>
<td>This SR and that of "respect" can be distinguished on the basis of animacy</td>
</tr>
<tr>
<td>recipient or addressee</td>
<td>participant to which an event is directed</td>
<td>he told <span style="font-style: italic">me</span> that he was happy</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1469&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1469</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1470&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1470</a>
                </td>
<td>This SR prototypically depends on verbs of giving (recipient) and saying (addressee)</td>
</tr>
<tr>
<td>reference</td>
<td>participant in whose opinion an event holds good</td>
<td>pitful <span style="font-style: italic">in the eyes of many</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1496&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1496</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1497&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1497</a>
                </td>
<td/>
</tr>
<tr>
<td>respect</td>
<td>inanimate participant that delimits the scope of a property or event</td>
<td>harsh <span style="font-style: italic">of voice</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1516</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1600</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1605</a>
                </td>
<td>This SR can be expressed by the dative or the accusative. The SR of connection can be considered as a variant of it.</td>
</tr>
<tr>
<td>feeling</td>
<td>participant who shows participation/interest in an event to an interlocutor</td>
<td>study <span style="font-style: italic">me</span> how to please the eye</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1486&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1486</a>
                </td>
<td/>
</tr>
<tr>
<td>(time) simultaneous location</td>
<td>time at/in/on/during which an event occurs</td>
<td>
                  <span style="font-style: italic">in</span> the <span style="font-style: italic">morning</span>
                  <br/>
<span style="font-style: italic">at five</span>
                  <br/>
<span style="font-style: italic">on</span> the first <span style="font-style: italic">day</span>
                  <br/>
<span style="font-style: italic">during</span> that <span style="font-style: italic">day</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1447</a>; 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1539</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>;
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1582</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1587</a>
</td>
<td>More examples and explanation in Haspelmath 1997:102–116</td>
</tr>
<tr>
<td>(time) sequential location</td>
<td>time before or after which an event occurs</td>
<td>
                  <span style="font-style: italic">before</span>/<span style="font-style: italic">after</span> the <span style="font-style: italic">meal</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1447</a>
                </td>
<td>More examples and explanation in Haspelmath 1997:56–63</td>
</tr>
<tr>
<td>(time) sequential-durative</td>
<td>time by/until which an event occurs or since/from which an event has occurred/occurred</td>
<td>
<span style="font-style: italic">until midnight</span>
                  <br/>
<span style="font-style: italic">since</span> the <span style="font-style: italic">Middle Ages</span>
                  <br/>
<span style="font-style: italic">from now on</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1447</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1539</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>;
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1582</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1587</a>
</td>
<td>More examples and explanation in Haspelmath 1997:66–78</td>
</tr>
<tr>
<td>(time) temporal distance</td>
<td>time in which an event occurred; or how long ago an event occurred</td>
<td>(I will return) <span style="font-style: italic">in</span> three <span style="font-style: italic">weeks</span>
                  <br/> three <span style="font-style: italic">years ago</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1539</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>
                </td>
<td>More examples and explanation in Haspelmath 1997:80–96</td>
</tr>
<tr>
<td>(time) temporal extent</td>
<td>time for which an event has occurred</td>
<td>
                  <span style="font-style: italic">for</span> two <span style="font-style: italic">months</span>
                  <br/>
I wrote the letter <span style="font-style: italic">in</span> two <span style="font-style: italic">hours</span>
</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1447</a>;
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1539</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>;
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1582</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1587</a>
</td>
<td>More examples and explanation in Haspelmath 1997:120–136</td>
</tr>
<tr>
<td>topic</td>
<td>participant that is the topic around which an event of communication or disputing occurs</td>
<td>He talked to me <span style="font-style: italic">about him</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1380</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1381</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1409</a>
                </td>
<td/>
</tr>
<tr>
<td>source</td>
<td>participant that indicates the origin or the source of an event</td>
<td>
                  <span style="font-style: italic">of Darius</span> and <span style="font-style: italic">Parysatis</span> were born two sons; <br/>
I heard that from him</td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1410&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1410</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1411</a>
                </td>
<td>This SR is also known as "origin" in the literature</td>
</tr>
<tr>
<td>standard of judgment</td>
<td>participant by which another participant is measured or judged</td>
<td>it was plain <span style="font-style: italic">from that</span>
                </td>
<td>
                  <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1512&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1512</a>
                </td>
<td/>
</tr>
</table>


<p>
In the following sections I show the algorithms underlying the annotation for each case and their explanation: as for grammar definitions, the reader will constantly be referred to the relevant SG sections.
</p>




<a id="nom">
<h4>4.1.1.1 Nominative</h4>
<p>
The nominative is a grammatical case, which can encode different SRs: this is particularly clear if one considers the SR of the nominative of a passive verb, which 
can correspond to an accusative, or a genitive, or a dative depending on the same verb, when it is in the 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1745&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">active voice</a>. How many and which SRs the nominative can encode is a controversial issue, and so there is no attempt to annotate them in the treebank 2.0: the annotation for the dependent nominative, either as a subject or a predicate nominal, is therefore empty (nominative &gt; dependent). The nominative should be used also when a genitive, a dative, or an accusative are syntactically equivalent to a nominative (for example, when a genitive is the subject or the predicate nominal in a genitive absolute; see also examples of attraction (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1060</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1062</a>)). The following is the full algorithm for the nominative:
</p>
<ul>
	<li>
                  <a href="#nmn_dpn">dependent</a>
                </li>
	<li>
                  <a href="#nmn_ind">independent</a>
		<ul>
			<li>
                      <a href="#nmn_ctc">citation</a>
                    </li>
			<li>
                      <a href="#nmn_pnd">nominativus pendens</a>
                    </li>
			<li>
                      <a href="#nmn_exc">exclamation</a>
                    </li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>		
	<li>none of the above</li>
	<li>I do not know</li>			   
</ul>

<h4>
                <a id="nmn_dpn">4.1.1.1.1 Dependent</a>
              </h4>
<p>
The nominative is dependent if it is grammatically governed by another word in the sentence. In the treebank 2.0, the dependent nominative is annotated only for its syntact function (e.g., whether it is a subject or a predicate nominal), which is possible by using the labels of the Prague syntactic annotation.
</p>

<h4>
                <a id="nmn_ind">4.1.1.1.2 Independent</a>
              </h4>
<p>
Independent is a nominative which does not grammatically depend on another word in the sentence.
</p>
	
<h4>
                <a id="nmn_ctc">4.1.1.1.3 Citation</a>
              </h4>
<p>
The nominative of citation can occur in titles. It can also occur within a sentence (SG 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+940&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">940</a>), and so be (technically) attached to the word it specifies.
</p>
	
<h4>
                <a id="nmn_pnd">4.1.1.1.4 Nominativus pendens</a>
              </h4>
<p>
The nominativus pendens (SG 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+941&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">941</a>) is technically annotated as a dependent on the PRED verb.
</p>	

<h4>
                <a id="nmn_exc">4.1.1.1.5 Exclamation</a>
              </h4>
<p>
The nominative of exclamation (SG 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1288&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1288</a>) can be the head of a sentence or be technically dependent of another word when equivalent to a vocative.
</p>	


</a>

<a id="gnt">
<h4>4.1.1.2 Genitive</h4>
<p>
Three main functions are acknowledged for the bare genitive: the genitive proper, the ablatival genitive, and the genitive of time and place. Differently from SG, the algorithm for the genitive does not distinguish between genitives governed by a noun from those governed by a verb, because such a piece of information 
is expressed by the dependency annotation, which makes it explicit which the governor of a word is. Note that when the genitive is the subject or a predicate nominal in a genitive absolute, and hence is functionally equivalent to a nominative, the syntactic case selected should be the nominative. The same holds when the genitive is attracted (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1060</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1062</a>). If the genitive has the function of OCOMP (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2112&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2112</a>), the annotation ends with the selection of the dependent feature. The following is the algorithm for the genitive (with links referring to the SG sections of the noun-dependent and verb-dependent genitive, which distinction is lost at this level, it resulting from the tree structure). 
</p>
<ul>
	<li>
                  <a href="#gnt_dpn">dependent</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1289&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1289</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1406&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1406</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1408</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1449</a>)
		<ul>
			<li>genitive proper (noun: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1290&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1290</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1337</a>; verb: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1341</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1390&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1390</a>)
				<ul>
				<li>genitive of possession or belonging (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1297&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1297</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1305&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1305</a>)</li>
				<li>genitive of the divided whole (noun: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1306&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1306</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1319&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1319</a>; verb: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1341&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1341</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1371&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1371</a>)</li>
				<li>genitive of quality (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1320&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1320</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1321&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1321</a>)</li>
				<li>genitive of explanation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1322&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1322</a>)</li>
				<li>genitive of material or contents (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1323&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1323</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1324&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1324</a>)</li>
				<li>
                          <a href="#msr">genitive of measure</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1327</a>)
				<ul>
					<li>time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1327</a>)</li>
					<li>space (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1327</a>)</li>
					<li>degree (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1325&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1325</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1327&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1327</a>)</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
				</li>
				<li>subjective/objective genitive (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1328&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1328</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1335</a>)
					<ul>
					<li>subjective genitive (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1330&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1330</a>)</li>
					<li>objective genitive (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1331&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1331</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1335&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1335</a>)</li>
					<li>none of the above</li>
					<li>I do not know</li>
					</ul>
				</li>
				<li>genitive of price and value (noun: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1336&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1336</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1337&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1337</a>; verb: SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1372&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1372</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1374&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1374</a>)</li>
				<li>genitive of crime and accountability (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1375&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1375</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1379&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1379</a>)</li>
				<li>
                          <a href="#tpc">genitive of topic</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1380</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1381</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1409</a>)</li>
				<li>
                          <a href="#cnn">genitive of connection</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1380</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1381</a>)</li>
				<li>none of the above</li>
				<li>I do not know</li>
				</ul>
			</li>	
			<li>ablatival genitive (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1391&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1391</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1411</a>)
				<ul>
				<li>
                          <a href="#spr">genitive of separation</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1392</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1400</a>)
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
				</li>
				<li>genitive of distinction and comparison (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1401&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1401</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1404&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1404</a>)</li>
				<li>genitive of cause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1405&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1405</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1407&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1407</a>)</li>
				<li>genitive of purpose (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1408&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1408</a>)</li>
				<li>
                          <a href="#src">genitive of source</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1410&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1410</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1411&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1411</a>)</li>
				<li>none of the above</li>
				<li>I do not know</li>
				</ul>
			</li>
			<li>genitive of time and place (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1449</a>)
				<ul>
				<li>genitive of time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1444&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1444</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1447&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1447</a>)
				<ul>
					<li>simultaneous location</li>
					<li>sequential location</li>
					<li>sequential-durative</li>
					<li>temporal distance</li>
					<li>temporal extent</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
			</li>
				<li>genitive of place (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1448&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1448</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1449&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1449</a>)
				<ul>
					<li>location
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
					</li>
					<li>direction
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
					</li>
					<li>path
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
					</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
			</li>
				<li>none of the above</li>
				<li>I do not know</li>
				</ul>
			</li>
			<li>adpositional genitive
			<ul>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀπό</a>,
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐξ</a>) instrument or means</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀπό</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐξ</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπό</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">παρά</a>) agent</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀπό</a>,
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐξ</a>,
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyfth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπό</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) manner</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>) friendly association</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>) hostile association</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπό</a>) accompaniment</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπό</a>) accompanying circumstance</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1694&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρό</a>, 	
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1697&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπέρ</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) advantage</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) disadvantage</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) reference</li>
			
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀπό</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐξ</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>) conformity</li>
			
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
 	</li>
	<li>
                  <a href="#gnt_ind">independent</a>
		<ul>
			<li>exclamation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1407&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1407</a>)</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>

<h4>
                <a id="gnt_dpn">4.1.1.2.1 Dependent</a>
              </h4>
<p>
Dependent is the genitive which is syntactically dependent on another word in the sentence.
</p>

<h4>
                <a id="msr">4.1.1.2.2 Genitive of measure</a>
              </h4>
<p>
The genitive of measure specifies the measure of time, space, or degree.</p>

<h4>
                <a id="tpc">4.1.1.2.3 Genitive of topic</a>
              </h4>
<p>This kind of genitive specifies the topic with verbs of saying and thinking, which it depends on (note that I deviate from SG here, because this SR corresponds to the first kind of SG genitive of connection (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1380&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1380</a>) and what is treated in SG at <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1409&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1409</a>)</p>

<h4>
                <a id="cnn">4.1.1.2.4 Genitive of connection</a>
              </h4>
<p>The genitive of connection delimits the scope of the following clause, i.e., prototypically specifies with respect to what the following clause holds. It corresponds only to a part of SG genitive of connection (only SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1381&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1381</a>). Such kind of genitive is attached to the main verb of the clause it delimits. More generally, the genitive of connection is used here as an equivalent of the accusative/dative of respect, in that it can also specify in reference to/with respect to what the meaning of a verb (or verb phrase) holds.</p>

<h4>
                <a id="spr">4.1.1.2.5 Genitive of separation</a>
              </h4>
<p>
The SR of the genitive of separation ("separation") is usually labeled "source" in modern linguistic literature (which term is here and in traditional grammar used to indicate "origin"). Even though in SG the bare genitive of separation is mainly treatead not as a local function, it is in the present guidelines: more precisely, spatial separation corresponds to "separation &gt; concrete", while for verbs meaning "cease", "release", "remove", "lack", etc. (see SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1392&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1392</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1400&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1400</a>) select "separation &gt; figurative".</p>

<h4>
                <a id="src">4.1.1.2.6 Genitive of source</a>
              </h4>
<p>
The SR expressed by the genitive of source is sometimes labeled "origin" in linguistic literature. 
</p>

<h4>
                <a id="gnt_ind">4.1.1.2.7 Independent</a>
              </h4>
<p>
A genitive is independent if it does not dependent on any other word, and so is the linguistic head of a sentence.
</p>
</a> 

<a id="dtv">
<h4>4.1.1.3 Dative</h4>
<p>
There exist three main kinds of bare dative: the dative proper, the instrumental dative, and the locative dative. When the dative has the function of a PNOM (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1060</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1062&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1062</a>), the syntactic case selected should be the nominative. The following is the algorithm for the dative: 
</p>

<ul>
	<li>dependent (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1450&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1450</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1550&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1550</a>)
	<ul>
	<li>dative proper (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1457&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1457</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1498</a>)
	<ul>
		<li>dative as direct complement of verbs (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1460&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1460</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1468&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1468</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1471</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1473</a>)</li>
		<li>
                          <a href="#dat_ind_cmp">dative as indirect complement of verbs</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1469&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1469</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1470&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1470</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1471</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1473</a>)</li>
		<li>dative of interest (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1474&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1474</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1494</a>)
		<ul>
			<li>dative of the possessor (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1476&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1476</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1480&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1480</a>)</li>
			<li>dative of advantage (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1481</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1485</a>)</li>
			<li>dative of disadvantage (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1481&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1481</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1485&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1485</a>)</li>
			<li>dative of feeling (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1486&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1486</a>)</li>
			<li>dative with participle of inclination or aversion (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1487&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1487</a>)</li>
			<li>dative of agent (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1488&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1488</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1494&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1494</a>)</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>
		<li>dative of relation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1495</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1498</a>)
		<ul>
			<li>dative of relation proper (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1495&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1495</a>)</li>
			<li>dative of reference (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1496&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1496</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1497&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1497</a>)</li>
			<li>dative of the participle expressing time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1498&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1498</a>)</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
	</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
</li>
	<li>instrumental dative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1503&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1503</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1529&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1529</a>)
	<ul>
		<li>instrumental dative proper (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1506&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1506</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1520</a>)
		<ul>
		<li>dative of instrument or means (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1507&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1507</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1511&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1511</a>)</li>
		<li>dative of standard of judgment (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1512&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1512</a>)</li>
		<li>
                              <a href="#dtv_mnn">dative of manner</a>
                            </li>
		<li>dative of measure of difference (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1513</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1515&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1515</a>)</li>
		<li>dative of respect (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1516</a>)</li>
		<li>dative of cause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1517&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1517</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1520&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1520</a>)</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
	</li>
		<li>comitative dative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1521&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1521</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1528</a>)
		<ul>
			<li>dative of friendly association (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1523</a>)</li>
			<li>dative of hostile association (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1523&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1523</a>)</li>
			<li>dative of accompaniment (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1524&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1524</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1526&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1526</a>)</li>
			<li>
                              <a href="#dtv_acc_crc">dative of accompanying circumstance</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>)</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
	</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
</li>
	<li>locative dative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1530&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1530</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>)
	<ul>
		<li>dative of place (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1531&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1531</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1538&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1538</a>)
		<ul>
			<li>location
			<ul>
				<li>concrete</li>
				<li>figurative</li>
				<li>none of the above</li>
				<li>I do not know</li>
			</ul>
			</li>
			<li>direction
			<ul>
				<li>concrete</li>
				<li>figurative</li>
				<li>none of the above</li>
				<li>I do not know</li>
			</ul>
			</li>
			<li>
                              <a href="#dtv_pth">path</a>
			<ul>
				<li>concrete</li>
				<li>figurative</li>
				<li>none of the above</li>
				<li>I do not know</li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>dative of time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1539&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1539</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1543&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1543</a>)
		<ul>
			<li>simultaneous location</li>
			<li>sequential location</li>
			<li>sequential-durative</li>
			<li>temporal distance</li>
			<li>temporal extent</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
</li>
	<li>adpositional dative 
	<ul>
	<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>) purpose</li>
	<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1687&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐν</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1696&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">συν</a>) conformity</li>
	<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>) price and value</li>
	<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>) condition</li>
	<li>none of the above</li>
	<li>I do not know</li>
	</ul>
	</li>
	<li>none of the above</li>
	<li>I do not know</li>
	</ul>	
</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>

<h4>
                <a id="dat_ind_cmp">4.1.1.3.1 Dative as indirect complement of verbs</a>
              </h4>
<p>
The dative of indirect complement of verbs is associated with the SR of recipient or addressee (with verbs of saying). Note that if a verb can take a dative as direct or indirect complement of a verb (as described in  SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1471&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1471</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1473&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1473</a>), the annotator will label the dative  as a direct or an indirect complement according to the actual usage in a given sentence.
</p>

<h4>
                <a id="dtv_mnn">4.1.1.3.2 Manner</a>
              </h4>
<p>
The dative of manner is here meant to cover the SR of manner (according to my definition above), which SG associates with the "dative of accompanying circumstance" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>). In SG the dative of manner corresponds to a dative of measure of difference or dative of respect (see SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1513&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1513</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1516&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1516</a>), both of which I consider separate categories here.
</p>

<h4>
                <a id="dtv_acc_crc">4.1.1.3.3 Dative of accompanying circumstance</a>
              </h4>
<p>
The dative of accompanying circumstance is to be selected when the SR expressed by the SG "accompanying circumstance" (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1527&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1527</a>) is not of "manner", as here conceived.
</p>

<h4>
                <a id="dtv_pth">4.1.1.3.4 Path</a>
              </h4>
<p>
"Path" partly corresponds here to what is labeled (dative of) "space and time" in SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1528</a>). Similarly, the dative of time treated in SG as a kind of instrumental/comitative dative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1528&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1528</a>) has to be simply annotated with one of the categories under "dative of time".
</p>

</a> 

<a id="acc">
<h4>4.1.1.4 Accusative</h4>
<p>
There are five main kinds of bare accusative: 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">internal object (object effected)</a>, 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1590&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">external object (object affected)</a>, 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1580&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">accusative of extent</a>, 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">terminal accusative</a>, and 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">accusative of respect</a>. The so-called <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1606&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">adverbial accusative</a> is treated under the category 'adverb'. The accusative can express (1) one of 
these functions by itself or in conjunction with an adposition, which defines it more precisely, or (2) a new function in conjunction with an adposition (e.g., 'purpose'): in the former case, the function of the accusative is always annotated under one of the main functions, while in the latter case one of the adpositional functions should be used. Note that when the accusative is the subject or the predicate nominal in an infinitive clause, and hence is functionally equivalent to a nominative, the syntactic case selected should be the nominative. When the accusative has the function of OCOMP, the annotation process ends with the selection of the dependent feature (which parallels the annotation of the nominative as PNOM). The adverbial accusative should always be morphologically labeled as an adverb, so this kind of accusative is never annotated as a case. The algorithm for the accusative is the following:
</p>

<ul>
	<li>
                  <a href="#acc_dpn">dependent</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1551</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1598&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1598</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1600</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1635&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1635</a>)
		<ul>
			<li>
                      <a href="#acc_eff">internal object</a> (object effected) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1563</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1577&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1577</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1619&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1619</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1627&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1627</a>)</li>
			<li>
                      <a href="#acc_aff">external object</a> (object affected) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1590&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1590</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1598&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1598</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1613&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1613</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1633&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1633</a>)</li>
			<li>
                      <a href="#acc_ext">accusative of extent</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1580&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1580</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1587</a>)
				<ul>
				<li>accusative of space (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1581</a>)
				<ul>
					<li>location
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
					</li>
					<li>path
					<ul>
						<li>concrete</li>
						<li>figurative</li>
						<li>none of the above</li>
						<li>I do not know</li>
					</ul>
					</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
				</li>
				<li>accusative of time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1582</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1587</a>)
				<ul>
					<li>simultaneous location</li>
					<li>sequential location</li>
					<li>sequential-durative</li>
					<li>temporal distance</li>
					<li>temporal extent</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
				</li>
				<li>accusative of measure (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1581</a>)</li>	
				<li>none of the above</li>
				<li>I do not know</li>
				</ul>
				</li>
			<li>
                      <a href="#acc_trm">terminal accusative</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1588</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1589</a>)
			<ul>
				<li>concrete</li>
				<li>figurative</li>
				<li>none of the above</li>
				<li>I do not know</li>
			</ul>
			</li>
			<li>
                      <a href="#acc_rsp">accusative of respect</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1600</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1605</a>)</li>
			<li>adpositional accusative
			<ul>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1682&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀνά</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) manner</li>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>) instrument or means</li>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">παρά</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) cause</li>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>, 
				<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) purpose</li>
			<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) standard of judgment</li>
				<li>(with <a href="http://www.perseus.txufts.edu/hopper/text?doc=Smyth+grammar+1692&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">παρά</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>, <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>) comparison</li>
				<li> advantage</li>
				<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>, 
					<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a>) disadvantage</li>

				<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>, 
					<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a>) recipient or addressee</li>
				
				<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>, 
					<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) conformity</li>
					
				<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) friendly association</li>
				
				<li>(with <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>) hostile association</li>
					
		
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
	<li>
                  <a href="#acc_ipn">independent</a> (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1599</a>)
		<ul>
			<li>elliptical accusative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1599</a>)</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
</ul>


<h4>
                <a id="acc_dpn">4.1.1.4.1 Dependent</a>
              </h4>
<p>
Dependent is the accusative which is syntactically dependent on another word in the sentence.
</p>

<h4>
                <a id="acc_eff">4.1.1.4.2 Internal object (object effected)</a>
              </h4>
<p>
This accusative is considered to be already contained in the meaning of the verb. An object effected is a noun or one of its equivalents from a similar or the same root as that of the governing verb (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1563&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1563</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1577&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1577</a>).
</p>

<h4>
                <a id="acc_aff">4.1.1.4.3 External object (object affected)</a>
              </h4>
<p>
The accusative of the affected object is not contained in the verb, and so it is considered to be external. The semantic macro-role is Patient. SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1551&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1551</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1562&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1562</a>) 
provides some examples of verbs taking an external accusative. The accusative of result (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1578&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1578</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1579&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1579</a>) is not annotated, but is subsumed under the external or internal object on the basis of the relationship of the accusative with the verb.
</p>

<h4>
                <a id="acc_ext">4.1.1.4.4 Accusative of extent</a>
              </h4>
<p>
The accusative of extent expresses extension over 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1581&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">space</a> 
and 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1582&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">time</a>, or measure. The category measure should be used only when concerning space or amounts, not time. The accusative of extent can also be expressed by the accusative in conjunction with many 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1587&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">adpositions</a>.
</p>

<h4>
                <a id="acc_trm">4.1.1.4.5 Terminal accusative</a>
              </h4>
<p>
The terminal accusative expresses place direction (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1588</a>). While in poetry the simple terminal accusative is common, in prose such an accusative is regularly specified by an adposition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1589&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1589</a>).
</p>

<h4>
                <a id="acc_rsp">4.1.1.4.6 Accusative of respect</a>
              </h4>
<p>
The accusative of respect (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1600</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1605&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1605</a>)
expresses in relation to what the meaning of a verb or adjective is circumscribed. It can also be expressed by an accusative with an adposition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1603&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1603</a>) 
. 
</p>

<h4>
                <a id="acc_ipn">4.1.1.4.7 Independent</a>
              </h4>
<p>
Independent is the accusative which is the head of a sentence, i.e. the elliptical accusative (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1599&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1599</a>).
</p>


</a> 

<a id="prp">
<h4>4.1.1.5 Adpositions</h4>	
<p>
In the following sections, the annotation of the adpositional case is detailed. I follow the SG list for the meanings/functions of each proper adposition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1681&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1681</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1698</a>; note that some use of a certain preposition might not be covered in SG and hence here). Each function is followed by indication of how to annotate it. Note that "genitive of place/time", "dative of place/time", and "accusative of space/time" are here used as abbreviations to mean that the annotator has to choose, on the basis of the verb governing the case, the right SR that is algorithmically available for each of them (e.g., genitive of place &gt; location). If it is not possible to annotate a semantic funtion (i.e., it is not included in the list), "none of the above" has to be selected. The annotator should try to stick to the lemma translation proposed (if present). Since most prepositions conveying a local meaning can also be used in a figurative sense, the annotation algorithm always requires specification of whether a certain use of a preposition is concrete or figurative (this option is therefore available under any local meaning of a case).
</p>


<a>
<h4>4.1.1.5.1 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1681&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀμφί</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>cause ("about", "concerning"): genitive of topic</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>cause: dative of cause</li>
	<li>means: dative of instrument or means</li>
</ul>


<p>with accusative</p>
<ul>
	<li>local: accusative of space/terminal accusative</li>
	<li>temporal: accusative of time</li>
	<li>number: it depends on the function of the PP in the clause</li>
	<li>of occupation with an object (i.e., figuratively): accusative of space</li>
	<li>οἱ ἀμφί τινα (i.e., figuratively): accusative of space</li>
</ul>

</a>

<a>
<h4>4.1.1.5.2 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1682&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀνά</a>
                </h4>

<p>with dative</p>
<ul>
	<li>local: dative of place</li>
</ul>

<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>time: accusative of time</li>
	<li>distributively: none of the above</li>
	<li>manner: adpositional manner</li>
</ul>

</a>

<a>
<h4>4.1.1.5.3 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1683&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀντί</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>In other meanings ("instead of" or "in return for"): none of the above (for the lemma translation use, according to the meaning, "instead of" or "in return for")</li>
	<li>in entreaty: adpositional advantage</li>
</ul>
</a>

<a>
<h4>4.1.1.5.4 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1684&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἀπό</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of separation</li>
	<li>figuratively: genitive of separation</li>
	<li>temporal: genitive of time</li>
	<li>PPs such as ἀφ᾽ οὗ should be annotated as temporal adverbs</li>
	<li>origin/source: genitive of source</li>
	<li>author: adpositional agent</li>
	<li>cause: genitive of cause</li>
	<li>means/instrument: adpositional instrument or means</li>
	<li>manner: adpositional  manner</li>
	<li>conformity: adpositional conformity</li>
</ul>

</a>


<a>
<h4>4.1.1.5.5 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1685&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">διά</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>figuratively: genitive of place</li>
	<li>temporal: genitive of time</li>
	<li>intervals of space or time: genitive of place or time</li>
	<li>PPs such as διὰ πολλοῦ should be annotated as adverbs of measure</li>
	<li>means: adpositional instrument or means</li>
	<li>state or feeling: genitive of quality wherever possible, otherwise "none of the above"</li>
	<li>manner: adpositional manner</li>
</ul>


<p>with accusative</p>
<ul>
	<li>local: accusative of space</li>
	<li>cause: adpositional cause</li>
	<li>purpose: adpositional purpose</li>
	<li>agency/mediation/means: adpositional instrument or means</li>
</ul>
</a>


<a>
<h4>4.1.1.5.6 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1686&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">εἰς</a>, ἐς</h4>

<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>"against": adpositional disadvantage</li>
	<li>"in the presence of": adpositional recipient or addressee (with verbs of speaking)</li>
	<li>temporal: accusative of time</li>
	<li>measure and limit with numerals: it depends on the function of the PP in the clause</li>
	<li>goal, purpose, intention: adpositional purpose</li>
	<li>relation: accusative of respect</li>
	<li>manner: adpositional  manner</li>
	<li>PPs such as ἐς καιρόν should be annotated as adverbs of manner</li>
</ul>
</a>

<a>
<h4>4.1.1.5.7 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1687&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐν</a>
                </h4>

<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>of circumstance, occupation (i.e., figuratively): dative of place</li>
	<li>temporal: dative of time</li>
	<li>PPs such as ἐν ᾧ should be annotated as temporal adverbs</li>
	<li>instrument or means: dative of instrument or means</li>
	<li>cause: dative of cause</li>
	<li>manner: dative of manner</li>
	<li>conformity: adpositional conformity</li>
</ul>

</a>

<a>
<h4>4.1.1.5.8 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1688&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐξ</a>, ἐκ</h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of separation</li>
	<li>temporal: genitive of time</li>
	<li>immediate succession or transition: wherever possible, genitive of time</li>
	<li>origin: genitive of source</li>
	<li>agent: adpositional agent</li>
	<li>consequence: genitive of cause</li>
	<li>cause or ground of judgment: genitive of cause</li>
	<li>material: genitive of material or contents</li>
	<li>instrument and means: adpositional instrument or means</li>
	<li>conformity: adpositional conformity</li>
	<li>manner: adpositional manner</li>
	<li>PPs such as ἐκ τοῦ ἴσου should be annotated as adverbs of manner</li>
	<li>partitive: genitive of the divided whole</li>
</ul>

</a>

<a>
<h4>4.1.1.5.9 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1689&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ἐπί</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>temporal: genitive of time</li>
	<li>other relations (figuratively): genitive of place</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>temporal: dative of time</li>
	<li>succession, addition: dative of time</li>
	<li>supervision/dependence (i.e., figuratively): dative of place</li>
	<li>condition: adpositional condition</li>
	<li>reason, motive: dative of cause</li>
	<li>hostility: dative of disadvantage</li>
	<li>price: adpositional price and value</li>
</ul>	


<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>temporal: accusative of time</li>
	<li>quantity, measure: accusative of measure</li>
	<li>PPs such as ἐπὶ μικρόν should be annotated as adverbs of manner</li>
	<li>purpose: adpositional purpose</li>
	<li>hostility: adpositional disadvantage</li>
	<li>reference: accusative of respect</li>
</ul>
</a>

<a>
<h4>4.1.1.5.10 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1690&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">κατά</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of separation/genitive of place</li>
	<li>PPs such as κατ᾽ ἄκρας should be annotated as adverbs of manner</li>
	<li>temporal: genitive of time</li>
	<li>"against": adpositional disadvantage</li>
	<li>"with regard to": genitive of connection</li>
	<li>with verbs of swearing: none of the above</li>
</ul>


<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>temporal: accusative of time</li>
	<li>purpose: adpositional purpose</li>
	<li>conformity: adpositional conformity</li>
	<li>ground on which an act is based: adpositional cause</li>
	<li>comparison: adpositional comparison</li>
	<li>manner: adpositional manner</li>
	<li>distribution: none of the above</li>
	<li>approximate number: it depends on the function of the PP in the clause</li>
</ul>

</a>

<a>
<h4>4.1.1.5.11 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1691&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">μετά</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place/adpositional accompaniment</li>
	<li>accompanying circumstance: adpositional accompanying circurmstance/instrument or means</li>
	<li>joint efficient cause: genitive of cause</li>
	<li>conformity: adpositional conformity</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
</ul>	

<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>temporal, "after": accusative of time</li>
	<li>figuratively: accusative of space</li>
</ul>	

</a>

<a>
<h4>4.1.1.5.12 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1692&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">παρά</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of separation</li>
	<li>author, source: genitive of source</li>
	<li>with passives and intransitives: adpositional agent</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>possessor: dative of the possessor</li>
	<li>"of the superior in command" (i.e., figuratively): dative of place</li>
	<li>of the person judging: dative of reference</li>
</ul>	


<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>"contrary to": none of the above (lemma translation should be "contrary to")</li>
	<li>"in addition to": none of the above (lemma translation should be "in addition to")</li>
	<li>PPs such as παρ᾽ ὀλίγον ("of no account") should be annotated as adverbs of measure</li>
	<li>temporal: accusative of time</li>
	<li>cause/dependence: adpositional cause</li>
	<li>Adverbial PPs such as παρὰ πολύ or παρὰ μικρόν: πολύ and μικρόν are morphologically annotated as adverbs (adverb &gt; measure in SG tab)</li>
	<li>comparison: adpositional comparison</li>
</ul>	

</a>

<a>
<h4>4.1.1.5.13 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1693&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">περί</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>"about", "concerning": genitive of connection/genitive of topic</li>
	<li>superiority: genitive of distinction and comparison</li>
	<li>PPs such as περὶ παντός ("above all") should be annotated as adverbs of measure</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>external cause: dative of cause</li>
	<li>inner impulse: dative of cause</li>
</ul>	


<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>of person (i.e., figuratively): accusative of space</li>
	<li>indefinite statement of time and number: it depends on the function of the PP in the clause</li>
	<li>occupation (i.e., figuratively): accusative of space</li>
	<li>relation: accusative of respect</li>
</ul>	

</a>


<a>
<h4>4.1.1.5.14 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1694&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρό</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>temporal: genitive of time</li>
	<li>defence or care: adpositional advantage</li>
	<li>preference: none of the above (for the lemma translation use, according to the meaning, "in preference to" or "on behalf of")</li>
	<li>PPs such as πρὸ πολλοῦ ("highly") should be annotated as adverbs of measure</li>
</ul>

</a>


<a>
<h4>4.1.1.5.15 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1695&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">πρός</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>local: genitive of place</li>
	<li>descent: genitive of source</li>
	<li>characteristic: genitive of quality</li>
	<li>point of view of a person: adpositional reference</li>
	<li>agent: adpositional agent</li>
	<li>"to the advantage of": adpositional advantage</li>
	<li>in oaths and entreaties: none of the above</li>
</ul>


<p>with dative</p>
<ul>
	<li>local: dative of place</li>
	<li>occupation: none of the above</li>
	<li>"in addition to": none of the above (the lemma translation should be "in addition to")</li>
	<li>"in the presence of": dative as indirect complement of verbs</li>
</ul>	


<p>with accusative</p>
<ul>
	<li>local: terminal accusative</li>
	<li>temporal: accusative of time</li>
	<li>friendly or hostile relation: adpositional recipient or addressee (with verbs of speaking) or adpositional association</li>
	<li>relation in general: accusative of respect</li>
	<li>purpose: adpositional purpose</li>
	<li>conformity: adpositional conformity</li>
	<li>standard of judgment: adpositional standard of judgment</li>
	<li>comparison: adpositional comparison</li>
	<li>exchange: none of the above</li>
</ul>	

</a>

<a>
<h4>4.1.1.5.16 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1696&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">σύν</a>
                </h4>

<p>with dative</p>
<ul>
	<li>"with", "along with", "together with", "including": genitive of association/accompaniment/accompanying circumstance</li>
	<li>means and instrument: dative of means or instrument</li>
	<li>manner: dative of manner</li>
	<li>"in conformity with": adpositional conformity</li>
</ul>

</a>

<a>
<h4>4.1.1.5.17 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1697&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπέρ</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>"from over", "over", "above": genitive of separation/genitive of place</li>
	<li>"in defence of", "on behalf of": adpositional advantage</li>
	<li>"in place of", "in the name of": none of the above</li>
	<li>purpose: genitive of purpose</li>
	<li>"concerning", "about": genitive of topic / genitive of connection</li>
</ul>


<p>with accusative</p>
<ul>
	<li>local: accusative of space</li>
	<li>temporal: accusative of time</li>
	<li>measure: accusative of measure</li>
</ul>
	

</a>

<a>
<h4>4.1.1.5.18 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1698&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">ὑπό</a>
                </h4>

<p>with genitive</p>
<ul>
	<li>"out from under": genitive of separation/genitive of place</li>
	<li>direct agent/with passive nouns: adpositional agent</li>
	<li>external/internal cause: genitive of cause</li>
	<li>external accompaniment: adpositional accompanying circumstance/accompaniment</li>
	<li>manner: adpositional manner</li>
</ul>


<p>with dative</p>
<ul>
	<li>"under": dative of place</li>
	<li>agent: dative of agent</li>
	<li>cooperative cause: dative of cause</li>
	<li>subjection: none of the above</li>

</ul>	


<p>with accusative</p>
<ul>
	<li>local: terminal accusative/accusative of space</li>
	<li>temporal: accusative of time</li>
	<li>subjection: none of the above</li>
</ul>	

</a>

</a> 

</a>

<a id="adj_prp">
<h4>4.1.2 Adjective proper</h4>

<p>
If an adjective is also syntactically used as such, no further SG annotation is (currently) available.
</p>

<p>
The Prague annotation labels are usually ATR, PNOM, and OCOM.
</p>
</a>

<a id="sbs_adj">
<h4>4.1.3 Substantive adjective</h4>

<p>A substantive adjective is an adjective lemma in the <a href="http://www.perseus.tufts.edu/hopper/resolveform?redirect=true" target="_blank">LSJ dictionary</a> which is used as a noun (e.g., Ἀθαναῖος in Ἀθαναῖοι, 'the Athenians'). The SG algorithm allows annotation of its <a href="#snt_cas">syntax of the case</a> (whose categories are the same as those for the noun).</p>
	
<p>The Prague annotation label for the substantive adjective are the same as those for the <a href="#nou">noun</a>.</p>
</a>

<a id="vrb_adj">
<h4>4.1.4 Verbal adjective in τος/τεος</h4>

<p>A verbal adjective in τος/τεος derives from a verb root by the addition of the suffix τος/τεος (see SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2149&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2149</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2152&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2152</a> for more information). The present option is reserved when the verbal adjective has adjective function only (i.e., is not a substantive). No further SG annotation is available.</p>
	
<p>The verbal adjective in τος/τεος takes the same Prague annotation labels as the <a href="#adj">adjective</a> in adjective function.
</p>
</a>

<a id="vrb_adj_sbs">
<h4>4.1.5 Substantive verbal adjective in τος/τεος</h4>

<p>A substantive verbal adjective in τος/τεος is a verbal adjective used as a noun. The SG tagset allows annotation of its <a href="#snt_cas">syntax of the case</a>.</p> 

<p>The Prague annotation labels are the same as those for the <a href="#nou">noun</a>.
</p>
</a>

<a id="sbs_prn">
<h4>4.1.6 Substantive pronoun</h4>
<p>A substantive pronoun is a pronoun used as a noun. This option gives access to the annotation of the <a href="#snt_cas">syntax of the case</a> of the pronoun.</p>

<p>The Prague annotation labels are the same as those for the <a href="#nou">noun</a>.</p>  
</a>

<a id="adj_prn">
<h4>4.1.7 Adjective pronoun</h4>

<p>An adjective pronoun is a pronoun used as an adjective. As occurs with any other <a href="#adj">adjective</a> in adjective function, no further SG annotation is (currently) avaialble.</p>

<p>The Prague annotation labels are the same as those for the <a href="#adj">adjective</a> in adjective function.</p>
</a>

<a id="fnt_moo">
<h4>4.1.8 Syntax of the finite verb</h4>

<p>
On the basis of the mood selected at the morphological level, the annotation algorithm gives access to the the following options:
</p>

<ul>
<li>
                <a href="#ind_fnt_vrb">independent</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=1&amp;doc=4971" target="_blank">tree1</a>)
<ul>
	<li>statement (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2153&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2153</a>)</li>
	<li>assumption (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2154&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2154</a>)</li>
	<li>command (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2155&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2155</a>)</li>
	<li>wish (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2156&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2156</a>)</li>
	<li>question (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2157&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2157</a>)</li>
	<li>exclamation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2158&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2158</a>)</li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>
</li>
<li>
                <a href="#dpn_fnt_vrb">dependent</a>
	<ul>
		<li>
                    <a href="#sbs_cls">substantive clause</a>	
														(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=11&amp;doc=4971" target="_blank">tree1</a>) 
														(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=12&amp;doc=4971" target="_blank">tree2</a>)
		<ul>
			<li>statement (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2576&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2576</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2588</a>)
				<ul>
					<li>in indirect discourse</li>
					<li>not in indirect discourse</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
				</li>
			<li> will or desire (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2207&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2207</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2239&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2239</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>question (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2663&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2663</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2680&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2680</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>exclamation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2681&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2681</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2687</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>
                    <a href="#adj_cls">adjective clause</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=17&amp;doc=4971" target="_blank">tree1</a>)
		<ul>
		<li>adjective clause proper
		<ul>
				<li>ordinary relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2553&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2553</a>)
				<ul>
				<li>in indirect discourse</li>
				<li>not in indirect discourse</li>
				<li>none of the above</li>
				<li>I do not know</li>
				</ul>
				</li>
			<li>final relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2554&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2554</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>cause relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2555&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2555</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>consecutive relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2556&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2556</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2559&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2559</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>conditional relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2560&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2560</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2573&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2573</a>)
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect discourse</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>substantivized adjective clause
			<ul>
			<li>in indirect discourse
			<ul>
				<li>
                                <a href="#snt_cas">
                                  <span style="font-style:italic">syntax of the case</span>
                                </a>
                              </li>
			</ul>
			</li>
			<li>not in indirect discourse
			<ul>
				<li>
                                <a href="#snt_cas">
                                  <span style="font-style:italic">syntax of the case</span>
                                </a>
                              </li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>adverb clause (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=38&amp;doc=4971" target="_blank">tree1</a>)
		<ul>
		<li>final clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2193&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2193</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2206&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2206</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>	
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>causal clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2240&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2240</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2248&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2248</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>consecutive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2249&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2249</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2278&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2278</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>	
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>conditional clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2280&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2280</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2368&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2368</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>	
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>concessive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2369&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2369</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2382&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2382</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>	
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>temporal clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2383&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2383</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2461</a>)
		<ul>
			<li>simultaneous location
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect speech</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>sequential location
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect speech</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>sequential-durative
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect speech</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>temporal distance
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect speech</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>temporal extent
			<ul>
			<li>in indirect discourse</li>
			<li>not in indirect speech</li>
			<li>none of the above</li>
			<li>I do not know</li>
			</ul>
			</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>clause of comparison (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2462&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2462</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2487</a>)
		<ul>
		<li>in indirect discourse</li>
		<li>not in indirect speech</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
		</ul>
		</li>
	<li>none of the above</li>
	<li>I do not know</li>	
	</ul>
	</li>
		<li>none of the above</li>
		<li>I do not know</li>
</ul>

<a id="ind_fnt_vrb">
<h4>4.1.8.1 Independent</h4>

<p>A finite verb form is said to be independent if it is the head of a main clause (simple or coordinated). On the basis of its meaning, the clause can be annotated as a statement (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2153&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2153</a>), an assumption 
	(SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2154&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2154</a>), a command (SG 
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2155&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2155</a>), a wish (SG 
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2156&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2156</a>), a question (SG 
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2157&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2157</a>), or an exclamation (SG
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2158&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2158</a>).</p>

<p>The finite verb takes the Prague annotation label PRED, OBJ, ADV, or ATR.</p>
</a>

<a id="dpn_fnt_vrb">
<h4>4.1.8.2 Dependent</h4>
<p>A finite verb form is said to be dependent if it is the head of a subordinate clause.</p>
</a>

<a id="sbs_cls">
<h4>4.1.8.3 Substantive clause</h4>
<p>A substantive clause is equivalent to a noun with respect to its governing verb (and indeed it could often be replaced with a pronoun such as τόδε). On the basis of its meaning, the clause can be annotated as a statement (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2576&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2576</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2588&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2588</a>), will or desire (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2207&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2207</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2239&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2239</a>), a question (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2663&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2663</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2680&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2680</a>), or an exclamation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2681&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2681</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2687&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2687</a>).</p> 

<p>The head verb of the substantive clause takes the Prague annotation labels SBJ, OBJ, or APOS.</p>
</a>

<a id="adj_cls">
<h4>4.1.8.4 Adjective clause</h4>
<p>
The Adjective clause is a relative clause. Just like an adjective, the relative clause can have the function of an adjective (adjective clause proper) or be substantivized (i.e., when the antecedent is not expressed). There two ways to annotate substantivized relative clauses. The easiest way is to not add an elliptical node for the omitted antecedent. The second option is to add the elliptical node and so treat the relative clause as an adjective clause proper (and so any relative clause is treated as an adjective clause proper, independentely of whether or not the antecedent of the relative pronoun is expressed). The first option is the default one, while the second one has to be declared. The adjective clause proper can be an ordinary relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2553&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2553</a>), a final relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2554&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2554</a>), a cause relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2555&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2555</a>), a consecutive relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2556&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2556</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2559&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2559</a>), or a conditional relative clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2560&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2560</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2573&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2573</a>), on the basis of its meaning.</p>

<p>The easiest example of relative clause is the one with the antecedent expressed (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=46&amp;doc=4971" target="_blank">tree1</a>). When the antecedent is not expressed, and so the adjective clause it taken to be substantivized, the verb of the relative clause is attached to the governor verb and receives the SG annotation that an antecedent would have received if it were expressed; the relative pronoun is attached to the verb of the relative clause and receives the SG annotation that is required by the governor verb, no matter what the morphology of the relative pronoun is (i.e., the syntactic case can be different from the morphological one of the relative pronoun/adverb): see  <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=20&amp;doc=4971" target="_blank">tree1</a>, <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=49&amp;doc=4971" target="_blank">tree2</a>. The possibility to choose a different syntactic case for each word allows also the annotation of examples of incorporation of the ancedent (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=51&amp;doc=4971" target="_blank">tree1</a>). When an adjective clause proper has adverbial function, it has to be appended to its superordinate verb: <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=47&amp;doc=4971">tree1</a>.</p>

<p>
The Prague annotation labels for the head verb of an adjective clause are the same as those for the <a href="#adj">adjective</a> or <a href="#noun">noun</a> (for the substantivized adjective clause).
</p>
</a>

<a id="adv_cls">
<h4>4.1.8.5 Adverb clause</h4>
<p>
An adverb clause is a clause functioning as an adverb with respect to its governing verb. On the basis of its meaning it is possible to specify if the adverb clause is a final clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2193&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2193</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2206&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2206</a>), a causal clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2240&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2240</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2248&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2248</a>), a consecutive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2249&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2249</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2278&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2278</a>), a conditional clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2280&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2280</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2368&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2368</a>), a concessive clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2369&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2369</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2382&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2382</a>), a temporal clause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2383&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2383</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2461</a>), or a clause of comparison (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2462&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2462</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2487&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2487</a>).
</p>

<p>The verb head of an adverb clause takes the Prague annotation label ADV.</p>
</a>

</a>

<a id="adj_prt">
<h4>4.1.9 Adjective participle</h4>

<p>The participle is a verbal adjective (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2039&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2039</a>). Like any other <a href="#adj">adjective</a>, it can have adjective function or be <a href="#sbs_prt">substantivized</a>. In the former case, the SG tagset allows annotation of the following categories:</p>

<ul>
	<li>
                <a href="#att_prt">attributive participle</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=42&amp;doc=4971" target="_blank">tree1</a>) (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=44&amp;doc=4971" target="_blank">tree2</a>)</li>
	<li>
                <a href="#crc_prt">circumstantial participle</a>   (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=43&amp;doc=4971" target="_blank">tree1</a>)
															(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=3&amp;doc=4971" target="_blank">tree2</a>)
	<ul>
		<li>time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2061&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2061</a>)
		<ul>
			<li>simultaneous location</li>
			<li>sequential location</li>
			<li>sequential-durative</li>
			<li>temporal distance</li>
			<li>temporal extent</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>manner (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2062&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2062</a>)</li>
		<li>means (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2063&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2063</a>)</li>
		<li>cause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2064&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2064</a>)</li>
		<li>purpose (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2065&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2065</a>)</li>
		<li>concession (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2066&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2066</a>)</li>
		<li>condition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2067&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2067</a>)</li>
		<li>any attendant circumstance (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2068&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2068</a>)</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>
                <a href="#spp_prt">supplementary participle</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=21&amp;doc=4971" target="_blank">tree1</a>)
														(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=5&amp;doc=4971" target="_blank">tree2</a>)
														(<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&amp;doc=4971" target="_blank">tree3</a>)
														
	<ul>
		<li>in indirect discourse</li>
		<li>not in indirect discourse</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>
                <a href="#prh_prt">periphrastic participle</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=45&amp;doc=4971" target="_blank">tree1</a>)</li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>

<a id="att_prt">
<h4>4.1.9.1 Attributive participle</h4> 

<p>The attributive participle is the participle having a function similar to that of an attributive adjective (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2049&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2049</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2053&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2053</a>), and so is annotated as depending on the noun (or one of its equivalents) which it agrees with. It usually has attributive position (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1166&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1166</a>), but can also be in predicate position (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2053&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2053</a>):</p>

<blockquote>
<p>ἐπὶ Κόδρου βασιλεύοντος</p> 
<p>'in the reign of Codrus', Lyc. 84</p>
<p>Κόδρου (genitive &gt; dependent &gt; genitive of time and place &gt; time &gt; sequential durative)</p>
<p>βασιλεύοντος (participle &gt; attributive)</p>
</blockquote>

<p>The temporal function is annotated as part of the genitive noun, while the participle is annotated as attributive. Another example of attributive participle not being in attributive position is:</p>
	
<blockquote>
<p>ἐπὶ τὸν Χάλον ποταμόν, ὄντα τὸ εὖρος πλέθρου</p> 
<p>'to the river Chalus, which is a plethrum in width', X. A. 1.4.9</p>
<p>ὄντα (participle &gt; attributive &gt; proper)</p>
</blockquote>

<p>There are participles that can be taken to be attributive with the force of an improper relative clause  (i.e., a relative clause having the force of a an adverb clause, such as a final clause):</p>

<blockquote>
<p>προπέμψαντες κήρυκα πόλεμον προεροῦντα</p> 
<p>'having sent a herald in advance to proclaim war', T. 1.29</p>
</blockquote>

<p>The participle προεροῦντα can be interpreted as translating a final relative clause. Participles such as these are traditionally considered to be circumstantial and so syntactically dependent on their superordinate verbs, as occurs with circumstantial participles when they are in the nominative case.</p>

<p>All the participles so far discussed take the Prague annotation label ATR when they are attached to a noun or the function ADV if they are equivalent to an adverb clause and are attached to their superordinate verb.</p>
</a>

<a id="crc_prt">
<h4>4.1.9.2 Circumstantial participle</h4>

<p>The circumstantial participle, according to SG
(<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2054&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2054</a>),  specifies the circumstance under which the action of the superordinate verb takes place. The annotation algorithm allows us to specify the force of the circumstantial participle:</p>

<ul>
		<li>time (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2061&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2061</a>)
		<ul>
			<li>simultaneous location</li>
			<li>sequential location</li>
			<li>sequential-durative</li>
			<li>temporal distance</li>
			<li>temporal extent</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>manner (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2062&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2062</a>)</li>
		<li>means (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2063&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2063</a>)</li>
		<li>cause (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2064&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2064</a>)</li>
		<li>purpose (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2065&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2065</a>)</li>
		<li>concession (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2066&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2066</a>)</li>
		<li>condition (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2067&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2067</a>)</li>
		<li>any attendant circumstance (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2068&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2068</a>)</li>
</ul>

<p>
It is to be noted that the force of a participle heavily depends on the context, and so ambiguities may sometimes arise (SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2069&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2069</a>) well acknowledges this as well): the annotator should choose the most likely label according to his/her interpretation of the participle. Notwithstanding, the meaning of the circumstantial participle is very often signalled clearly by adverbs in the superordinate clause, such as 
ἔπειτα 'thereupon', τότε 'then', ἤδη 'already', etc. (a list can be found in SG 
(<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2079&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2079</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2087&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2087</a>); note that ἅτε, οἷα, οἷον, ὡς, and ὥσπερ depend on the participles - and not on the superordinate verb of the participle - as AuxZ). 
The label "any attendand circumstance" should be reserved for those participles whose meaning can be rendered in English with a preposition (“ἔχων στρατιὰν ἀφικνεῖται” he arrives with an army” <a href="http://www.perseus.tufts.edu/hopper/text?doc=Thuc.%204.30&amp;lang=original" target="_blank">T. 4.30</a>) or with a coordinate clause (rather than a subordinate clause).</p> 

<p>These kinds of circumstantial participles are labeled as ADV in the Prague annotation.</p>

<p>The genitive absolute and the accusative absolute (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2070&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2070</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2078&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2078</a>) are considered to be a kind of circumstantial participle, so there is no difference in their annotation, except that the genitive or the accusative nouns functioning as their subjects are attached to the participle (and receive the Prague annotation label "SBJ") and not to the superordinate verb of the participle.</p>
</a>

<a id="spp_prt">
<h4>4.1.9.3 Supplementary participle</h4>

The supplementary participle is an argument of the verb. Following SG, two kinds of supplementary participles are distinguished: the one not in indirect discourse (SG 
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2094</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2105</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2123</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>) and the one in indirect discourse (SG
<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2106&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2106</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2115</a>; <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2120&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2120</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>). The difference lies in the nature of the governing verb, which can allow a participle to be equivalent to a dependent statement according to the principles of indirect discourse (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2589&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2589</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2635&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2635</a>):

<blockquote>
<p>οὐ γὰρ ᾔδεσαν αὐτὸν τεθνηκότα (= τέθνηκε)</p> 
<p>'for they did not know that he was dead', X. A. 1.10.16</p>
<p>τεθνηκότα (participle &gt; supplementary &gt; indirect discourse)</p>
</blockquote>

<p>In the example the participle depends on ᾔδεσαν, and αὐτὸν depends on the participle, being interpreted as its subject. Such participles receive the function OBJ, as in the example, or PNOM, if a personal construction is present (as with δῆλός εἰμι, SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2107&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2107</a>); when building the tree, the participle is attached to the adjective). When the supplementary participle is not in indirect discourse, there is no dependent statement according to the principles of indirect discourse:</p>

<blockquote>
<p>διάγουσι μανθάνοντες</p> 
<p>'they are continually (they spend their time in) learning', X. C. 1.2.6</p>
<p>τεθνηκότα (participle &gt; supplementary &gt; not in indirect discourse)</p>
</blockquote>

<p> Such participles are attached to the governing verb and their label is PNOM. There may be cases where a supplementary participle agrees with a dative, as in:</p>

<blockquote>
<p>εἰ (αὐτοῖς) πολεμοῦσιν ἄμεινον ἔσται</p>
<p>'(they asked the god) whether it would be better for them to make war', T. 1.118.</p>
</blockquote>
	
<p>The participle πολεμοῦσιν depends on ἔσται and receives the label SBJ: the accordance with the implied dative of advantage can be explained as a case of attraction (SG 
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1060&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1060</a>). A list of verbs allowing a supplementary participle not in indirect discourse can be found in (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2094&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2094</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2105&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2105</a>). Verbs of perceiving and finding (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2110&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2110</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2115&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2115</a>) allow participles both in indirect discourse and not in indirect discourse: when the participle is not in indirect discourse, it takes the function OCOMP (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=23&amp;doc=4971" target="_blank">tree1</a>).
	Some verbs (SG 
 <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2123&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2123</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2145&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2145</a>) allow either the participle or the infinitive in indirect discourse or not in indirect discourse.</p>
</a>

<a id="prh_prt">
<h4> 4.1.9.4 Periphrastic participle</h4>

<p>In SG, this participle is considered to be a kind of supplementary participle (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2091&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2091</a>; note that if a participle is substantivized it cannot be taken to be periphrastic). However it seems to be useful to categorize it separately. See SG (<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+599&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">599</a>, 
		<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+600&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">600</a>, 
			<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1961&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1961</a>-<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1965&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1965</a>) for plenty of examples.</p> 

<p>The syntactic label for the periphrastic participle is PNOM.</p>

</a>
</a>

<a id="sbs_prt">
<h4>4.1.10 Substantive participle</h4>

<p>A substantive participle is a participle which is used as a noun. The SG algorithm allows annotation of its <a href="#snt_cas">syntax of the case</a> (whose categories are the same as those for the noun).</p> 

<p>The Prague annotation labels for the substantive participle are the same as those for the <a href="#nou">noun</a>.</p>
</a>

<a id="inf">
<h4>4.1.11 Syntax of the infinitive</h4>

<p>The infinitive is a <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1966&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">verbal noun</a>. Its syntactic behavior is due to its partly nominal and partly verbal nature. Although such an "in-between" nature is always present in the infinitive, the articular function and the (for a lack of a better term) verbal function of the infinitive are here distinguished for the purposes of the classification. The algorithm for the infinitive is the following:</p>

<ul>
<li>
                <a href="#dpn_inf">dependent</a>
<ul>
<li>
                    <a href="#art_inf">articular</a>
<ul>
<li>nominative</li>
<li>genitive</li>
<li>dative</li>
<li>accusative</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>
                    <a href="#vrl_inf">verbal</a>
<ul>
<li>as nominative (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=39&amp;doc=4971" target="_blank">tree1</a>)
<ul>
<li>in indirect discourse
<ul>
	<li>statement</li>
	<li>assumption</li>
	<li>command</li>
	<li>wish</li>
	<li>question</li>
	<li>exclamation</li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>
                          </li>
<li>not in indirect discourse
</li>	
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>as accusative (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=4&amp;doc=4971" target="_blank">tree1</a>)
<ul>
<li>in indirect discourse
<ul>
	<li>statement</li>
	<li>assumption </li>
	<li>command </li>
	<li>wish</li>
	<li>question</li>
	<li>exclamation</li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>


</li>
<li>not in indirect discourse</li>	
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>uncertain case
<ul>
<li>
                            <a href="#vrl_inf">infinitive of purpose (uncertain case)</a> (<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=41&amp;doc=4971" target="_blank">tree1</a>)  </li>
<li>
                            <a href="#vrl_inf">infinitive of result (uncertain case)</a>
                          </li>
<li>
                            <a href="#vrl_inf">temporal infinitive (uncertain case)</a>
				<ul>
					<li>simultaneous location</li>
					<li>sequential location</li>
					<li>sequential-durative</li>
					<li>temporal distance</li>
					<li>temporal extent</li>
					<li>none of the above</li>
					<li>I do not know</li>
				</ul>
</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>
                <a href="#idp_inf">independent</a>
<ul>
<li>command (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2013&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2013</a>)</li>
<li>wish (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2014&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2014</a>)</li>
<li>exclamation (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2015&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2015</a>)</li>
<li>absolute infinitive (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2012&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2012</a>)</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>
</li>
<li>none of the above</li>
<li>I do not know</li>
</ul>


<a id="dpn_inf">
<h4>4.1.11.1 Dependent</h4>
<p>An infinitive is said to be "dependent" if it is (linguistically) governed by another word in the sentence.</p>
</a>

<a id="idp_inf">
<h4>4.1.11.2 Independent</h4>
<p>An infinitive is said to be "independent" if it is the head of a sentence (or linguistically independent, as the absolute infinitive is).</p>
</a>

<a id="art_inf">
<h4>4.1.11.3 Articular infinitive</h4>

<p>The articular infinitive is the infinitive preceded by the definite article:</p>

<ul>
<li>nominative (articular) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2031&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2031</a>)</li>
<li>genitive (articular) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2032&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2032</a>)</li>
<li>dative (articular) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2033&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2033</a>)</li>
<li>accusative (articular) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2034&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2034</a>)</li>
</ul>

<p>The whole spectrum of possibilities available to annotate the noun is algorithmically made available for the articular infinitive, even though only some them 
	are likely to be found in practice. On the basis of the case selected, the annotator has access to the <a href="#snt_cas">syntax of the case</a>.</p>
<p>The Prague annotation labels are the same as those for the <a href="#nou">noun</a>.</p>

</a>

<a id="vrl_inf">
<h4>4.1.11.4 Verbal infinitive</h4>

<p>When the infinitive is not articular, it is labeled as "verbal". The following possibilities are available:</p>

<ul>
	<li>as nominative
	<ul>
	<li>in indirect discourse
	<ul>
		<li>statement</li>
		<li>assumption </li>
		<li>command </li>
		<li>wish</li>
		<li>question</li>
		<li>exclamation</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>not in indirect discourse</li>
	<li>none of the above</li>
	<li>I do not know</li>
	</ul>
	</li>
	<li>as accusative
	<ul>
	<li>in indirect discourse
	<ul>
		<li>statement</li>
		<li>assumption </li>
		<li>command </li>
		<li>wish</li>
		<li>question</li>
		<li>exclamation</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>not in indirect discourse</li>
	<li>none of the above</li>
	<li>I do not know</li>
	</ul>
	</li>
	<li>uncertain case
	<ul>
	<li>infinitive of purpose (uncertain case) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2008</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2010&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2010</a>)</li>
	<li>infinitive of result (uncertain case) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2011</a>)</li>
	<li>temporal infinitive (uncertain case) (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2453&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2453</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2461</a>)
	<ul>
		<li>simultaneous location</li>
		<li>sequential location</li>
		<li>sequential-durative</li>
		<li>temporal distance</li>
		<li>temporal extent</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>none of the above</li>
	<li>I do not know</li>
	</ul>
	</li>
<li>none of the above</li>
<li>I do not know</li>	
</ul>
	
	
<p>The infinitive, when depending on a verb, bears a syntactic nominative or accusative case on the basis of whether it is the subject or the object of a verb, and can be in indirect discourse (SG
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2016&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2016</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2024&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2024</a>) or not in indirect discourse (SG 
	<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+1989&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">1989</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2007&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2007</a>). The infinitive can also be used to express purpose (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2008&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2008</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2010&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2010</a>), result (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2011&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2011</a>), or temporal clauses (SG <a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2453&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2453</a>–<a href="http://www.perseus.tufts.edu/hopper/text?doc=Smyth+grammar+2461&amp;fromdoc=Perseus%3Atext%3A1999.04.0007" target="_blank">2461</a>).
</p>

<p>The Prague annotation labels are the same as those for the <a href="#nou">noun</a>. When the infinitive is of purpose, result, or temporal, the label is <a href="#adv_fnc">ADV</a>.</p>

</a>

<a id="adv_snt">
<h4>4.1.12 Syntax of the adverb</h4>	
<p>The SG tagset allows the annotation of the following SRs for the adverb:</p>
<ul>
<li>time
<ul>
	<li>simultaneous location</li>
		<li>sequential location</li>
		<li>sequential-durative</li>
		<li>temporal distance</li>
		<li>temporal extent</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>place
	<ul>
		<li>location
		<ul>
			<li>concrete</li>
			<li>figurative</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>direction
		<ul>
			<li>concrete</li>
			<li>figurative</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>path
		<ul>
			<li>concrete</li>
			<li>figurative</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>separation
		<ul>
			<li>concrete</li>
			<li>figurative</li>
			<li>none of the above</li>
			<li>I do not know</li>
		</ul>
		</li>
		<li>none of the above</li>
		<li>I do not know</li>
	</ul>
	</li>
	<li>source</li>
	<li>cause</li>
	<li>result</li>
	<li>manner</li>
	<li>measure (/degree)</li>
	<li>instrument or means</li>
	<li>purpose</li>
	<li>concessive</li>
	<li>negation</li>
	<li>
                  <a href="#part">particle</a>
                </li>
	<li>none of the above</li>
	<li>I do not know</li>
</ul>
	
	
<p>The tagset distinguishes many kinds of time and place adverbs because the annotation aims to preserve the distinctions that are morphologically signaled by the case when the SR is expressed by a noun.</p>

<p>The Prague annotation labels are <a href="#obj">OBJ</a>, <a href="#adv_fnc">ADV</a> (on the basis of whether or not the adverb is an argument), <a href="#auxz">AuxZ</a>, or <a href="#auxy">AuxY</a>.</p>

</a>

<a id="part">
<h4>4.1.12.1 Particle</h4>
<p>Particle are here defined as those adverbs, typically sentence adverbs, which in AG are usually in pospositive position. The definition in SG, as well as in many traditional grammars, is broader, in that it also includes conjunctions: these, however, have to be always annotated as conjunctions. As is known, the meaning and function of AG particles is very complex to capture. In the following guidelines there is no attempt to provide detailed criteria to annotate particles. The annotator is only required to be able to identify those particle (in the traditional large definition of terms) which are conjunctions, such as:</p> 

<ul>
                  <li>ἀλλά</li>
	<li>ἀτάρ</li>
	<li>δέ <a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=51&amp;doc=4971" target="_blank">tree1</a>
                  </li>
	<li>εἴτε</li>
	<li>ἤ</li>
	<li>ἠδέ</li>
	<li>καί</li>
	<li>καίτοι</li>
	<li>οὐδέ</li>
	<li>οὔτε</li>
	<li>μηδέ</li>
	<li>μήτε</li>
	<li>τε</li>
</ul>
	
	
<p>Some of these particples can of course be adverbs, and so should accordingly be annotated as such. When a particle is a conjunction, it governs other nodes: 

<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=24&amp;doc=4971" target="_blank">tree1</a>,
<a href="http://sosol.perseids.org/tools/arethusa/app/#/perseids?chunk=26&amp;doc=4971" target="_blank">tree2</a>.

Any other particle which is not one of the above conjunctions is attached to the verb of the main clause and receives the AuxY label, if the particle is a sentence adverb, or is attached to the word which it modifies and receives the label AuxZ. In the current version of the treebank it is left to the annotator to decide which of these two options is the right one for each of the non-conjuntion particles.

</p>
</a>
 
		
</a>

</a>

</a>
</a>
</a>
</body>
