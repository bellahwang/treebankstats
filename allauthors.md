# Tag Explanations
In the table below, I break down each of the tags used in the 'allauthors.csv' file containing compiled and standardized data from the Pedalion trees, gAGDT trees, Gorman trees, and Proiel trees. Each row in 'allauthors.csv' corresponds to an annotated word with its' respective identifying information - more details about the information can be found in [this table](#tags-in-file).

My dataset consisted of all Pedalion trees (EXCLUDING 'example-sentences.xml' and some portions of 'chilia-sentences.xml', and INCLUDING 'papyri.xml'), all gAGDT trees, all Gorman trees, and some Proiel trees (INCLUDING 'greek-nt.xml', 'chron.xml', and 'hdt.xml'). 

I 

Although 'papyri.xml' consists of scraps of papyri manuscripts, many of which have no traceable authors, I included it in the final csv file. As a result, all words from the 'papyri.xml' file do not contain author related information. 

To avoid repeated data, I have excluded Book 1 of Herodotus in 'hdt.xml', because Vanessa Gorman already has annotated trees for Book 1 of Herodotus. However, echoing Dr. Greg Crane, it would be an interesting future project to compare and contrast similarities and differences in the Proiel analysis and Gorman analysis of Book 1 of Herodotus. 



I've standardized differences across the Pedalion trees, gAGDT trees, Gorman trees, and Proiel trees. Namely:
* correcting POStags (Part of Speech Tags) of incorrect lengths 
    * e.g. 'c' is replaced by 'c--------'
