# 02. Particles

$public=true$

$p=24$

## NetLogo basics

NetLogo ==**primitives**==
- built-in procedures in NetLogo

### Patches, turtles and links

----
$widec$
Three important building blocks
$/widec$
----

|patches|turtles|links|
|---|---|---|
|![Image](img$2qy1)|![Image](img$2vmr)|![Image](img$uobp)|

$acco$
==**patches**==
- the default ==spatial organisation== in NetLogo
- a set of discrete square cells laid out in a two-dimensional rectangular grid
- each patch has a fixed, **unique location**
	- but: can be assigned arbitrary properties
- usually used to represent an **environment**
$/acco$

$p=25$

$acco$
==**turtles**==
- used to represent ==agents==
- can move, die, reproduce, or form nodes in a network
- spatially embodied
- have a position in continuous space
- have a directional heading

$info$
The continuous space overlaps with the discrete space on which the patches exist.
$/info$

$info$
One may also ignore these pieces of locational information if they are not important to a model’s dynamics.
$/info$
$/acco$

$acco$
==**links**==
- connections between turtles
- can be directed or undirected
- e.g. network
$/acco$

### Netlogo tabs

----
$widec$
Three tabs
$/widec$
----

==**Interface**==
- displays the **model visualizations**
- allows for real-time inspection of the model output as well as rapid parameter manipulation

$p=26$

==**Info**==
- a template for extensive documentation of the model and associated code
- nothing in this tab directly affects the run of the model itself

==**Code**==
- where the instructions for the model’s operation are coded

## Programming basics

$widec$
I know how this works, so I skipped this section :)
$/widec$

$p=30$

## Particle world

particle world
- a very simple agent-based model

### The story of particle world

#### Description

$p=30-31$

$acco$
==**torus**==
- donut-like surface
- topological structure to explain the fact that a field wraps around

$widec$
$down
$/widec$

toroidal grid / grid with ==**periodic boundaries**==
- if you move past the rightmost edge, you end up on the left
side, and if you move past the topmost edge, you end up at the bottom
- ~= Pac-Man

$info$
The grid is
toroidal rather than a true torus because each cell or patch is presumed to be a perfect square
with an area equal to that of all the other cells.
$/info$

$gallery port$
**Torus**

$widec$
![Image](img$qsqd)
$/widec$
$/gallery port$
$/acco$

$acco$
whimsiness
- extent to which individuals fail to stick to their current directional heading
- various cultural groups of PW exhibit varying levels of whimsiness
- opposite: stubbornness

$gallery port$
**Particle**

$widec$
![Image](img$vkog)
$/widec$

- The particle has position, (x, y), and a directional heading, θ.
- Its heading and position are updated on every time step.
$/gallery port$
$/acco$

$p=31$

$acco$
collision
- when two particles collide, they resume into a random direction
$/acco$

$p=32$

#### Research questions

$wide$
- article World physicians have become concerned about the long-term health consequences of these collisions.
- As such, they are particularly interested in **how often the collisions occur**. 
- Some regions of Particle World are more densely populated than others,
and they suspect that **higher densities lead to more collisions**. But **how many more**?
- Particle World scientists also know that individuals in some areas tend to be very whimsical,
while individuals in other areas are more stubborn. They wonder: **How does the whimsy of
a region affect the number of collisions observed in that region**?
$/wide$

### Coding the model

$p=35$

==**focal agent**==
- agent that we're focussing on at the moment

$p=39$

## The components of a model

models decompose reality
- simplified set of parts, properties and relationships
- not one 'right' way to decompose a system
	- decomposition is as valuable as its usefulness for explaining a phenomenon

$wide$
- $result keep asking: what are we assuming, and what are we excluding?
$/wide$

model descriptions
- should be very clear in answering question of $see $up
- clear statements about
	1. what the ==**parts**== and ==**properties**== of the model are
	2. how the model is ==**instantiated and initialized**==
	3. how the ==**dynamics**== of the model are scheduled
	4. how the ==**outcomes**== of the model simulations are ==**measured or computed**==

