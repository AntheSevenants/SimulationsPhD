# Frequencies, probabilities, and association measures in usage-exemplar-based linguistics

$public=true$

## Introduction

two large fields
- generative grammar
- cognitive/functional linguistics

$reader$
While corpus linguistic approaches have been around for quite a while, the methodological
evolution of corpus linguistics is still a relatively young development and many
corpus-based studies are lacking the methodological sophistication of much of
the experimental literature. This situation poses a bit of a challenge because, while
a usage-based approach to language — an approach stipulating that the use of
language affects the representation and processing language — does not require
usage data, the two are of course highly compatible. This makes the development
of an appropriate corpus-linguistic toolbox an important goal for usage-based linguistics.
$/reader$

this paper
- **collostructional analysis**
- developed to apply
recent developments in corpus linguistics to issues and questions in cognitive/usage-based linguistics

## Collostructional analysis: A brief overview

### Perspective 1: CA and its goals

$reader$
All of corpus linguistics is by definition based on frequencies — either on the
question of **whether something occurs** (i.e., is a frequency n>0?) **or not** (i.e., is
n=0?) or on the question of **how often something occurs** (how large is n?) — which
makes it a **distributional discipline**. Since linguists are usually not that much interested in frequencies per se but rather structure, semantics/meaning, pragmatics/
function, etc., corpus-linguistic work has to make one very fundamental assumption, namely that **distributional characteristics of an element reveal many if not
most of its structural, semantic, and pragmatic characteristics**

$widec$
(p. 479)
$/widec$
$/reader$

collocations
- the elements with which words in question co-occur

colligations
- the grammatical patterns with which words co-occur

association measures
- measures that
downgrade/penalize words whose high frequency around a word of interest 𝑤
may reflect more their overall high frequency than their revealing association with
𝑤

$example$
**Workflow of working with association measures**

1. retrieves all instances of a word 𝑤;
2. computes an AM score for every collocate of 𝑤 (cf. Wiechmann 2008 or Pecina
2009 for overviews);
3. ranks the collocates of 𝑤 by that score;
4. explores the top 𝑡 collocates for functional patterns (where functional encompasses ‘semantic’, ‘pragmatic’, ‘information-structural’, …)
$/example$

$result the purpose of ranking words on the basis of such AMs
- produce a ranking that will place words at the top of the list that
	1. have a relatively high
frequency around 𝑤 while 
	2. not being too frequent/promiscuous around other
words

### Perspective 2: CA and its mathematics/computation

collocation analysis
- the extension of AMs
- from lexical co-occurrence — a word M and its lexical
collocates — to lexico-syntactic co-occurrence: a construction 𝑐 and the 𝑥 words 𝑤~1~, 𝑤~2~, …, 𝑤~𝑥~ in a particular slot of 𝑐

## Bybee's points of critique

### Perspective 1: CA and its goals

most frequent implementation of CA
- two features
	1. downgrades the influence of words that are frequent _everywhere_
	2. weighs more highly observed relative frequencies of co-occurrence that are
based on high absolute frequencies of co-occurrence

Bybee's criticism
- "lexemes do not
occur in corpora by pure chance" -> "it is entirely possible that the factors
that make a lexeme high frequency in a corpus are _precisely_ the factors that make
it a central and defining member of the category of lexemes that occurs in a slot
in a construction"

$example$
Using the Spanish adjective solo ‘alone’ as an example, she goes
on to say that, for solo, “Collostructional Analysis may give the wrong results [my
emphasis, STG], because a high overall frequency will give the word solo a lower
degree of attraction to the construction according to this formula” (2010: 98).
$/example$

### Perspective 2: CA and its mathematics/computation

bottom right cell
- the number of constructions in the corpus

Bybee's criticism
- "there is no known way to count the
number of constructions in a corpus because a given clause may instantiate multiple constructions"

### Perspective 3: CA and its results, interpretation, and motivation

#### The perceived lack of semantics

collocation analysis
- has a "lack of semantics"

Bybee's criticism
- "[p]roponents of Collostructional Analysis hope to arrive at a semantic analysis but do not include any semantic factors in their method.
Since no semantic considerations go into the analysis, it seems plausible that no
semantic analysis can emerge from it" (Bybee 2010: 98)

#### The perceived lacks of semantics and discriminatory power

#### The absence of cognitive mechanisms underlying CA

$reader$
Gries and colleagues argue for their statistical method but do not propose a cognitive mechanism that corresponds to their analysis. By what cognitive mechanism does a language user devalue a lexeme in a construction if it is of high frequency generally? This is the question Collostructional Analysis must address.
(2010: 100f.)
$/reader$

## Clarifications, repudiations, and responses

### Perspective 1: CA and its goals

1. There are many flavours of AM.
2. 

