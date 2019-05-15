# Vocabularies Swiss Art Research Infrastructure (SARI)

Initial controlled vocabularies used in the SARI project for the definition of nationalities and occupations. These vocabularies are not final, but represents the current state of work.

## Nationalities

The controlled vocabulary for nationalities includes terms from English (en-US) and german (de-DE) to indicate the national affiliation of an agent using the following forms:

* English male singular
* German male singular
* German feminine singular
* German neuter singular

Examples of the terms used are:

> |-----------|-----------------|----------------|---------------|
> | Brasilian | Brasilianischer | Brasilianische | Brasilianisch | 

Each term is linked with the corresponding one present (when available) from the [Art and Architecture Thesaurus](https://www.getty.edu/research/tools/vocabularies/aat/) produced by the [Getty](http://www.getty.edu).


## Occupations

The controlled vocabulary for occupations includes terms from English (en-US) and german (de-DE) to indicate the occupation of an agent using the following forms:

* English male singular
* English feminine singular
* English male plural
* English feminine plural
* German male singular
* German feminine singular
* German male plural
* German feminine plural

Examples of the terms used are:  

|-------------	|---------------	|-------------	|---------------	|---------------	|---------------	|-----------------	|-----------------	|
| businessman 	| businesswoman 	| businessmen 	| businesswomen 	| Geschäftsmann 	| Geschäftsfrau 	| Geschäftsmänner 	| Geschäftsfrauen 	|

Each term is linked with the corresponding one present (when available) from the [Art and Architecture Thesaurus](https://www.getty.edu/research/tools/vocabularies/aat/) produced by the [Getty](http://www.getty.edu).


## Model

The vocabularies are Semantic Web ready and modelled in RDF using both the [Ontolex](https://www.w3.org/2016/05/ontolex) and [Lexinfo](https://lexinfo.net/) ontologies. A graphic model of the mapping is available below in figure 1

![**Figure 1**](https://workspace.digitale-diathek.net/confluence/rest/gliffy/1.0/embeddedDiagrams/ea8df865-2778-4b49-850a-bdbf437db060.png)


The main entity (e.g. sari:2CF4DA9C-69DF-46DA-89CC-CE96BCA21716) are described as `crm:E55_Type`, `skos:Concept` and `ontolex:lexicalConcept` and linked with `ontolex:LexicalEntry` in German and English.
Each `ontolex:LexicalEntry` is linked using `ontolex:lexicalForm` with a `ontolex:Form` identified by a gender, a number, and by a `ontolex:writtenRep`.     

Preferred forms in both English and German are identified at both the root level using `skosxl:prefLabel` as well as in the `ontolex:LexicalEntry` level using the property `ontolex:canonicalForm`. Moreover, for practical reason, each `ontolex:LexicalEntry` describe also the preferred label of that entry using `rdfs:label`.     

Language are decoded using both the language tags in the labels as well as with the link to [glottolog.org](https://glottolog.org)


## Adding terms

Currently there is no automatic way to ingest or add new term. If you are using the vocabularies and would like to import some of your terms, the process can be done manually. Please, open an issue and request the addition for new terms.