# Chaos: making a new science

$public=true$

## The Butterfly Effect

$p=16$

Lorenz middle run
- when the weather simulation run is paused, and a new run is started from the middle conditions, we get a **new pattern**
- due to a **rounding error**

$widec$
$down
$/widec$

$p=8$

$result ==sensitive dependence on initial conditions==
- **tiny differences in input** can lead to **big differences in output**

$p=15$

$widec$
$contrast
$/widec$

Western science
- general belief that **approximations are OK**
- "probably do not influence output too much"

$p=17$
$gallery port$
$widec$
![Image](img$exha)
$/widec$

From nearly the same starting point, Edward Lorenz saw his
computer weather produce **patterns that grew farther and farther apart** until all resemblance disappeared.


(From Lorenz’s 1961 printouts)
$/gallery port$

$p=20$

$widec$
$down
$/widec$

==Butterfly effect==
- errors and uncertainties multiply, cascading upward through a chain of turbulent features
- => cause larger-scale effects which cannot be predicted (nvda.)

$p=22$

$widec$
$down ~=
$/widec$

==aperiodic system==
- a system that never finds a steady state
- can almost repeat themselves, but never quite

$example$
**Examples of aperiodic systems**

- weather
- animal populations
- epidemics

$info$
If the weather ever did reach a state exactly like one it had
reached before, every gust and cloud the same, then presumably it would
repeat itself forever after and the problem of forecasting would become
trivial.
$/info$
$/example$

$p=23$

----

chaos from a deterministic system
- Lorenz was able to mimic _aperiodicity_ and _sensitive dependence on initial conditions_ with a **simple deterministic program**

## Revolution

$p=38$

graphic images are key
- needed for interpretation of chaos theories

----

$p=46$

differential equations
- describe the way systems change continuously over time

$widec$
$down allow for
$/widec$

$p=47$

parameters at the start
- large changes in parameters can make large differences in a system
- e.g. the difference between arriving at a steady state and oscillating periodically
- but: physicists assumed that very small changes would cause only very small differences in numbers, *not* qualitative changes in behaviour

$widec$
$down therefore ...
$/widec$

$acco$
topology and dynamical systems
- the possibility of using a shape to help visualise the whole range of behaviours of a system
- simple system: curved surface
- complicated system: manifold of many dimensions

$gallery$
![Image](img$r7iy)

$widec$
these are loss surfaces, but the idea is the same
$/widec$
$/gallery$
$/acco$

|Stale's stability|any chaotic system|
|---|---|
|a system can behave erratically, but the **erratic behaviour cannot be *stable***|a system which can have **chaos and stability at once**|
|stable behaviour that does not disappear just because some number was changed a tiny bit<br>$down<br>strangeness does not go away when perturbed by noise||

$info$
The difference is that Smale assumed that behaviour we see in the real world is actually stable, since real life has many disturbances and noise. In reality, systems are chaotic by definition, since *stable* systems would be those that are disturbed by tiny differences. It is a philosophical discussion, in that sense.
$/info$

$p=59$

## Life's Ups and Downs

ecology
- theoretical branch of biology that treats populations as dynamical systems

$p=60$

models as 'caricatures'
- 'soft' sciences of reality
- 'difficult' to deduce equations
	- necessary to 'idealise' these questions
- => **models as 'suggestions for real-life behaviour'**

$p=61$

discrete time intervals
- helpful for modelling the world
- <-> differential equations: smooth changes over time

feedback loop function
- result for next x is applied to previous **y** ($todo)
- so: $x_\text{next} = F(x)$

$info$
Feedback can get out of hand, as it does when sound from a loudspeaker feeds back through a microphone and is rapidly amplified to an unbearable shriek. Or feedback can produce stability, as a thermostat does in regulating the temperature of a house: any temperature above a fixed point leads to cooling, and any temperature below it leads to heating.
$/info$

$p=62$

