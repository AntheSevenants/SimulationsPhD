# 03. The Schelling Chapter

$public=true$

$p=53$

this chapter
- ==**segregation**==
- model by Thomas Schelling
- one of the most influential models of human social behaviour

further
- how to turn an **idea** into a **model**
- then: how to **analyse** that model
- paying particular attention to **assumptions**
	- decomposition and its consequences

## The puzzle of segregation

segregation
-  individuals of different races or ethnicities tend to be **geospatially clustered**

$p=54$

$gallery$
**Map of racial and ethnic divisions in the New York City metropolitan area**

![Image](img$189o)

- Red is White
- Blue is Black
- Green is Asian
- Orange is Hispanic
- Yellow is Other
- Each dot is 25 residents. Data is from the 2010 U.S. Census.
$/gallery$

----
$widec$
Possible explanations for segregation
$/widec$
----

==**1.**== organised action
- only certain classes of individual are permitted to live in certain neighbourhoods

$p=55$

==**2.**== socioeconomic filters
- race or ethnicity, once associated with different socioeconomic classes, retain those associations
- structural differences in opportunities and incentives for advancement and mobility

==**3.**== individual preferences / ==**homophily**==
- individuals may choose to live near others who are similar

$result why take individual preferences into account?
- 1. individual preferences can have an effect on population structure
  2. (more generally) relationship between individual preferences and population-level patterns are interesting

$widec$
$down
$/widec$

$result Schelling model
- how do homophilic inclinations translate to segregated spatial distributions?
- _in absence of other factors_, to what extent do individual preferences to live
near similar neighbours influence the population-level pattern of segregation?

## A model of segregation

### Requirements

model as a drastic simplification
- capturing the **essence** of segregation

individuals
- home location + group identity (race)
- with preferences of proportion of neighbours they can tolerate belonging to a different group
- if their neighbourhood falls below their preference threshold, they move

$info$
A funny thing about building models is that **a model almost always contains models
within it**. A model of segregation needs a model of _geographical space_ and models of _individuals’ ethnicity and behaviour_. ==It’s models all the way down.== 
$/info$

group identities
- 'at least two'

other facilities
- a minimal model of geographical space
- a mechanism for changing location

$p=56$

### Spatial properties

defining neighbourhoods
- requires an **explicit spatial structure**
- here: discrete square grid / ==square lattice==

$info$
The grid is discrete rather than continuous (as it was in the Particle World model) because
dwellings in most urban areas are **discrete**. Homes tend to have fixed locations, and you cannot move your home arbitrarily close to another. 
$/info$

$p=57$

$gallery port$
**A square lattice**

$widec$
![Image](img$4cj7)
$/widec$
$/gallery port$

$p=56$

----
$widec$
Important properties of a square grid
$/widec$
----

$acco$
==**1.**== intuitive to visualise
- simple to identify a neighbourhood, its race and its neighbours (and their races)
$/acco$

$acco$
==**2.**== symmetrical
- all agents will have an equal number of neighbours
- (assuming infinite size)

boundaries and **boundary effects**
- agents along boundaries have fewer neighbours -> effects
- to avoid this: **toroidal boundaries**

==**3.**== no effects of preferred axis of orientation
- not one area is more desirable or has more/less capacity of residency

==**4.**== easy to code
- it's simple
$/acco$

----
$widec$
Properties a square grid ignores
$/widec$
----

==**1.**== features common to real cities influencing **desirability**
- density of housing
- natural features (parks, rivers)

$p=56-57$

$info$
You might
find yourself a bit uncomfortable with this oversimplification. This discomfort is healthy—
hold on to it. It is **important to keep in mind the simplifying assumptions one makes when modelling**, because the results of our simulations are direct consequences of those
assumptions. [...] Nevertheless, we must always do violence to reality to make any sense of our world, and we have to start somewhere. 
$/info$

$p=57$

### Agent properties

$acco$
agent location
- one cell in the lattice
$/acco$

$acco$
agent ethnicity
- 'real' ethnicity not needed
- i.e. one of two colours (easy for viz)

$result problems
- 1. not all identities are clear-cut and observable
  2. one can have multiple identities at once

$info$
Because this is a simple baseline model, this is all OK.
$/info$
$/acco$

$p=58$

$acco$
agent behaviour
- stay if the fraction of similar neighbours is sufficiently high, and move
otherwise

$warn$
It is worth noting that **other formal decision rules** consistent with the idea that
“individuals prefer to live near similar neighbors” **are possible**, and that **using these may
somewhat change the model outcomes** (Bruch and Mare, 2006).
$/warn$
$/acco$

$acco$
'neighbourhood'
- several ways to operationalise a neighbourhood

[ Types of neighbourhoods ]
|Moore neighbourhood|Von Neumann Neighbourhood|
|---|---|
|![Image](img$th00)|![Image](img$qhuy)|
|eight closest cells|four closest cells|
|includes diagonals|cardinal directions only|

