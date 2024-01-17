# Modeling the Complexity and Descriptive Adequacy of Construction Grammars

$public=true$

##  Complexity and Descriptive Adequacy

construction grammars
- operate at multiple levels of representation (lexical, syntactic, and semantic)
- much more complex than
purely syntactic grammars

this paper
- $see $down

1. the **computational complexity of CxGs**
	- = complexity
2. the descriptive adequacy against unannotated corpora using Minimum Description Length
(MDL)
	- descriptive adequacy

$reader$
These two measures, complexity and descriptive adequacy, can be used together as an
**objective function** for measuring the quality of
CxGs: **the optimum grammar balances higher
descriptive adequacy against lower complexity.**
$/reader$

$reader$
The goal is not to examine the representational
capacity of CxGs in general because CxG is a fundamentally usage-based paradigm (Hopper, 1987;
Kay & Fillmore, 1999; Bybee, 2006). This means
that the general capacity of its grammars must
be weighted by their actual content: how can we
model the complexity of a specific CxG used to
describe a specific language, where that language
is represented by a specific observable corpus?
$/reader$

$reader$
**Previous computational work** on CxG (Steels,
2004; Bryant, 2004; Chang, et al., 2012; Steels,
2012) **has relied on introspection-based representations that require a linguist to determine the optimum constructions by intuition**. From a linguistic
perspective, these representations are **neither replicable nor falsifiable** and are **unable to test hypotheses about the mechanisms of emergence that map
from observed usage to learned generalizations**.
From a computational perspective, these representations are not scalable across domains and languages and are subject to all the constraints of
knowledge-based systems. Other data-driven approaches (Wible & Tsao, 2010; Forsberg, et al.,
2014) generate potential constructions but do not
evaluate the quality of competing CxGs as collections of constructions.
$/reader$

## Representing CxGs

### Types of representations

----
$widec$
Representations recognised by the algorithm
$/widec$
----

**1.** lexical representations
- consist of tokenised word forms (in lowercase)

**2.** syntactic representations
- consist of part-of-speech categories
- Universal POS tagset

**3.** semantic representations
- consist of clusters of distributionally similar words
- represent semantic domains, computed using GenSim's implementation of word2vec (Rehurek & Sojka, 2010)

$info$
The embedding model is trained using 1
billion words from web-crawled corpora for each
language (from the WAC corpora: Baroni, et al.,
2009; and Aranea corpora: Benko, 2014) using
skip-grams with 500 dimensions. These embeddings are segmented into categorical domains using k-means clustering (k = 100). The idea behind these three types of representation is that a
particular slot in a construction can be defined or
constrained at the lexical, syntactic, or semantic
level. These representations thus form the basic
alphabet of the algorithm.
$/info$

### What are constructions?

constructions
- sequences containing a certain number of **slots**

$acco$
$example$
$widec$
(1a) [slot 1 — slot 2 — slot 3 — slot 4]
$/widec$
$/example$

$result each construction
- surrounded by brackets
and each slot within a construction is separated by
a dash (“—”)

$result each slot in a construction
- represented or defined by **constraints** that govern which
units can occupy that slot
$/acco$

$acco$
$example$
**Types of constraints**

$widec$
(1b) [NOUN — “gave” — (animate) — “a hand”]  
(1d) [NOUN — (transfer) — (animate) — NOUN]  
$/widec$
$/example$

$result lexical constraints
- indicated using single quotes (e.g. "gave")

$result syntactic constraints
- indicated using part-of-speech tags in uppercase (e.g., noun)

$result semantic constraints
- indicated within parentheses with the identifier for the semantic domain (e.g. _animate_)
$/acco$

$widec$
$down
$/widec$

$info$
$example$
(1c) “Bill gave Peter a hand.”  
(1e) “Bill sent Peter a package.”  
$/example$

The construction in
(1b) describes the utterance in (1c) but not the utterance in (1e); the construction in (1d) describes
the utterances in both (1c) and (1e).
$/info$

$widec$
$down
$/widec$

$info$
This provides a good example of the **complexity problem**: CxGs potentially have **multiple overlapping representations for any given sentence**. The sentence in (1e), for example, can
be represented by the construction in (1d), in
which slots are defined by both syntactic constraints (i.e., NOUN) and semantic constraints (i.e.,
animate). CxGs can distinguish between (1e) and
its more idiomatic counterpart (1c) using representations such as (1d) and (1b). The question,
however, is **how many of these item-specific or
idiomatic representations are needed in the grammar**: each item-specific construction increases
grammar complexity.
$/info$