### Parts and properties

$wide$
- What is being represented, and what is the nature of that representation?
- If we are talking about an agent-based model, what are the agents like?
	- What properties do they have?
	- What behaviors do they exhibit?
	- If the agents interact, how are those interactions structured?
	- What is the nature of their environment, and what are its properties?
$/wide$

$wide$
**Particle world description**
$/wide$

|'real' world|model world|
|---|---|
|lush terrain|simple, flat and square terrain|

$p=40$

use of toroidal boundaries
- helps avoid...
	- ... **tricky artifacts** like agents getting stuck in the corners of the grid
	- ... **asymmetries** where agents near the edges have fewer spatial neighbors

model square size
- arbitrary!
- determines the meaning of things like speed and distance

$info$
In some models this unit may correspond to real lengths or distances. In NetLogo, this is the width of a patch.
$/info$

population size
- determines the population **density** (when model size is kept constant)

agent properties
- location
- directional heading
- => each agent will keep track of where it is and where it is heading

visualisations
- very useful to gain insight into the emergent effect of the simulation
- can help you gain intuition

### Initialisation

$wide$
- What’s going on when a model simulation **begins**?
- **How many agents** are there, and what are their properties?
- Where are they in their **environment** and in relation to each other?
- What does the **environment** look like?
$/wide$

initial conditions
- can be *very* important in non-linear dynamic systems
- nvda. $see chaos theory book (weather etc.)
- small variation can quickly be amplified!

$p=41$

$wide$
**Particle world description**
$/wide$

$reader$
At the beginning of a Particle World simulation, the spatial environment is established and the agents are placed upon it. Recall that agents have only two uniquely held
properties—location and heading—and so each agent will keep track of its own values for
these variables (NetLogo does this automatically for turtles). How should they be initially
assigned? There are lots of possibilities. For example, all the agents might start in the same
location, or be evenly spaced in a grid pattern, or be arranged in a circle, or in the shape of
a T-rex, or be placed on the grid in locations representing actual places in the real world.
Similar concerns apply to their directional headings. If we don’t have good reasons to choose
one of these, or if we have a good reason to think it doesn’t matter, we might as well draw
both locations and headings at random from a uniform distribution of choices, and this is
what we have done.
$/reader$

### Dynamics

----
$widec$
How does the state of the model system update from one moment to the next?
$/widec$
----

[ Types of time advancement ]
|continuous time|discrete time|
|---|---|
|modelled using mathematical formulations + differential equations|modelled using ABM|
|mathematical representation|computational representation|

discrete time
- 'ticks' / 'time steps'
- can represent units of time (second, day, year, generation ...)

$warn$
You should carefully consider the specifics of what happens during a time step and in
what order those things occur.
$/warn$

$widec$
$down
$/widec$

#### Scheduling 

==**scheduling**==
- the ordering of the computations performed during each time step
- can be consequential!

[ Types of response ]
|synchronous response|asynchronous response|
|---|---|
|all agents respond to the same environment at the same time|agents respond to the environment one at a time|

$warn$
The order in which agents are scheduled can matter, and it is usually wise to randomize the order in which agents are “stepped” at each tick.
$/warn$

$info$
Whether agents
respond synchronously [...] or asynchronously [...] can affect how the dynamics of the model unfold, though **the qualitative results of most models are usually robust to both styles of scheduling.**
$/info$

$result agent ordering
- the order in which agents execute actions

$p=42$

$result action ordering
- the order in which a single agent executes actions

$result interactions
- should all agents perform one action at a time?
- should each agent perform all actions, then move on to the next one?
- => /!\ different answers can lead to different outcomes!

#### Stopping conditions

stopping conditions
- conditions deciding when a simulation is considered finished

