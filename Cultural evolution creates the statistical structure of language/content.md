# Cultural evolution creates the statistical structure of language

$public=true$

$reader$
**Abstract**

Human language is unique in its structure: language is made up of **parts that can be recombined
in a productive way**. The parts are not given but have to be **discovered** by learners exposed to
unsegmented wholes. Across languages, the frequency distribution of those parts follows a **power law**.
Both statistical properties—**==having parts==** and **==having them follow a particular distribution==**—facilitate
learning, yet their origin is still poorly understood. Where do the parts come from and why do they
follow a particular frequency distribution? Here, we show how these two core properties emerge
from the process of **cultural evolution** with whole-to-part learning. We use an experimental analog
of cultural transmission in which participants copy sets of non-linguistic sequences produced by a
previous participant: This design allows us to ask if parts will emerge purely under pressure for the
system to be learnable, even without meanings to convey. We show that **parts emerge from initially
unsegmented sequences**, that **their distribution becomes closer to a power law over generations**, and,
importantly, that **these properties make the sets of sequences more learnable**. We argue that these
two core statistical properties of language **emerge culturally** both as a cause and effect of greater
learnability.
$/reader$

$p=1$

## Introduction

### Fundamental properties of language

$acco$
language segmentation
- segmented into smaller parts -> combined **sequentially**

skewed frequency distribution
- power law distribution
$/acco$

$result make language **learnable**
- arise from **cultural transmission** -> repeatedly learnt by multiple generations

$widec$
$down
$/widec$

fundamental challenge of language acquisition
- discovery of relevant parts of language
- in spoken language: **no clear word boundaries**

### Segmentation

#### How segmentation works

statistical regularities
- serve as cues for word boundaries in speech

$widec$
$down
$/widec$

transitional probabilities
- which syllable is likely to follow another?
- can cue word boundary

$info$
The transitional probabilities within these units will be higher than the transitional probabilities across unit boundaries.
$/info$

$reader$
Take the sequence _pretty baby_ as an example, there are many different words that can appear after
_pretty_ (e.g., _car_, _boy_, _hat_, _cat_, and many more) but there are only few sounds that can appear after _pre_ and result
in a possible English sequence (_premature_, _precise_, and some more). This makes the transitional probability of
syllables within a word (of the syllable _ty_ given _pre_ in our example) higher than that of syllables across word
boundaries (_ba_ given _ty_). A wealth of experimental evidence shows that infants, children and adults can track
these transitional probabilities and use them to segment a novel continuous speech stream into its constituent
parts (see 5 for a review). 
$/reader$

$p=2$

#### Origins of segmentation

statistical learning literature
- focusses on segmentation in languages that **already have parts**

$widec$
$down
$/widec$

----
$widec$
How does language end up being constructed of parts whose combination makes such a learning strategy effective?
$/widec$
----

easy answer
- language is made up of parts because of the nature of the meanings we want to convey with language, which are themselves made up of parts
- => "because the world has structure"

this study
- language has structure, regardless of meaning

### Power law

#### What is the power law?

frequency distribution
- not all words occur with equal frequency -> exponential!
- => power law distribution (**Zipfian**)

#### Advantage

facilitative for learning
- performance in **word segmentation improves** when power law distribution
- => cognitive preference for such distributions

$widec$
$down
$/widec$

----
$widec$
Why does this facilitative distribution arise in language?
$/widec$
----

### Learnability

learnability
- both *cause* and *effect* of two fundamental properties of language:
	1. having parts
	2. having power law distribution

circular?
- no/yes -> product of one generation's learning in the target for the next

$wide$
- => iterated learning over multiple generations leads to languages that are **optimised for learning biases** inherent in transmitting individuals
$/wide$

### Research questions and hypotheses

whole to part learning
- start from single words and multiword sequences

$widec$
$down

**distributional properties** of language can, and **will emerge** through the process of cultural transmission
$/widec$

$p=3$

$widec$
$down consequences of whole-to-part learning *and* iterated learning
$/widec$

**1.** gradual emergence of sub-parts 
- higher transitional probabilities *within* units <-> *across* units

**2.** increasingly skewed distribution
- power-law after a while


### Methodology

experimental setting
- learn language of colour sequence, then reproduce it later
- but: task frames as copying a whole, but copying is difficult
- => will iterated learning biases take over?

## Methods

$wide$
Simon game
$/wide$

## Results

$p=4$

$gallery$
**Change in error across generations in the experiment**

![Image](img$bmmc)

- The error value shown is an average across the different chains for each generation (error is calculated for each sequence, then averaged across all sequences
in the set, then averaged across the six chains).
- Error bars are bootstrapped 95% CIs. 
- There is a clear **downward trend in error**, indicating that the sets of sequences in later generations are easier to copy than those of earlier
ones.
- => The sequences have evolved to become **more learnable**.
$/gallery$

$gallery port$
**Segmentation emerges**

$widec$
![Image](img$haqk)
$/widec$

$widec$
The numbers refer to generations in the experiment  
Dashed lines indicate particularly low transitional probabilities detected by our segmentation method
$/widec$

- Segmentation occurs when there is a drop in the transitional probabilities in a sequence of syllables -> indicative of a word boundary
$/gallery port$

$p=5$

$p=6$

$gallery$
**Change in the length of the units (i.e., the parts segmented by our procedure) over generations**

![Image](img$fb7b)

- The vertical coordinates represent the average length of all the units in a particular generation, averaged across all of the chains.
- => **Units are getting shorter**, indicating that smaller parts are emerging out of the larger wholes over generations.
$/gallery$

$gallery$
**Change in the transitional probabilities within and between units over generations.**

![Image](img$ra1r)

- After applying our segmentation method, we can classify each transitional probability
within a sequence as being within a unit or between two units. Each point on the graph shows the means
(for a particular generation across all chains) of the within-unit and between-unit transitional probabilities.
- Necessarily, due to the way we infer cutting points, the across-unit probabilities will be lower, even in generation
zero.
- => The key point here is that the **transitional probabilities _within_ units increase**.
$/gallery$

$p=7$

### Statistical structure emerges

$gallery$
**Distributions of units in the sequence sets over generations**

![Image](img$qukl)

- Each is plotted as a count of how often each unit occurs against its frequency rank. Bootstrapped 95% CIs across chains are shown as a shaded region
around the mean.
- => From the initial relatively uniform distribution, **a skewed distribution emerges** with a small
number of high frequency units and a long tail of low frequency ones.
$/gallery$

$p=8$

### Learnability as both cause and effect

$gallery$
**Entropy of units plotted against generation**

![Image](img$40si)

- Entropy is calculated for each generation in each chain
and the average across chains is plotted. Error bars are bootstrapped 95% CIs.
- => There is an initial increase in entropy due to an increase in inventory size (since the initial random set of sequences has very few segmentable
units), but then **the increasingly skewed distribution leads to a reduction in the entropy of units over
generations**.
$/gallery$

$p=9$

## Discussion

$reader$
ote that we deliberately designed our experiment to be a non-linguistic task. The memory game is one
that appears unrelated to language. The sequences have no similarity to language, and the task was not framed
as one which required participants to learn about properties of a set of behaviours. Moreover, both the whole
sequences and the emerging parts do not have meaning. Nevertheless, system-wide statistical structure emerges
that is strikingly similar to that found in languages. This suggests that structure in language may similarly arise
via cultural evolution through a **highly general process of iterated sequence learning**, rather than learning biases
that are specifically adapted to language. 
$/reader$