$reader$
Bybee’s logic would force us to say that the as-predicative,
exemplified in (4) and discussed by Gries, Hampe & Schönefeld (2005), is most
importantly characterized not by regard (the verb with the highest collostruction
strength), but by see and describe, which occur more often in the as-predicative
than regard (and maybe by know, which occurs nearly as often in the as-predicative as regard). Given the semantics of the as-predicative and the constructional
promiscuity and semantic flexibility of especially see and know, this is an unintuitive result;

1. V NP~Direct Object~ as complement constituent
2. I never saw myself as a costume designer
3. Politicians regard themselves as being closer to actors
$/reader$

3. Relative frequencies are simply important, *and* informative

### Perspective 2: CA and its mathematics/computation

#### The issue of the corpus size

"exact number of constructions"
- cannot be easily estimated

1. “a given clause may instantiate multiple constructions” (Bybee 2010: 98);
2. researchers will disagree on the number of constructions a given clause instantiates;
3. in a framework that does away with a separation of syntax and lexis, researchers will even disagree on the number of constructions a given word instantiates

obvious remedy
- choose a level of granularity close to the one of the studied phenomenon

#### The distribution of p~FYE~

$widec$
Many effects in learning, memory, and cognition are _not_ linear
$/widec$

$wide$
- the power law of learning (cf. Anderson 1982, cited by Bybee herself);
- word frequency effects are logarithmic (cf. Tryk 1986);
- forgetting curves are logarithmic (as in priming effects; cf. Gries 2005,
Szmrecsanyi 2006), …
$/wide$

### Perspective 3: CA and its results, interpretation, and motivation

#### The perceived lacks of semantics

----
$widec$
Problems
$/widec$
----

$acco$
1. her claim appears to contradict
the exemplar-model perspective that permeates both her whole book and much of
my own work; “[s]ince no semantic considerations go into
the analysis, it seems plausible that no semantic analysis can emerge from it”

$widec$
$contrast
$/widec$

$reader wide$
There is a whole body of work in, e.g., computational (psycho)linguistics
where purely frequency-based distributional analyses reveal functionally interpretable clusters. Two classics are Redington, Chater & Finch (1998) and Mintz,
Newport & Bever (2002). Both discuss how multidimensional distributional analyses of co-occurrence frequencies reveal clusters that resemble something that,
in cognitive linguistics, is considered to have semantic import, namely parts of
speech. And even if one did not postulate a relation between parts of speech and
semantics, both reveal that something can emerge from a statistical analysis (parts
of speech) that did not enter into the analysis.

$widec$
(p. 493)
$/widec$
$/reader wide$
$/acco$

$acco$
2. it does not engage fully with the literature

$reader wide$
In sum, the statement that “[s]ince no semantic considerations go into the
analysis, it seems plausible that no semantic analysis can emerge from it” can only
be upheld by ignoring both the distributional linguistics literature that Bybee is
otherwise sympathetic towards and the specific collostructional literature that she
means to criticize and that shows the opposite.
$/reader wide$
$/acco$

$acco$
3. it is based on a
partial representation of ca, and so it is really arguing against a straw man
$/acco$

#### The perceived lacks of semantics and discriminatory power

$reader wide$
Bybee systematically chooses to not mention results of even a single
study with experimental and/or corpus-based data running counter to her claims,
but even a cursory glance at the literature shows that the picture is the opposite of
the one she painted or, at least, much more complicated.

(p. 496)
$/reader wide$

#### The absence of cognitive mechanisms underlying CA

$reader wide$
First, given the strong (experimental and otherwise)
support of collostruction strength in many studies that all adopt a cognitive-linguistic/usage-based framework, it is surprising there should be a special need for a
cognitive underpinning in addition to what all these studies are based on anyway.
Second, the earliest studies make it very clear what their cognitive underpinning
is. In Section 2.3 above, I already provided several quotes (from the studies Bybee
refers to) to illustrate the CA position: Ultimately, collostruction strengths are based
on (i) the conditional probabilities p(word|construction) and p(construction|word),
which are related to notions of cue validity, cue reliability (cf. Goldberg 2006: Ch.
5–6 and Stefanowitsch to appear), associative learning measures such as ΔP, and
prototype formation, and (ii) the frequencies that give rise to the probabilities,
which are correlated with entrenchment. Put yet another way: “it is assumed […]
that the statistical associations found in the data are reflected in psychological associations in the mind of the language user” (Stefanowitsch 2006:258).

(p. 496)
$/reader wide$

## Towards a new empirical perspective and its theoretical implications

### A cline of co-occurrence complexity and its motivations/implications

#### Approach 1: Raw frequencies/percentages

#### Approach 2: Association measures

#### Approach 3: Full cross-tabulation

#### Approach 4: Dispersion of (co-)occurrence

### Why CA works at all and a brief excursus on Zipf

### Towards a refined usage- / exemplar-based definition of construction