# 01. Doing violence to reality

$public=true$

$p=1$

human behaviour silos
- social scientists are trained within certain frameworks, which have their associated methods
- limits the sorts of questions researchers tend to ask + approaches to answer those questions
- => researchers often lack frameworks or tools for dealing with complex problems at multiple scales

$p=2$

why modelling?
- arming social and behavioral scientists with a basic toolkit
of **formalized theories** and models will allow them to **tackle the most important questions
from ==multiple perspectives==**
- provide a language through which richer theories of social behaviors can be developed and communicated

----
$widec$
Why should you do violence to reality?
$/widec$
----

**1.** stepping stone
- we first have to understand **simple systems** before we can understand complex systems

**2.** precision 
- we receive little training in understanding social systems with much precision

## Flocking birds and boids

### An illustration of local behaviour

$p=2-3$

flocking starlings
- no central authority coordinating individual bird flight
- each bird is aware only of its **immediate surroundings**
- => **emergent behaviour**

$p=3$

emergent behaviour?
- description at the **level of the collective** is fundamentally distinct from the behavior of the collective’s **individual constituents**

### Boids

boids
- virtual birds programmed in a simulation
- each boid is aware only of its local surroundings -> no individual boid is aware of the entire flock

$widec$
$down three rules
$/widec$

**1.** separation
- if there are other boids immediately in front of you, turn away from them
to avoid collisions and crowding

**2.** alignment
- turn to align with the average heading of nearby boids

**3.** cohesion
- attempt to stay close to nearby flockmates by steering toward the average
position of nearby boids

$gallery$
![Image](img$cefu)
$/gallery$

$p=4$

$gallery$
**Screenshot from a simulation of the boids model**

![Image](img$kup9)
$/gallery$

### Agent-based models

agent-based model
- model in which individuals are represented as computational entities (= agents)
- agents behave and interact locally

*models*
- a simplified representation of reality
- we can instantiate this representation to observe the consequences of our assumptions

## What are models?

### What is a model?

model
- an abstract or physical structure
- can *potentially* represent a real-world phenomenon

$p=5$

### Types of studies

|direct study|indirect study|
|---|---|
|questions are about the thing you are observing|questions are about something else than you're observing|
|directly|proxy|
|e.g. weighing a rock|e.g. marshmallow test|

$p=6$

### Formal models

formal models
- mathematical or computational specifications of a system

|formal models in exact sciences|formal models in social sciences|
|---|---|
|elements of a model are direct representations of measurable quantities in the world|models are intended to capture core elements of a theoretical idea|
|(usually) near-perfect one-to-one mapping between measurement and model|*no* perfect one-to-one mapping between measurement and model|

circularity
- the model produces what you expect because you built in the assumptions
- model analysis is merely a series of computations based on assumptions specified by the modeler
- a formal model is a logical engine that turns assumptions into conclusions

assumptions and consequences
- often: we cannot predict consequences from our assumptions

model building
- forces us to reflect on what we *are* assuming
- also: what we *must* assume (minimal requirements)

$info$
Good models can show us how our assumptions lead to unexpected conclusions.
$/info$

## The parable of the cubist chicken

verbal ambiguity
- everywhere in language
- problematic for science -> amounts to **imprecision**

verbal theories
- theories which solely exist in a verbal fashion
- opens up explanatory power to ambiguities

$p=8$

$reader$
In the social and behavioral sciences, the search for clarity can present a problem for verbal
models and can lead to a depressing recursive avalanche of definitions. For example, many
researchers are interested in preferences. But before we ask about the sorts of things that
influence preferences or are influenced by preferences, we should first ask: What _is_ a preference? Perhaps a preference is a tendency to choose certain behaviors over others. This leads
to a new question: What are the available behaviors? Of course, the set of possible behaviors depends on the social and environmental context. What are these contexts, and what
determines them? This can go on for a while.
$/reader$

formal models as an escape from recursive abyss
- discussion is restricted to the model system

$widec$
$down problem
$/widec$

all models are obviously wrong
- gross oversimplifications -> leave out important details

$widec$
$down solution
$/widec$

stupidity as a strength
- focus only on part of the real-world system
- theoretically: how would such a system work if we *could* ignore everything we are ignoring?

$wide$
- => formal models help solve the problem by **systematizing our stupidity**, and ensuring that, at the very least, **we are all talking about the same thing**
$/wide$

## Decomposition

### The use of decomposition

standard science
- hypothesis, testing, statistical significance ...

$result problem
- where do hypotheses come from?

$p=8-9$

$reader$
A hypothesis is usually a proposal that the parts of a system are organized in some way
and/or that because the parts are organized in a particular way, some phenomena and not
others occur. But what are these parts? If we want to understand some aspect of a system and
form hypotheses and theories about it, we first have to articulate the parts of the system, a
process I’ll call **decomposition** after Herbert Simon, who used the term similarly. 
$/reader$

$p=9$

$widec$
$down questions we have to answer
$/widec$

1. What are the parts of the system we are interested in? 
2. What are their properties? 
3. What are the relationships between the parts and their properties? 
4. How do those properties and relationships change?

