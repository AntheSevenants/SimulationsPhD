# A cultural evolutionary model of patterns in semantic change

$public=true$

$reader$
**Abstract**

Language change has been described as **an unintended effect of language in
use (Keller 1994)**. In this view, change results from the way individuals use
their language; the challenge is thus **to explain change and its properties in
terms of factors operating on the individual level, and population dynamics**.
An intriguing example of such a phenomenon is the finding that language
change shows some **highly regular tendencies**. This has recently received
considerable attention in the literature (Bybee et al. 1994; Heine and Kuteva 2002; Traugott and Dasher 2002; Hopper and Traugott 2003). In unrelated languages, **similar words often change in similar ways, along similar
‘‘trajectories’’ of development**. This phenomenon is called **‘‘unidirectionality’’**, and it is an important part of processes of **grammaticalization, items
changing from a lexical meaning to a grammatical function**. It has been
claimed that around 90–99% of all processes of grammaticalization are unidirectional (Haspelmath 1999).

This article explores several mechanisms that may lead to language
change, and examines whether they may be responsible for unidirectionality. We use a cultural evolutionary **computational model** with which **the effects of individual behavior on the group level can be measured**. By using
this approach, **regularities in semantic change can be explained in terms of
very basic mechanisms and aspects of language use such as the frequency
with which particular linguistic items are used**. One example is that **frequency differences by themselves are a strong enough force for causing unidirectionality**. We argue that adopting a cultural evolutionary approach
may be useful in the study of language change.
$/reader$

## Introduction

liguistic changes (p. 363)
- how at least some degree of regularity and directionality
- e.g. paths of grammaticalization as described in Heine et al. (1991), Bybee
et al. (1994), Heine and Kuteva (2002), Hopper and Traugott (2003)
	- describe tendencies in morphosyntactic change that are
often accompanied by a semantic change and an increase in frequency

$example$
An example is the development of _can_ (ABILITY -> POSSIBILITY),
in which _can_ has **changed from a full verb with lexical meaning** (indicating the subject’s ability to perform some activity) **to a modal auxiliary with a functional meaning** (indicating the likelihood of some
situation). (p. 363)
$/example$

this article (p. 363)
- explain such tendencies in semantic change
- a cultural evolutionary perspective on language, and using an
agent-based computer model of cultural evolution

$reader$
The **advantage** of using a cultural evolutionary approach is that **it models patterns in complex
systems such as the language of a population as a result of the interactions between individuals**, and by population-level processes of selection
and random drift. (p. 363)
$/reader$

$reader$
This approach is not new in itself: Keller (1994) proposes an approach of this kind in his **‘‘invisible hand theory’’**. In his
model, **group level phenomena are to be reduced to individual behavior**,
and the notions of mutation on the one hand and spread or propagation
of new variants on the other are distinguished. He states that **language
change is the unintended result of intentional individual behavior**. Individuals apply strategies or ‘‘maxims’’ when they use their language, such
as ‘‘speak in such a way that you are communicatively successful’’ and
‘‘talk like the others talk’’. Although most of these maxims lead to the
creation of linguistic conventions, **some maxims can — unintentionally
— lead to change**, such as ‘‘talk in such a way that you are noticed’’
and ‘‘talk in such a way that you do not spend superfluous energy’’.
Haspelmath (1999) uses Keller’s model to explain unidirectionality in
grammaticalization. (p. 363)
$/reader$

$reader$
<span style="color: red;">HEEL BELANGRIJK</span>

**Cultural evolution view**

Croft (2000) gives a conceptual model of language change as **cultural
evolution**. He explicitly states that actual utterances are the units of cultural transmission, a view that we adopt in this article. He also <span style="color: red;">differentiates between **linguistic factors** and **social factors**</span>. **Linguistic or cognitive
factors** give rise to new variants that come into existence by both **intentional and unintentional mechanisms such as reanalysis, creativity and
economy**. Whether these mutations spread through a population depends
on **social factors**, such as the structure of the population and the prestige
of speakers. (p. 364)
$/reader$

$reader$
Agent-based computer models of language change have been used in
other studies before, such as Niyogi and Berwick (1997) and Yang
(2000). These models simulate syntactic change as a result of imperfect
learning. A different approach, which is more comparable to the model
presented in this article, is the use of **‘‘language games’’**. **In these models,
change is the result of communication and adjustment of the agents’
knowledge based on the input they receive**, and imperfect learning plays
no role (e.g., de Boer 2001). In general, most of the studies using computer simulations so far have focused on syntax and phonetics. As Steels
(2003) has pointed out, **grammaticalization and unidirectionality have received less attention in this line of research**. (p. 365)
$/reader$

## Possible causes for asymmetries in semantic change

## The model

### Theoretical background

$reader$
we take a
**usage-based approach** to language change, in which individuals construct
their linguistic knowledge **on the basis of the input they receive in communication**, in which **actual utterances are the units of transmission and
in which the locus of mutation is in adult communication** (Bybee and
Slobin 1982; Croft 2000; Croft and Cruse 2004; Slobin 2005)