* assigning standardized author information based on [this dict](#author-dict)
    * e.g. 
* adding additional standardized author and work information
    * e.g. including information from [this dict](#author-dict) to each word
* 

Some things I have NOT standardized include:
* Proiel POS (part of speech) tagging
    * Proiel encodes parts of speech in the form of '[POS-tag-here]-' instead of '[POS-tag-here]'. For example, when encoding a verb, it will be listed as 'V-' instead of 'v'.

## Tags in file
| Tag         				| Description | Notes		|
| ----------- 				| ----------- | -----------	|
| Author      				| Name of Author | corresponds with Author Name in [this dict](#author-dict) containing info about authors, timelines, and genres 
| AuthorTLG   				| Standardized TLG code identifying each author | corresponds with TLG Identifier in [this dict](#author-dict)
| WorkTLG  	  				| Standardized TLG code identifying each work | not every work has a TLG identifier
| Timeline    				| Rough century date for each author to display in timeline settings |
| StartDate   				| Start of century for author's work | date markers are not standardized yet
| EndDate  	  				| End of century for author's work | date markers are not standardized yet
| Poetry/Prose 				| Labels author's work as poetry or prose |
| Genre  	  				| Labels author's work as specific genre |
| sentID  	  				| Unique ID for each sentence in work |
| docID  	  				| Unique ID for |
| subdoc  	  				| Identifier | Different uses across treebanks
| AuthorName  				| 'Author' tag listing name of author | only present in Pedalion trees |
| wordID  	  				| Unique ID for each word relative to each sentence | Not unique across all sentences, except for in Pedalion 
| head  	  				| Text        |
| form  	  				| Text        |
| lemma  	  				| Text        |
| relation    				| Text        |
| ref  	      				| Text        |
| presentation_after  	  	| Text        |
| insertionID  	  			| Text        |
| artificial  	  			| Text        |
| gloss  	  				| Text        |
| sem  	  					| Text        |
| postag  	  				|  | separated into different subcategories to make searching more smooth (Listed below) |
| pos  	  					| part of speech |
| person  	  				| subcategory of postag: person | 1st, 2nd, or 3rd
| number  	  				| subcategory of postag: number | singular, dual, plural
| tense  	  				| subcategory of postag: tense | 
| mood  	  				| subcategory of postag: mood  |
| voice  	  				| subcategory of postag: voice |
| gender  	  				| subcategory of postag: gender |
| case  	  				| subcategory of postag: case |
| degree  	 				| subcategory of postag: degree |
| strength  	  			| subcategory of postag: strength |
| inflection  	  			| subcategory of postag: inflection |

# Author Dict

Created by Dr. Greg Crane in 'Treebank.ipynb'
| TLG Identifier | Author Name | Timeline | StartDate | EndDate | Poetry/Prose | Genre
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| tlg0011 | Sophocles | -5 | -497 | -406 | poetry | drama
| tlg1220 | Batrachomyomachia | -1 | -100 | -1 | poetry | hexameter
| tlg0013 | Homeric Hymns | -6 | -650 | -450 | poetry | hexameter
| tlg0020 | Hesiod | -8 | -750 | -650 | poetry | hexameter
| tlg0026 | Aeschines | -4 | -389 | -314 | prose | orator
| tlg0058 | Aeneas Tacticus | 4 | 301 | 400 | prose | misc
| tlg0096 | Aesop | -6 | -620 | -564 | prose | misc
| tlg0085 | Aeschylus | -5 | -525c | -455c | poetry | drama
| tlg0028 | Antiphon | -5 | -490 | -411 | prose | orator
| tlg0551 | Appian | 2 | 95 | 165 | prose | history
| tlg0086 | Aristotle | -4 | -384 | -322 | prose | philosophy
| tlg0019 | Aristophanes | -5 | -446 | -386 | poetry | drama
| tlg0008 | Athenaeus | 3 | 170 | 223 | prose | misc
| tlg0554 | Chariton | 2 | 101 | 200 | prose | misc
| tlg0041 | Chionis Epistulae | 1 | 1 | 200 | prose | misc
| tlg0627 | Corpus Hippocraticum | -5 | -450 | -350 | prose | misc
| tlg0014 | Demosthenes | -4 | -384 | -322 | prose | orator
| tlg0060 | Diodorus Siculus | -1 | -90c | -30c | prose | history
| tlg0081 | Dionysius of Halicarnassus | -1 | -60c | -7c | prose | history
| tlg0557 | Epictetus | 2 | 50 | 135 | prose | philosopy
| tlg0537 | Epicurus | -3 | -341 | -270 | prose | philosophy
| tlg0343 | Ezechiel the Tragic Poet | -2 | -200 | -101 | poetry | drama
| tlg0006 | Euripides | -5 | -480c | -406c | poetry | drama
| tlg0016 | Herodotus | -5 | -484c | -425c | prose | history
| tlg0559 | Heron of Alexandria | 1 | 10 | 70 | prose | misc
| tlg0010 | Isocrates | -4 | -436 | -338 | prose | orator
| tlg0526 | Josephus | 1 | 37 | 100c | prose | history
| tlg2003 | Julian the Apostate | 4 | 331 | 363 | prose | misc
| tlg0561 | Longus | 2 | 101 | 200 | prose | misc
| tlg0061 | Pseudo-Lucian | 3 | 201 | 400 | prose | misc
| tlg0062 | Lucian | 2 | 125 | 180 | prose | misc
| tlg0540 | Lysias | -4 | -445c | -380c | prose | orator
| tlg0541 | Menander | -3 | -342 | -291 | poetry | drama
| tlg0255 | Mimnermus | -7 | -650 | -600 | poetry | lyreleg
| tlgX208 | Paeanius | 4 | 301 | 400 | prose | misc
| tlg0585 | Phlegon | 2 | 151 | 200 | prose | misc
| tlg0059 | Plato | -4 | -428c | -347c | prose | philosophy
| tlg0007 | Plutarch | 2 | 46 | 119 | prose | history
| tlg0543 | Polybius | -2 | -200 | -118 | prose | history
| tlg4029 | Procopius | 6 | 500 | 565 | prose | history
| tlg0009 | Sappho | -7 | -630 | -570 | poetry | lyreleg
| tlg0260 | Semonides | -7 | -700 | -601 | poetry | lyreleg
| tlg0527 | Septuagint | -2 | -250 | -100 | prose | bible
| tlg0544 | Sextus Empiricus | 3 | 150 | 250 | prose | philosophy
| tlg0032 | Xenophon | -4 | -430c | -354 | prose | history
| tlg0005 | Theocritus | -3 | -300 | -255 | poetry | hexameter
| tlg0003 | Thucydides | -5 | -460c | -400c | prose | history
| tlg0093 | Theophrastus | -4 | -371 | -287 | prose | philosophy
| tlg0012 | Homer | -8 | -775c | -700c | poetry | hexameter
| tlg0031 | New Testament | 1 | 80 | 100 | prose | bible
| tlg3143 | Georgius Sphrantzes | 16 | 1480 | 1550 | prose | history

# POS Tag Dicts
## Tense Dict
| Identifier (ID) | Meaning |
| ----------- | ----------- |
| p | present |
| f | future |
| i | imperfect |
| a | aorist |
| r | perfect |
| l | pluperfect |
| t | future perfect|

## Voices Dict
| Identifier (ID) | Meaning |
| ----------- | ----------- |
| a | active | 
| m | middle |
| p | passive |
| i | imperfect |
| e | middle-passive |

## Mood Dict
| Identifier (ID) | Meaning |
| ----------- | ----------- |
| i | indicative |
| s | subjunctive |
| o | optative |
| m | imperative |
| p | participle |
| n | infinitive |