adding realism
- you need more terms
- not just percentage increase of a population
- for ecology: growth rate, natural death rate, starvation / predation death rate ...
- => give rise to intricate and complex functions

$p=63$

logistic equation
- $x_\text{next} = rx(1 - x)$

$p=64$

$gallery port$
$widec$
![Image](img$70k3)
$/widec$

$widec$
a population reaches equilibrium after rising, overshooting, and falling back
$/widec$
$/gallery port$

erratic behaviour
- 'must be due to model's faults' -> 'the calculator must be acting up'
- stable solutions were the interesting ones

$p=68$

supremacy of chaos
- chaos is not a footnote on a physics textbook
- "the first message is that there is disorder" - Yorke

$p=71$

==bifurcation diagram==
- shows parameter on x, final population on y
- if system starts to oscillate, these oscillations are shown in the diagram! ($see $down)

$gallery port$
$widec$
![Image](img$25z8)
$/widec$
$/gallery port$

$p=73$

chaos region
- beyond a specific point, the bifurcation breaks down and gives way to chaos
- but: regularity of periodicity *can* return

$widec$
$down thus...

**chaos is also regular**

$down

regularity - chaos - regularity - chaos ...
$/widec$

$reader$
**In the real world, a researcher sees only a single point**, with no knowledge of the dynamics of the system. He would only see one kind of behaviour -- possibly a steady state, possibly a seven-year cycle, possibly apparent randomness. He would have **no way of knowing** that the same system, with some slight change in some parameter, **could display patterns of a completely different kind**.
$/reader$

$reader$
In any one-dimensional system, if a regular cycle of period three ever appears, the same system will also display regular cycles of every other length, as well as completely chaotic cycles.

\- James Yorke
$/reader$

$p=78$

$gallery port$
$widec$
![Image](img$420i)
$/widec$

$widec$
The outline of the bifurcation diagram as May first saw it, before more powerful computation revealed its
rich structure.
$/widec$
$/gallery port$

$p=93$

## A Geometry of nature

### Cantor sets

cantor set
- a set of points lying on a single line segment, arranged in clusters
- infinitely many, with a total length of zero

$gallery port$
**Cantor dust**

$widec$
![Image](img$vchm)
$/widec$

Begin with a line; remove the middle third; then remove the middle third of the
remaining segments; and so on. The Cantor set is the dust of points that remains. They are infinitely many,
but their total length is 0.
$/gallery port$

$info$
Mandelbrot saw the Cantor set as a model for the occurrence of errors in an electronic transmission line.
Engineers saw periods of error-free transmission, mixed with periods when errors would come in bursts.
Looked at more closely, the bursts, too, contained error-free periods within them. And so on—it was an
example of fractal time. At every time scale, from hours to seconds, Mandelbrot discovered that the
relationship of errors to clean transmission remained constant. Such dusts, he contended, are
indispensable in modeling intermittency.
$/info$

$p=98$

### Fractals

fractal
- 'a way of seeing infinity'
- continuous shape that can be enlarged infinitely
- as such, has a total circumference of $\infty$

$p=95$

$gallery port$
**A fractal shore**

$widec$
![Image](img$kwf5)
$/widec$

A computer-generated coastline: the details are random, but the fractal dimension is
constant, so the degree of roughness or irregularity looks the same no matter how much the image is
magnified.
$/gallery port$

$p=107$

### Scaling

$reader$
How big is it? How long does it last? These are the most basic questions a
scientist can ask about a thing. They are so basic to the way people
conceptualize the world that it is not easy to see that they imply a certain
bias. They suggest that size and duration, qualities that depend on scale, are
qualities with meaning, qualities that can help describe an object or classify
it. When a biologist describes a human being, or a physicist describes a quark,
how big and how long are indeed appropriate questions. In their gross physical
structure, animals are very much tied to a particular scale. Imagine a human
being scaled up to twice its size, keeping all proportions the same, and you
imagine a structure whose bones will collapse under its weight. Scale is important.