(p. 368)
$/reader$

### Properties of the model

$reader$
We use a so-called **‘‘agent-based model’’** of cultural evolution. The approach derives its name from the fact that it is a computer simulation of
a group of individuals, or agents. **The behavior of each agent can be independently controlled, and its effect on the population can be measured** (p. 368)
$/reader$

$reader$
The simple model we present here simulates the semantic evolution of a
single random word w in a population of speakers. The meaning of w is
represented by a set of senses, which represent concrete uses of w. These
senses are positioned on a one dimensional scale with a range of values
between 0 and 1. Each value on this scale represents a specific sense of w
with nearby values representing similar senses. The left end of the scale
(with value 0) is arbitrarily chosen to represent lexical senses and the right
end of the scale (with value 1) functional senses (Figure 1).

$gallery$
![Image](img$x2lj)

_The one-dimensional semantic scale of the model_
$/gallery$

(p. 369)
$/reader$

$reader$
Agents construct their linguistic knowledge on the basis of input they receive during communication. Communication in the model is the random
selection of two agents from the population, one of which is assigned the
role of speaker and one the role of hearer. The speaker selects a specific
sense (represented by a value) from its set of senses and transmits it to
the hearer. This models the evaluation by the speaker that the word w is
applicable in the specific context, given the set of senses of w that the
speaker knows. The hearer compares the transmitted sense to its own set
of senses, i.e., it evaluates whether the word w is applicable in the context,
given its set of senses of w. When this sense is already part of the hearer’s
knowledge of w, communication is successful and the communication
process comes to an end. However, the speaker can also transmit a sense
that is unknown to the hearer, i.e., that is outside the hearer’s range of
senses associated with w. In that case, communication fails, and the fact
of this failure is understood by not only the hearer, but also the speaker.

(p. 370)
$/reader$

$reader$
**Unsuccessful communication results in a learning process**, in which
both agents adjust their sets of senses of w. The **hearer**, confronted with
a new sense, will **increase its set up to (and including) the uttered sense**.
The **speaker**, confronted with unsuccessful communication, realizes that
any values beyond the uttered sense will lead to more unsuccessful communication and therefore **decreases its set and makes the uttered sense
its new limit**.

(p. 371)

$gallery$
![Image](img$1i82)

_An example of communication and learning. When a speaker utters a sense that is
not known to the hearer, this leads to a learning process in which both speaker and hearer adjust their set of senses._
$/gallery$
$/reader$

$reader$
Apart from the learning process described above, agents also change
their linguistic knowledge by **mutation**. Mutation in the model is a **randomly occurring small change in set size**. Agents that are selected for
communication have a probability m~r~ to undergo mutation before that
communication event. Mutations may be extensions or constrictions on
either side of the set. In linguistic reality, possible causes for the former
include the need to express something for which there is not yet a signal,
and for the latter the need to redress ‘‘semantic overextension’’ or competition by another word.

(p. 371)
$/reader$

$reader$
The population consists of 100 agents, and the agents have a maximum
age of 70 years, after which they are replaced by an agent with age 0.
Newborn agents start with an exact copy of the set of senses of a randomly assigned ‘‘parent’’, after which they participate fully in the communication between agents. Note that this ‘‘parent’’ is not the agent that
is being replaced (because in such a case there would be no need to add
generations in the model). Rather, **the transmission of the parent knowledge is a simplification of the acquisition process. This means that any
evolution displayed by the model is not due to imperfect learning situations in child language acquisition, but to variation coming about and
spreading in adults**; in this way we are able to test whether such variation can by itself lead to semantic change. Note that this does not mean
that transmission in the model is completely horizontal (i.e., within peer
groups only); communication is random between all agents regardless of
their age, and therefore transmission can be said to be both horizontal
and oblique (Cavalli-Sforza and Feldman 1981). (p. 372)
$/reader$

## Results

### General behavior of the model

$reader$
The simulations show slightly di¤erent behaviors each time they are run, with fluctuations in the average meaning
size as the result: specialization and generalization both occur. Basically,
the simulations exhibit random drift in the direction of both the upper
and lower limit of the meaning set. With meanings drifting in both directions along the scale, there is evolution, but no unidirectionality. (p. 373)
$/reader$

$gallery$
![Image](img$crta)

_Examples of random drift of the average meaning of w in 10 populations
(N = 100) after 500 years, showing both drift on the 0–1 scale and drift in size. Each
population started with an average knowledge with limits [0.4–0.6]. f = 500, mr = 0.01,
ms = 0.01._
$/gallery$

$reader$
We tested the effect of **three factors on this coherency**: **mutation rate,
frequency of use and population structure**. Coherency was measured as
the average amount of overlap, between agents in that population, of the
sets of senses. **The greater this overlap, the greater the consensus about
the meaning of word 𝑤** (eq. 3 in the appendix). (p. 374)
$/reader$

$reader$
First, the mutation rate in the population should not be too high. **A
certain amount of communication is needed for a single mutation to
spread through the entire population and to even out the emerged variation between the agents**. **When the number of communications relative to
the mutation rate becomes too low, the individual variation caused by
mutation is not transmitted to other individuals often enough, thus causing a lower coherency**  (p. 374)