$result larger neighbourhoods
- larger squares, more area
- when you want agents to assess or otherwise interact with spatial neighbours on a square lattice

<table>
<caption>Neighbourhood extensions</caption>
<tr>
<th></th>
<th>r = 1</th>
<th>r = 2</th>
<th>r = 3</th>
</tr>
<tr>
<th>Moore neighbourhood</th>
<td>

![Image](img$7h7p)
</td>
<td>

![Image](img$lizu)
</td>

<td>

![Image](img$0u53)
</td>
</tr>
<th>Von Neumann neighbourhood</th>
<td>

![Image](img$zk5w)
</td>
<td>

![Image](img$47dr)
</td>

<td>

![Image](img$0cjm)
</td>
</tr>
</table>

$info$
In bounded finite spaces,
the neighbourhoods will become truncated, leaving agents near the edges of the space with
fewer neighbours than those nearer the middle. Toroidal neighbourhoods fix this issue again.
$/info$
$/acco$

### Dynamics

----
$widec$
How does the world change?
$/widec$
----

time step core loop
- each time step, every agent takes one of two actions
	1. do nothing and remain where it is
	2. move

neighbourhood calculation
- other agents can be perceived, and neighbourhood proportion can be calculated

$info$
An agent doesn’t
necessarily mind being a minority in its neighbourhood, but it wants to have at least some
similar neighbours.
$/info$

$p=59$

$wide$
- => If the proportion of my neighbours who are the same colour as I am is below my tolerance threshold, move. Otherwise, stay put.
$/wide$

'moving'
- search at random for a new empty cell which satisfies the conditions
- happens until ==**equilibrium**== is reached

$result equilibrium
- stable change that will not change further if the system is not perturbed

### Outcomes

----
$widec$
What do we want to learn from this model?
$/widec$
----

once equilibrium
- how segregated is the population?
- => measure of segregation

$widec$
$down
$/widec$

==**1.**== average similarity
- have each agent count the proportion of its neighbours that are the same colour as itself
- averaged over all agents
- for *no* segregation: should be 0.5

==**2.**== other measures $todo exploration

$p=64$

## A formal description of the model

[ Explaining simple <-> complex models ]
|simple models|complex models|
|---|---|
|can be fully described in just a few paragraphs|may require you to partition your model description<br>$down<br>important computations in the main text, specific implementation in the appendix|

$info$
Partitioning your model description is advised for **readability**
$/info$

variables
- i.e. grid with 𝐿 𝑥 𝐿 size (rather than specifying the size)
- makes model description **general**
- also reminds you of choices you make for parameter vlaues

### Initialisation

$reader wide$
Consider an 𝐿 × 𝐿 square grid with toroidal boundaries. At initialization, one agent is placed
upon each cell with a probability p, which characterizes the population density relative to
the available space (0 < 𝑝 < 1, so that each agent can relocate to an empty location). The
expected population size is therefore 𝑁 = 𝑝𝐿². The population is divided into 𝐺 groups, such
that each agent 𝑖 is randomly assigned a fixed group identity 𝑔~𝑖~ ∈ {1, 2, . . . , 𝐺}, each chosen with equal probability. For all of our analyses, we will use 𝐿 = 51 and 𝐺 = 2. The population is also defined by a similarity threshold, 𝑆, which defines the minimum proportion of an agent’s neighbors that must be similar for it to refrain from moving.
Note that the use of probabilistic assignments means that, even holding 𝑝 and 𝐺 constant, there will be some variation between simulation runs in terms of exactly how large
the population is and how many agents belong to each group. This stochasticity is often seen
as a positive because it allows us to assess how robust the model is to minor fluctuations.
However, one could also impose stricter requirements, so that, for example, the population
size was always the nearest integer value of 𝑝𝐿².
$/reader wide$

$p=62-63$

### Dynamics

$reader wide$
At any given time, each agent is either “happy,” in which case its neighbors are sufficiently
similar and it will not move, or “unhappy,” in which case it will move because its
neighborhood does not contain enough similar neighbors.

At the beginning of each time
step, each agent 𝑖 first determines whether or not it is happy. The agent considers the other
agents in its neighborhood (defined as a Moore neighborhood with radius r =1) and determines the proportion of its neighbors that share its group identity, 𝑠~𝑖~. If 𝑠~𝑖~ < 𝑆, the agent is
unhappy, otherwise it is happy. After each agent has made this assessment, each unhappy
agent, in random order, moves to a random empty cell (happy agents remain in their current
locations). These dynamics repeat until no agents are unhappy. And they all lived happily
ever after.
$/reader wide$

$p=62$

## Thinking about consequences

possible dynamics
- think about what your model could do

==**cascade**== effects
- movement of one agent sets in motion an entire reshuffling

$p=63$

## Coding the model

$p=68$

## The power of play

$p=69$

play
- good for getting to know your model
- understanding how the dynamics arise

Schelling conclusions
- even when everyone is content to be in the minority, most agents end up in highly segregated neighbourhoods in which they are the majority