The physics of earthquake behavior is mostly **independent of scale**. A
**large earthquake is just a scaled-up version of a small earthquake**. That
distinguishes earthquakes from animals, for example—a ten-inch animal
must be structured quite differently from a one-inch animal, and a hundred-inch 
animal needs a different architecture still, if its bones are not to snap
under the increased mass. Clouds, on the other hand, are **scaling phenomena**
like earthquakes. Their characteristic irregularity—describable in terms of
fractal dimension—changes not at all as they are observed on different scales.
That is why air travelers lose all perspective on how far away a cloud is.
Without help from cues such as haziness, a cloud twenty feet away can be
indistinguishable from two thousand feet away. Indeed, analysis of satellite
pictures has shown an **invariant fractal dimension in clouds observed from
hundreds of miles away**.
$/reader$

$gallery port$
$widec$
![Image](img$qg8j)
$/widec$
$/gallery port$

scaling phenomena
- phenomena which are independent of scale
- e.g. clouds -> do not have a reference scale, can appear at any scale

$p=108$

$widec$
$down
$/widec$

claim of fractal geometry
- for some elements of nature, looking for a characteristic scale becomes a distraction

## Strange attractors

$p=122$

### Turbulence

turbulence
- a mess of disorder at all scales
- small eddies [(draaikolken)] within larger ones
- unstable, dissipative, random motion

$gallery port$
$widec$
![Image](img$obsw)
$/widec$