### Writing a grammar

$acco$
----
$widec$
In this paper
$/widec$
----

_construction_
- the grammatical description (e.g. 1b) 

_construct_
- a member of the set of utterances which that construction represents (e.g. 1c)
$/acco$

----

$reader$
For a given grammar, the set of constructions is
closed but the set of constructs is open. A construct or utterance can be represented by multiple
constructions: representations like (1b) that are
more item-specific alongside representations like
(1d) that are more schematic. This leads to relationships between constructions: an inheritance
hierarchy in which (1b) is a child of (1d).
$/reader$

----
$widec$
Limitations
$/widec$
----

1. constraints are limited to a **single type of representation per slot**
	- if a slot is constrained to the semantic
domain _animate_, any syntactic category could be
used to fill that slot
2. although constituents
are able to fill construction slots (i.e., “a hand”
can occupy a single slot as a single NOUN), **larger
constructions** such as (1d) **cannot fill slots in other
constructions**
3. no **relations are learned between constructions** in the grammar (i.e., the inheritance hierarchy is not modelled)

### Computational representation

construction
- an array of slots
- each slot = a tuple with two pointers
	1. pointer to the alphabet constraining that slot (i.e. lexical/syntactic units)
	2. pointer to a particular unit *within* that alphabet (i.e. "a hand" or <span class="feature">NOUN</span>)

slot-fillers
- can be constituents
-  accomplished using a context-free phrase structure
grammar containing rules such as $see $down

$rewrite$
NOUN -> DETERMINER + NOUN
$/rewrite$

$info$
The CFG is learnt during a syntax-only iteration described in the next section.
$/info$

$info$
The syntactic alphabet, then, also supports pointers to complex sequences through this CFG: the construction points
to a <span class="feature">NOUN</span> and the CFG allows larger constituents
to be labeled as a single <span class="feature">NOUN</span>. The current implementation produces a context-free CxG
$/info$

## Finding CxGs

### Building the grammar

data source for each language
- a large web-crawled corpus in
that language
- grammar is learned by searching across potential grammars, each of which is
evaluated against the corpus until the optimum
grammar is found
	- measure -> $see $down

$info$
The search for the optimum grammar is conducting using a tabu search (Glover
1989, 1990a) with multi-unit association measures
(Dunn, 2017) used to sample potential constructions.
$/info$

$result objective function
- very important
- how can we know that one
grammar is better than another without evaluating
them against gold-standard annotations?

### Levels

----
$widec$
Three levels of CxGs are learnt
$/widec$
----

**1.** CxG~LEX~
- operates only on **lexical** representations
- identifies purely lexical constructions: sequences of lexical items that have been fused together so that their internal structure can be ignored
- e.g. *could be* and *will be*

**2.** CxG~SYN~
- operates only on **syntactic** representations
- later used as phrase structure rules
- e.g. [<span class="feature">VERB</span> - <span class="feature">NOUN</span>] is identified as a purely syntactic construction

**3.** CxG~FULL~
- operates on **all levels of representation**
- constructions output from a previous pass become
atomic units in the current pass

## Measuring grammar quality

"grammar"
- a method for encoding observed linguistic utterances 
- the learner is searching for the smallest adequate encoding
method
- => can the grammar produce the utterances observed in held-out test-sets?

"optimal grammar"
- balances model complexity (the number and
type of constructions in the grammar) and the
amount of compression achieved when the model
is used to encode a test corpus

$eq$
$$
M D L=\min _G\left\{L_1(G)+L_2(D \mid G)\right\}
$$

- the optimum grammar is the grammar which minimises model complexity (represented by the encoding size of the grammar) and the size of the dataset encoded *by means* of the grammar
$/eq$

$eq$
**Encoding size in MDL**

$$
$todo
$$
$/eq$

$eq$
**Comparing grammar models**

$$
$todo
$$

- to what degree is $G_A$ better than $G_B$?
$/eq$

### Relevance of Minimum Description Length

why?
- does not rely on gold-standard annotations

$widec$
$down
$/widec$

1. we do not
necessarily have gold-standard annotations for every language and language variety we are interested in
2. simply relying on gold-standard annotations ignores the question we are most interested
in: how do we know empirically that one grammar is better than another?

## Measuring the encoding size of CxGs

## ???

## Results and discussion