$result decomposition
- consists of usable answers to these questions

how decomposed?
- depends on the questions you are trying to answer with your model
- *and* the granularity required for answers to those questions

$info$
The value of a model largely depends on how well
its decomposition usefully answers the questions the modeler is asking.
$/info$

$gallery$
**Decomposition visualised (OC)**

![Image](img$p1ue)
$/gallery$

### Theory

theory
- always embedded in every idea
- our mental perception of the world is also influenced by **categories** and **schemas**

$widec$
$down
$/widec$

models
- reflections of how *we* parse the world
- there are *many* ways to parse the world -> many ways to model the world

$p=10$

----
$widec$
_[I]t is the question that determines the relevant parts of the system_
$/widec$
----

building models
- thinking about the parts to **include** and the parts to **ignore**

$widec$
$down
$/widec$

$wide$
- What questions does your theory address?
- What parts do you need to include to answer those questions?
- Is your model a satisfying representation of your theory? If not, why not?
$/wide$

### Canonical models

canonical models
- well-known models in social sciences
- useful for shared communication about a topic if you have the same reference point

$deflist$
hypothesis
:  a prediction that **if a particular set of assumptions are met, a particular set of consequences will follow**

$info$
In practice, [a hypothesis] is a prediction that either (1) the
parts of a system are organized in a particular way—in other words, that a particular decomposition carries explanatory power for some observed phenomena—or that
(2) because the parts of a system are organized in a particular way, certain phenomena and not others will occur. Good hypotheses allow us to exclude and distinguish
between competing theories.
$/info$

theory
: a set of assumptions upon which hypotheses derived from that theory _must_ depend

$info$
Strong theories allow us to generate clear and falsifiable hypotheses.
$/info$

theoretical framework
: a broad collection of related theories that all share a common set of core assumption

$example$
An example of a theoretical framework is Darwinian evolution by natural selection, from which many subordinate theories have
been derived.
$/example$
$/deflist$

$p=11$

## Formal theory in the inexact sciences

### Hard science <-> soft science

challenges in doing science
- pinning down *what we are talking about*

hard science (according to Popper)
- concerns **falsifiability**