$widec$
(picture from [The Constructor](https://theconstructor.org/fluid-mechanics/laminar-turbulent-flow/559432/))
$/widec$
$/gallery port$

$reader$
All the rules seem to break down. When flow is smooth, or laminar,
small disturbances die out. But past the onset of turbulence, disturbances
grow catastrophically.

$info$
Think for example of when you pour water in a glass. If you do it slowly, the glass is filled in an 'undisturbed' way. However, when you really pour in the water, you get a turbulent flow of water where water molecules are scattered around violently.
$/info$
$/reader$

$p=129$

$gallery port$
**Flow between rotating cylinders**

$widec$
![Image](img$y9v7)
$/widec$

The patterned flow of water between two cylinders gave Harry
Swinney and Jerry Gollub a way to look at the onset of turbulence. As the rate of spin is increased, the
structure grows more complex. First the water forms a characteristic pattern of flow resembling stacked
doughnuts. Then the doughnuts begin to ripple. The physicists used a laser to measure the water’s
changing velocity as each new instability appeared.
$/gallery port$

### Strange attractors

$p=134$

==phase space==
- shows the **complete state of knowledge about a dynamical system at a single instant in time, collapsed to a point**
- if the system changes, so will the point in the phase space
- => history of the system time can be charted by the moving point

$example$
**Pendulum**

In [this video](https://www.youtube.com/watch?v=_L0aHxhdeYE), pendulum movement is shown with 𝑣 = velocity and θ = angle. The ground plane shows the phase space.

However, if we add realism ([friction](https://www.youtube.com/watch?v=MwKoGa8A5UQ)), both the angle and velocity will converge towards zero, which means the centre point of the ground plane is an 'attractor'.
$/example$

$p=135$

utility of phase space
- easy to watch change -> a system becomes a **moving point**
- some combination of variables never present? not part of the system
- periodic system => phase space as a loop

multi-dimensional phase spaces
- every piece of a dynamical system that can move independently is **another variable**

$p=138$

----

periodic attractor / limit cycle
- an orbit that attracts all other nearby orbits

$p=139$

non-periodic phase space
- orbit drawn in a limited space which **does not repeat nor cross itself**
- => must be **fractal**

$gallery port$
$widec$
![Image](img$1dqt)
$/widec$
$/gallery port$

$p=142$

Poincaré map / return map
- removes a dimension from an attractor
- => turns continuous line into a collection of points

$gallery port$
**Exposing an attractor's structure**

$widec$
![Image](img$83j7)
$/widec$

The strange attractor above—first one orbit, then ten, then one
hundred—depicts the chaotic behavior of a rotor, a pendulum swinging through a full circle, driven by an
energetic kick at regular intervals. By the time 1,000 orbits have been drawn (below), the attractor has
become an impenetrably tangled skein.
To see the structure within, a computer can take a slice through an attractor, a so-called Poincaré
section. The technique reduces a three-dimensional picture to two dimensions. Each time the trajectory
passes through a plane, it marks a point, and gradually a minutely detailed pattern emerges. This example
has more than 8,000 points, each standing for a full orbit around the attractor. In effect, the system is
“sampled” at regular intervals. One kind of information is lost; another is brought out in high relief.

$info$
As far as I can tell, the strange attractor is not a single point as with the pendulum example. Rather, it is a multidimensional phenomenon.
$/info$

$widec$
[visualisation app](https://yoursamlan.github.io/lavis/)
$/widec$
$/gallery port$

$p=146$

$reader$
Hénon found that the oversimplification paid off. By abstracting only the essence of his system, he made discoveries that applied to other systems as well, and more important systems.
$/reader$

$p=149$

Hénon equation
- $x_\text{new} = y + 1 - 1.4 x^2$
- $y_\text{new} = 0.3 x$
- describes the point of attraction for a Hénon strange attractor
- starting point does not matter!

$p=150$

attractor
- shows **trajectory toward which all other trajectories converge**

$info$
This is why the starting conditions do not matter: as long as the starting point lies somewhere near the attractor, the next few points will converge to the attractor with great rapidity.
$/info$

$p=151$

$gallery port$
**The attractor of Hénon**

$widec$
![Image](img$ma3n)
$/widec$

A simple combination of folding and stretching produced an attractor that
easy to compute yet still poorly understood by mathematicians. As thousands, the millions of points
appear, more and more detail emerges. What appear to be single lines prove, on magnification, to be pairs,
then pairs of pairs. Yet whether any two successive points appear nearby or far apart is unpredictable.
$/gallery port$

$p=161$

## Universality

$acco$
universality
- idea that **different problems follow the same basic principles**
- i.e. boiling of liquids ~= magnetising of metals ...
$/acco$

$p=169$

$acco$
intransitive system
- a system with multiple equilibria
- can stay in one equilibrium or another, but not both at the same time

$reader$
An observer might see one kind of behavior over a very long time, yet a completely different kind of behavior could be just as natural for the system.
$/reader$

$example$
**Clock example**

In a trivial way, **a
standard pendulum clock is an intransitive system**. A steady flow of energy
comes in from a wind-up spring or a battery through an escapement
mechanism. A steady flow of energy is drained out by friction. **The obvious
equilibrium state is a regular swinging motion**. If a passerby bumps the clock,
the pendulum might speed up or slow down from the momentary jolt but will
quickly return to its equilibrium. But **the clock has a second equilibrium as
well**—a second valid solution to its equations of motion—and that is **the state
in which the pendulum is hanging straight down and not moving**. 
$/example$
$/acco$

$p=170$

$acco$
almost-intransistive system
- system displays **one sort average behaviour for a very long time, fluctuating within certain bounds**
- then: **shifts into a _different_ sort of behaviour**, still **fluctuating but producing a different average**
$/acco$

|intransitive system|almost-intransitive system|
|---|---|
|multiple equilibria (*attractors*) are possible, but change lies in parameters|multiple equilibria are possible within the same parameter settings|

$reader$
An intransitive system is characterized by two or more mutually coexisting attractors. Which attractor will be traversed is determined by the initial state of the system. In contrast, the long-term dynamical characteristics of transitive systems are not affected by the initial state as there is only one attractor.

[Intransitive Atmosphere Dynamics Leading to Persistent Hot–Dry or Cold–Wet European Summers, _Journal of Climate_](https://journals.ametsoc.org/view/journals/clim/34/15/JCLI-D-20-0943.1.xml)
$/reader$

$p=180$

$reader$
**Universality theory**

Universality offered the hope that **by solving an easy problem
physicists could solve much harder problems**.
$/reader$

$wide$
- $result means different systems **behave identically**
$/wide$

$p=186$

$reader$
It’s not an academic question any more to ask what’s going to happen
to a cloud. People very much want to know—and that means there’s money
available for it. That problem is very much within the realm of physics and
it’s a problem very much of the same caliber. **You’re looking at something
complicated, and the present way of solving it is to try to look at as many
points as you can, enough stuff to say where the cloud is, where the warm air
is, what its velocity is, and so forth. Then you stick it into the biggest
machine you can afford and you try to get an estimate of what it’s going to do
next. But this is not very realistic**.

\- Feigenbaum

$info$
This also echoes the FCG arguments by Katrien Beuls and Paul Van Eecke on language acquisition and language models. Fair enough.
$/info$
$/reader$

$p=187$

$reader$
I truly do want to know how to describe clouds. But to say there’s a
piece over here with that much density, and next to it a piece with this much
density—to accumulate that much detailed information, I think is wrong. It’s
certainly not how a human being perceives those things, and it’s not how an
artist perceives them. Somewhere the business of writing down partial
differential equations is not to have done the work on the problem.

\- Feigenbaum
$/reader$

$p=194$

## The Experimenter

non-linearity
- can a **defence against noise**
- chaotic systems can be **robust** and return to their **trajectory or attractor**
- <-> linear system: each perturbation immediately has effect 

turbulence onset
- NOT piling up of frequencies
- => *sudden* transition

$widec$
$down
$/widec$

$p=203$

very small change in temperature
- causes perturbations!
- ~= very small change in values of $see $up

$p=206$

$gallery$
**Another view into bifurcation**

![Image](img$51qt)

When an experiment like Libchaber’s convection cell produces a
steady oscillation, its phase-space portrait is a loop, repeating itself at regular intervals (top left). An
experimenter measuring the frequencies in the data will see a spectrum diagram with a strong spike for
this single rhythm. After a period-doubling bifurcation, the system loops twice before repeating itself
exactly (center), and now the experimenter sees a new rhythm at half the frequency—twice the period—of
the original. New period-doublings fill in the spectrum diagram with more spikes.
$/gallery$

bifurcation and looping systems
- no moving towards a single goal

$p=209$

'era of computer experimentation'
- faster and more reliable

$p=210$

$reader$
The modifications, the compromises, the approximations
needed to digitize systems of nonlinear differential equations were too
suspect. **Simulations break reality into chunks, as many as possible but
always too few.** A computer model is just a set of arbitrary rules, chosen by
programmers.
$/reader$

$reader$
Whenever a good physicist examines a
simulation, he must wonder **what bit of reality was left out, what potential
surprise was sidestepped**. Libchaber liked to say that he would not want to fly
in a simulated airplane—he would wonder what had been missed.
Furthermore, he would say that **computer simulations help to build intuition
or to refine calculations, but they do not give birth to genuine discovery**.
$/reader$

$p=221$

## Images of Chaos

$gallery$
**An assortment of Julia sets**

![Image](img$3zi4)
$/gallery$

Julia set
- values such that an arbitrarily small perturbation can cause drastic changes in the sequence of iterated function values (Wikipedia)

$p=227$

Mandelbrot set calculation
- $z -> z^2 + c$

$p=233-234$

$reader$
**Pinball analogy**

Like most pinball machines it has a plunger with a spring. You pull back the
plunger and release it to send the ball up into the playing area. The machine
has the customary tilted landscape of rubber edges and electric bouncers that
give the ball a kick of extra energy. The kick is important: it means that
energy does not just decay smoothly. For simplicity’s sake this machine has
no flippers at the bottom, just two exit ramps. The ball must leave by one
ramp or the other.

This is deterministic pinball—no shaking the machine. Only one
parameter controls the ball’s destination, and that is the initial position of
the plunger. Imagine that the machine is laid out so that a short pull of the
plunger always means that the ball will end up rolling out the right-hand
ramp, while a long pull always means that the ball will finish in the left-hand
ramp. In between, the behavior gets complex, with the ball bouncing from
bumper to bumper in the usual energetic, noisy, and variably long-lived
manner before finally choosing one exit or the other.

Now imagine making a graph of the result of each possible starting
position of the plunger. The graph is just a line. If a position leads to a righthand departure, plot a red point, and plot a green point for left. What can we
expect to find about these attractors as a function of the initial position?
The boundary proves to be a fractal set, not necessarily self-similar, but
infinitely detailed. Some regions of the line will be pure red or green, while
others, when magnified, will show new regions of red within the green, or
green within the red. For some plunger positions, that is, a tiny change
makes no difference. But for others, even an arbitrarily small change will
make the difference between red and green.

To add a second dimension meant adding a second parameter, a second
degree of freedom. With a pinball machine, for example, one might consider
the effect of changing the tilt of the playing slope. One would discover a kind
of in-and–out complexity that would give nightmares to engineers
responsible for controlling the stability of sensitive, energetic real systems
with more than one parameter—electrical power grids, for example, and
nuclear generating plants, both of which became targets of chaos-inspired
research in the 1980s. For one value of parameter A, parameter B might
produce a reassuring, orderly kind of behavior, with coherent regions of
stability. Engineers could make studies and graphs of exactly the kind their
linear-oriented training suggested. Yet lurking nearby might be another
value of parameter A that transforms the importance of parameter B.
$/reader$

$p=235$

$reader$
**A warning about complex behaviour**

To researchers and engineers, there was a lesson in these pictures—a
lesson and a warning. Too often, **the potential range of behavior of complex
systems had to be guessed from a small set of data**. When a system **worked
normally, staying within a narrow range of parameters, engineers made their
observations and hoped that they could extrapolate more or less linearly to
less usual behavior**. But scientists studying fractal basin boundaries showed
that **the border between calm and catastrophe could be far more complex
than anyone had dreamed**. “The whole electrical power grid of the East Coast
is an oscillatory system, most of the time stable, and you’d like to know what
happens when you perturb it,” Yorke said. “You need to know what the
boundary is. The fact is, **they have no idea what the boundary looks like**.”
$/reader$

$p=236$

Barnsley chaos game
- looks like a proto Game Of Life

$p=238-239$

limited set of rules could create an infinitely complex shape
- useful in nature!
- not needed to encode a lot of information

$p=258$

## The Dynamical Systems Collective

strange attractors
- create **unpredictability**, as as such, **raise entropy**

$p=266$

$wide$
"orderly disorder created by simple processes"
$/wide$

$p=273$

## Inner Rhythms

$p=278$

$reader$
What’s actually the case is that, **as physicians or scientists learning all
50,000 parts of everything, we resent the possibility that there are in fact
universal elements of motion**. And Bernardo comes up with one and look
what happens.
$/reader$

$p=278-279$

$reader$
The choice is always the same. **You can make your model more complex
and more faithful to reality, or you can make it simpler and easier to handle.**
**Only the most naïve scientist believes that the perfect model is the one that
perfectly represents reality. Such a model would have the same drawbacks as
a map as large and detailed as the city it represents**, a map depicting every
park, every street, every building, every tree, every pothole, every
inhabitant, and every map. Were such a map possible, its specificity would
defeat **its purpose: to generalize and abstract**. Mapmakers highlight such
features as their clients choose. Whatever their purpose, **maps and models
must simplify as much as they mimic the world**.
$/reader$

$p=301$

## Chaos and Beyond

$p=305$

$wide$
"universal laws guding the behaviour of feedback functions"
$/wide$

$p=321$

$book Dynamics Of Complex Systems
- book!