$p=70$

## Model analysis

model analysis
- **quantifying a model's behaviour** more precisely

### Batch, please

|models based on equations|models using agents|
|---|---|
|deterministic|stochastic|
|mathematically **tractable**|mathematically **untractable**|
|we *precisely* can compute how model parameters relate to outcomes|we *cannot* compute how model parameters relate to outcomes|
|less realistic|more realistic|

$widec$
$down how to report on stochastic outcomes?
$/widec$

$result ==**batch run**== / ==**batch**==
- generate representative distributions of outcomes possible under each set of parameters being investigated
- then: descriptive statistics of model outcomes *across* simulations

\# of runs required?
- *depends*
- if model is very stochastic, you need more runs

how long to run a simulation?
- until natural stopping condition
- fixed number of steps

$p=71$

### Parameter sweeps

different parameters,  
different outcomes
- systematically vary the parameter values
- then record: how does the system respond?

dynamic range of parameters
- within 'reasonable ranges'

$info$
We should use parameters that are meaningful or realistic.
$/info$

consider arbitrary / implicit assumptions
- not all decisions in your model may be as straight-forward

$example$
**Implicit assumptions of the Schelling model**

- There are only two groups in the population.
- Each group is roughly the same size.
- The quality of a neighborhood is completely determined by the trait makeup of an individual’s neighbors on the nearest eight patches.
- There are no costs to moving.
- Decisions to move are all-or-none based on a threshold.
- All agents have identical thresholds for similarity.
$/example$

$result problem with assumptions
- it is difficult to consider the consequences of *every* alternative assumption
- will lead you much too far

==**curse of dimensionality**==
- the number of simulations needed increases exponentially with the number of parameters

$p=72$

$info$
Playing with your model can help you realize which parameters are probably important to explore and at which range of values, as well as which
parameters you can more safely ignore, or run for only a couple of values to ensure
robustness.
$/info$

### Null models

null conditions
- eliminate mechanisms hypothesised to generate the main outcomes of your model
- serve as a baseline to illustrate importance of a certain influence

### Where are the stats?

inferential statistics?
- regressions, analyses of variance
- $see Chapter 10 for why no inferential statistics

$p=73$

## Analysing the segregation model

### BehaviorSpace

----
$widec$
To what extent do individual preferences for living among similar neighbors yield segregated
communities?
$/widec$
----

$result modus operandi
- vary thresholds, then check the effect (and quantitative measure)

here
- model capped at 100 steps
- usually 100 steps is enough to catch an equilibrium

how many runs?
- here: 100 for each combination

$p=76$

### Results

qualitative results
- 1. as `similarity-threshold` increases, we get more segregation
  2. average percent of similar neighbours is **always considerably higher than the minimum** acceptable percent of similar neighbours that agents will tolerate
- => if agents move when their preferences are not met, **even weak individual preferences can generate strong patterns of segregation** at the population level
  3. the effect of population density is quite large

$reader wide$
At lower densities, the population becomes much more segregated than it does at high densities. This is partly because at lower densities, individuals
are likely to have only one or two neighbors, making the threshold harder to reach. Imagine
you are in an isolated cluster of three agents. If you have only two neighbors, the only way
to have at least 30% of them be the same color as yourself is for at least one of them to be
that color. But if the remaining agent is a different color, then 100% of _their_ neighbors are a
different color, and so they will move.
$/reader wide$

**==tipping point==** events
- events which change the whole entire equilibrium of the model
- in this case, much more common at lower densities

$p=75$

$gallery$
![Image](img$f552)
$/gallery$

$p=76$

### Loner behaviour

depressed loners?
- changing behaviour so agents don't want to be alone
- more noisy patterns
- slight decrease in segregation

$reader wide$
Being a loner should be fairly common under very low densities. If loners are always unhappy, they are more
likely to end up in mixed neighborhoods, thereby decreasing overall segregation. 
$/reader wide$

$reader wide$
Notice that something funny
seems to be happening for the lowest density and highest similarity threshold condition, as
seen in the upper right of the rightmost plot in Figure 3.10. Average segregation dips down
as a result of greater variation in outcomes. Playing around with individual runs shows that
this is due to longer times needed to reach equilibrium for the lonely loners, often greater
than the 100 time steps we allotted. The result is that the simulation ends before the population has reached its peak level of segregation. The spatial patterns of segregation that emerge
at low densities also differ between the two conditions, as depicted in Figure 3.11.

This figure
illustrates both the importance of examining the effects of seemingly minor assumptions, as
well as the ways in which summary statistics can be limited in describing the true patterns
present in a model system (or, indeed, in a real-world system).
$/reader wide$

$p=77$

$gallery$
![Image](img$is5x)
$/gallery$

## Reflections

high abstraction
- you might feel uneasy because it might seem 'too simple'
- however: you will grow accustomed to this

$p=79$

## Going deeper

$p=80$

## Exploration