[ Types of stopping conditions (names nvda.) ]
|fixed stopping condition|dynamic stopping condition|
|---|---|
|simulation stops after fixed number of steps|simulation stops after a condition is met|
|number of steps should be **justified**!|condition should be **plausible**|

$widec$
(description of Particle World)
$/widec$

### Outcomes

quantifying model outcomes
- what are the outcome measures?
- can be counting (easy), or some sort of computation (harder)

$reader$
In the Particle World model, we are concerned with the number of collisions that occur
over the course of the simulation, as a function of both `whimsy` and `num-particles`.
$/reader$

$p=43$

## Describing a model

sharing a model
- you need to **describe** it well!
- a careful reader should be able to replicate your model solely based on your description

$info$
If a model is described poorly, the reader won’t be able to discern exactly how it works, and any results of the model’s analysis border on useless.
$/info$

### ODD protocol

ODD protocol
- used in ecology, but useful for modelling as wel!

$widec$
$down
$/widec$

$acco$
==Overview==
- 'story' of the model

==Design==
- computations involved in the model's dynamics

==Detail==
- all the model's algorithmic details
- sometimes relegated to an appendix
$/acco$

iterated description
- very useful!
- increasing detail given at each stage

$reader$
In order to make sense of how the model
details map onto the real-world system, it helps to explain the model system verbally. The
subsequently presented formal details can then be used to clarify how the model works
without requiring the reader to simultaneously figure out the underlying analogy to the real
world.
$/reader$

$p=44$

$reader$
**Particle World Description**

This model features a population of spatially embodied agents moving through continuous space, each using a correlated walk. When agents collide, they become
confused, and each sets off in a new direction. We run each model simulation for
10,000 time steps and compare the number of collisions during that time.

**Initialization**

A population of 𝑁 agents is initialized with each agent placed at a random real-valued
locations on an 𝐿 × 𝐿 grid with periodic boundaries. Each agent 𝑖 has a direction heading θ~𝑖~, which is initially chosen at random from a uniform distribution of integers
[0, 359]. Each agent is fully defined by its location and directional heading. Other
model parameters are the whimsy, 𝑤, which determines the turning angle agents use
on each time step, and the speed, 𝑠, which determines the size of the step they take
when moving. Finally, we keep track of the cumulative number of collisions over time,
𝐶(𝑡).

**Dynamics**

At each time step, each agent, in a random order, turns, moves, and collides.

1. An agent first _turns_ by adding to its direction heading an integer value that is randomly drawn
from a uniform distribution in [0, 𝑤]. The agent then subtracts a newly drawn value
from the same distribution from its directional heading. In other words, its new directional heading is θ~𝑖~ +ɛ, where ɛ is randomly drawn from a binomial distribution
bounded in [−𝑤, 𝑤].
2. The agent then moves 𝑠 units forward.
3. If there are any other agents with a position within one unit of the focal agent’s new location (defined by the Euclidean distance between the centers of each agent), a _collision_ occurs between the focal agent and all of these other nearby agents. In this case, all of the agents involved in the collision update their heading to a new value randomly selected from the uniform distribution [0, 359]. Each of the involved agents then moves forward 0.1 spatial
units in order to move away from the site of the collision and avoid cycles of perpetual collision. If a collision occurs, the cumulative collision counter 𝐶(𝑡) is incremented by one.
$/reader$

$p=44-45$

$reader$
(explanation on correlated random walk, reread again!)
$/reader$

$p=46$

## Flocking

$wide$
we adapt Particle World to include flocking -- this eliminates collisions!
$/wide$

$p=48$

## Reflections

play
- very valuable for becoming a competent modeller
- allows you to test the failure of modes -> solve novel problems in ways you might not otherwise have envisioned
	- no play? problems at a later satge!

$reader$
We can learn so much when we give ourselves license to
simply try things for the sake of trying them. Play is important even when coding artificial
worlds, partly because play helps you to develop stronger competence in turning your ideas
into reality. 
$/reader$

$p=49$

## Going deeper