$gallery$
![Image](img$mkyi)

_The coherency of the population (y-axis) with different mutation rates_
$/gallery$
$/gallery$
$/reader$

$reader$
Changes in frequency do not affect the
coherency of the population significantly (Figure 6b). (p. 374)

$gallery$
![Image](img$vpb2)

_The coherency of the population (y-axis) with frequencies of use (= communication between agents)_
$/gallery$
$/reader$

$reader$
Second, the population structure involves random communication between all agents. This might be realistic for small groups (of N = 100),
but not when populations are much larger. In the latter case it seems
more realistic to assume a population divided into several (socially based)
subgroups, within which agents communicate randomly, but between
which there is less frequent communication (cf. the notion of ‘‘social networks’’ in sociolinguistic theory, e.g., Milroy and Milroy 1992). We have
simulated such a structure by dividing the total population into a number
of subgroups and limit communication between individuals from di¤erent
subgroups. The probability of communicating with an agent from another subgroup is given by factor g. Not surprisingly, the less communication there is between the subgroups of the total population, the less coherent this population becomes. However, **only a very limited amount of
between-group communication (g = 0.01) is needed to create considerable coherency in the total population** (Figure 7). (p. 375)

$gallery$
![Image](img$cm1f)

_The coherency of a population of N ¼ 2000 divided into 20 subgroups of 100
agents, with different rates of g, the probability of communication with an agent from another
subgroup._
$/gallery$
$/reader$

$reader$
In summary, **populations are basically coherent unless there is a great
deal of mutation or virtually no communication between groups of
agents**. At the same time, word meaning gradually evolves within populations over time. Therefore, the model, simple as it is, behaves in a linguistically realistic way, and demonstrates the benefits of a cultural evolutionary approach to language change. (p. 375)
$/reader$

### Factors affecting the rate of semantic change

$reader$
Three possible explanations for this relationship were discussed: Words with a
general meaning are applicable in a wider range of contexts (factor 1),
they will have a higher frequency (factor 2) and they allow wider mutations (factor 3). As to the third factor, recall that the size of an individual
semantic mutation in our model is typically rather small, and is determined by a Gaussian function with a standard deviation (ms). However,
it is conceivable that di¤erent meanings allow different sizes for one-step
extensions; if so, then it is natural to assume that general meanings will
allow larger extensions than specific meanings, rather than the other way
around.
$/reader$

$widec$
(niet belangrijk voor ons)
$/widec$

### Factors causing unidirectional semantic change

$reader$
 First, speakers may only be able to freely manipulate lexical meanings of a word and second, functional meanings are
used more frequently than specific, lexical meanings. Haspelmath (1999)
argues that the combination of both factors leads to a unidirectional
change from lexical meaning to functional meaning.
We tested these two factors in the following way in the model.

The first
hypothesis is equivalent to an asymmetry in mutation: **words with lexical
meaning can be adapted to express functional meaning, but not the other
way around**. **To simulate this difference, we kept the mutation rate constant at m~r~ = 0.05, but varied the probability of the direction of mutations with a parameter p~m~.**

The second hypothesis concerns an **asymmetry in the frequency of use**:
senses with a functional meaning have a higher chance of being used in
communication than senses with a lexical meaning. **Individuals must select a sense of w for communication from within their set of meanings,
but here we varied how likely they were to pick different senses from
within that meaning.** In all simulations up to this point, individuals
picked a sense according to a **uniform** random distribution. In the present
set of simulations, **senses were picked according to an exponential distribution**. In this type of distribution, **the probability of selecting a certain
sense increases with increasing sense values**. The strength of this increase
can be altered with a parameter p~s~. For example, if p~s~ = 2, the probability of an agent selecting s = 1 is twice as big as selecting s = 0 (provided
the agent has both senses in its set of meanings), while with p~s~ = 100, the
di¤erence in probability is 100 (eq. 2 in the appendix).

(p. 380)
$/reader$

$reader$
Both factors combined indeed create a selection pressure that drives the
average set of senses of a population from the lexical side of the spectrum
to the functional side, even if both factors are weak (Figure 12a). Also,
the selection pressure blocks any change in the opposite direction (Figure
12b). (p. 381)
$/reader$

$reader$
These results seem to indicate that asymmetries in both mutation and
frequency might not have to be working together to create a unidirectional pressure. Small asymmetries in frequency and somewhat larger
asymmetries in mutation already lead to clear unidirectional change in
the model. However, as noticed above, a large asymmetry in mutation requires a fairly strict distinction between lexical and functional meanings,
and this may be at odds with the generally observed gradualness of semantic change, including shifts from lexical to functional (Hopper and
Traugott 2003); it may therefore be considered a relatively implausible
cause of unidirectionality on its own. In this respect, it is of course interesting that our model shows that the elementary mechanism of a small
difference in frequency is powerful enough to cause unidirectionality by
itself. (p. 384)
$/reader$