[ Karl Popper's distinction between 'science' and 'non-science' ]
|science|non-science|
|----|----|
|theory can be falsified through empirical result|theory **cannot be falsified** through empirical result|

$wide$
- $result 'soft science' on outskirts of what science is (according to this definition)
$/wide$

### Exact science <-> inexact science

----
$widec$
New distinction by Smaldino
$/widec$
----

[ Smaldino's distinction between 'exact sciences' and 'inexact sciences' ]
|exact sciences|inexact sciences|
|---|---|
|theories involve direct mappings between measurable constructs and model predictions|mappings between measurements and theories are imprecise|
|terms in fundamental equations all have universally-accepted units (e.g. mass, velocity)|model parameters don't align with empirical measures (typically ==proxies==)|
|$result theories are exact specifications of the relationships between quantities that can be measured with high level of precision|$result theories are more vague approximations of relationships assumed to hold (nvda.)|

$info$
Exactness is more like a _continuous variable_ rather than a _binary characteristic_.
$/info$

inexactness of models
- leads to dismissal of theories -> 'they don't capture enough!'
- however: extreme simplification is the entire point

$p=12$

## Why model?

### Predictions and assumptinos

prediction from models in social sciences
- a difficult task! -> often not achievable, or very imprecise
- but: *qualitative* predictions still valuable

|statistical models|generative models|
|---|---|
|powerful predictive correlations|qualitative predictions / no predictions at all|
|*extremely* dependent on conditions of the study|conditions modelled explicitly|

### Precision

#### Types of models

==**mental models**==
- simlpified descriptions of the world in our minds

==**verbal models**==
- descriptions of ==assumptions required== to explain a phenomenon
- written in **plain language**

==**formal models** (nvda.)==
- descriptions of ==assumptions required== to explain a phenomenon
- written in **formalised language**

$p=12-13$

$example$
The most successful verbal model—from a scientific point of view—may be **Darwin’s theory
of evolution by natural selection**, which provides the foundations for explaining much of life
as we know it. Darwin’s writings contain no mathematical formalisms, only richly described ideas.
$/example$

$p=13$

#### Distinction between verbal models and formal models

|verbal models|formal models|
|---|---|
|contain ambiguity|_cannot_ contain ambiguity|
|multiple interpretations|unique interpretation|
|useful for prototyping|useful for final  product|

$widec$
(ideas echoed from Gong & Shuai, nvda.)
$/widec$

#### Benefits of formal models

explicit assumptions
- formal models must have *all* assumptions explicited

$widec$
$down benefits
$/widec$

$acco$
**1.** clear ==scope==
- it is explicit **which contraints are required** for the theory to apply
- helps us to know when an empirical finding does or does not affect the validation of a theory
$/acco$

$acco$
**2.** aids ==communication==
- ambiguity from verbal models is avoided

$example$
We sidestep the problem of the Cubist chicken, because the formalism tells us exactly what the parts are and how they fit together.
$/example$
$/acco$

### $tt=handelbaarheid$Tractability$/tt$

$info$
Met 'tractability' bedoelen ze hier 'haalbaarheid'.
$/info$

tractable models
- formal models act as logical engines that turn **assumptions** into **conclusions**
- if assumptions are stated, we know what outcomes follow from these assumptions

$widec$
$down benefits
$/widec$

**1.** overcome ==real world messiness==
- time, resources, causality, ethics -> difficult to do research
- possible in formal models

$wide$
**2.** overcome ==time-scale constraints==
$/wide$

**3.** explore ==counterfactual scenarios==
- think up a world in which other constraints apply
- also: ethical constraints, time machine constraints ...
- _how might things have played out under different circumstances?_

**4.** ==cheap==
- running a simulation is usually **much
less costly** in terms of both time and resources than collecting sufficient empirical data to
build and test dynamical theories

$widec$
(more echoes from Gong & Shuai)
$/widec$

### Insight

$p=13-14$

gaining **insight**
- models provide us with a cognitive arsenal for understanding complex systems
- => model as a **playground** to explore dynamics of complex systems

$p=14$

## Some models of note

interesting models
- models which show how models can contribute to science

### Newton's model of gravity

$p=15$

$gallery$
**Newton’s model of planetary gravitation**

![Image](img$n3jh)

Earth has a forward velocity 𝑣, which is continuously altered by the gravitational attraction of the Sun, 𝐹~𝑔~, resulting in an elliptical orbit. In
reality, the model is even simpler than implied here, because the Sun and Earth are represented as
point masses rather than spheres.
$/gallery$

### The Lotka-Volterra predator-prey model

two animal species
- prey species: positive rate of growth in absence of predators
- predator species: negative rate of growth in absence of prey

relations
- number of predators negatively influences the number of prey
- number of prey animals positively influences the number of predators

model
- produces correlated oscillations in the two populations
- identifies conditions for end of oscillations
	1. stable equilibria
	2. population collapse

simplicity
- ignores seasonality, circadian cycles, migration, other species ...

$p=16$

extensions
- war and piece in human society

$gallery$
![Image](img$b44k)
$/gallery$

## Equation-based models and agent-based models

$p=16-17$

### Comparison

<table>
<tr>
<th></th>
<th>equation-based models</th>
<th>agent-based models</th>
</tr>
<tr>
<th>relationships</th>
<td>

**equations** specify the relationships between the parts of a system
</td>
<td>

individual **agents** enter into relationships 
</td>
</tr>
<tr>
<th>aggregation</th>
<td>necessary</th>
<td>not necessary</td>
</tr>
<tr>
<th>parameter exploration</th>
<td>easy -> plug in new numbers</td>
<td>possible, but less straightforward</td>
</tr>
<tr>
<th>heterogeneity<br>(spatial/network structure)</th>
<td>ill-suited</td>
<td>well-suited</td>
</tr>
<tr>
<th>complexity</th>
<td>complicated</td>
<td>intuitive</td>
</tr>
</table>

$p=19$

### Two ways of doing the same thing

$p=19-20$

$gallery port$
![Image](img$vgp5)
![Image](img$kgxi)

1. Temporal dynamics of infected individuals in the equation-based SIR model with a
recovery rate of γ = 0.07. This compares populations under either high transmissibility (β = 0.3)
or low transmissibility (β = 0.15).
2. Temporal dynamics of infected individuals in the agent-based SIR model. Agents
move using a random walk with either a large (orange) or small (blue) step size.
$/gallery port$

$p=19$

$gallery port$
![Image](img$ts74)
![Image](img$u561)

1. Visualization of a spatial agent-based SIR model. There are 500 agents, which
can be either susceptible (white), infected (red), or recovered (grey). 
2. Example random walk trajectories over 100 steps for agents taking either large (orange) or small (blue) steps.
$/gallery port$

$p=20$

## Fine-grained and coarse-grained models

### Comparison

|fine-grained models|coarse-grained models|
|---|---|
|there are **data** in the world that can be used to precisely parameterize and test the models|focus on broad, **qualitative patterns** in the data|
|e.g. mass, pressure, voltage|e.g. emotion, perception, norms|

$acco$
**Fine-grained models**

$example$
In epidemiology, some
agent-based models are calibrated using high-precision data on demographics, geography,
schools, travel matrices, and so forth, with the goal of predicting the time course of an epidemic. 
$/example$

$example$
In neuroscience, biophysical models might exactly predict the dynamics of action
potentials or motor behaviors.
$/example$
$/acco$

$acco$
**Coarse-grained models**

$info$
The utility of [concepts like norms and perceptions] in lay thought and communication is indisputable,
but it is less obvious how they should be measured for scientific study. Even when a concept
is precisely defined, measurement is often made difficult by constraints of time, resources,
or ethics.
$/info$
$/acco$

### Complexity of complex systems

complex systems are complex
- many interdependent components that interact in non-linear fashion
- => difficult to model with precision

$p=21$

## The journey begins

