# Modelling pronominal gender agreement in Dutch

$public=true$

$p=219$

## Introduction

$p=221$

agent-based model
- reorganisation of gender in Dutch

$p=221$

## Gender in Dutch

$widec$
(De Vogelaer re-iteration)
$/widec$

$p=224$

## Anaphoric reference game

language game
- yes

$p=225$

### Vocabulary

vocabulary
- 60 words, each with a gender
- also have values for tangibility, countability and animacy

$p=226$

$info$
Each construction represents an one-to-one mapping between a noun and its gender. In the case of gender acquisition for a word, the agent adopts a new construction for the respective noun, such that all the semantic properties of the word are
kept, while the score is initialized and the gender takes the new acquired value.
The old and new constructions now become gender competitors for the same
noun. 
$/info$

$gallery port$
$widec$
![Image](img$hox3)
$/widec$
$/gallery port$

$p=227$

$gallery$
**Example construction for 'hond' in FCG**

![Image](img$m1bm)
$/gallery$

### Learning operators

mapping mechanism
- allows agents to *infer* the gender of a word if they don't know
- works through **exemplars**

$result exemplars?
- each gender has a word with a very high score for gender
- that word serves as the basis for comparison (using feature vectors)

$p=228$

$reader$
The final step of the language game is the so-called alignment, performed by
the hearer. <span style="color: red;">**The agent that plays the role of the speaker does not perform 
any adjustment on his internal model, as this would mean that half of the time the agent will
boost his own preferences**, making him less adaptive overall (Wellens 2012)</span>. 
$/reader$

lateral inhibition
- widely adopted alignment method in the field of language games
- in case of a successful interaction, an agent...
	- ...decreases the scores for competing constructions
	- ...increases the score for the correct solution
- when a game fails, the wrongly chosen construction is decreased in score

$info$
A systematic overview of alternative updating functions is contained in ==Oliphant (1997)==.
$/info$

### Evaluation

----
$widec$
Measures that will be used to evaluate the outcomes of the language model
$/widec$
----

communicative success
- determine if an interaction was successful or not
- can happen in two cases:
	1. the speaker and the hearer have the same preferred gender for a word
	2. the hearer has the speaker’s solution in its inventory, but he did not choose it as its preference

alignment success
- measures the degree to which the agents have the same preferences over the genders for the elements of the world
- alignment success is reached at the end of an interaction only if the agents have the same choice of gender for the uttered noun

cluster purity  
(Manning et al. 2008, Chapter 16)
- a measurement of the quality of our final gender mapping

$p=228-229$

$reader$
We split our semantic space into 5
clusters (represented by all the feasible combinations of the features: animate-concrete-countable, inanimate-concrete-countable, inanimate-abstract-countable, inanimate-concrete-uncountable, inanimate-abstract-uncountable). For each cluster
we assign a class, i.e. the gender that is most frequently encountered inside the
cluster. The purity is then computed by dividing the number of words belonging
to this majority class by the total number of words in the cluster:

$widec$
$todo equation
$/widec$
$/reader$

$p=229$

## Results and discussion

----
$widec$
Three types of experiments
$/widec$
----

1. analyse the semantic systems that can form from our simulation when there is **no pre-existing syntactic gender system** in place
	- should offer us an indication regarding how well our chosen strategies can perform in terms of identifying discriminating dimensions and clusters
2. while **starting from the syntactic gender system**, we introduce a **gradual population replacement**
	- under various substitution and frequency rates
	- which conditions we still have a shift from the initial syntactic agreement system towards the semantic strategy?
3. we explore the effect of various knowledge transmission rates on the stability and purity of the obtained clusters

$info$
For all our experiments we use a closed population of size 20.
$/info$

### Weighing semantic features

weighting
- used to make a certain feature more important

$p=240$

population turnover rate
- percentage of population to be replaced

knowledge transmission rate
- percentage of gender knowledge to be transmitted between subsequent agents

turnover frequency
- population replacement interval in terms of number of interactions

$p=241$

### Population turnover

$p=244$

### Knowledge transmission

