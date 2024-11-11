# What is `SIMPLE`?

The development of `SIMPLE` was motivated by the results of my [PhD Research](https://openaccess.wgtn.ac.nz/articles/thesis/Exploring_modelling_and_simulating_the_Feeling_of_Comfort_in_residential_settings/17085467/1).
In these studies, I investigated what is it that people—not building scientists
or architects or engineers—mean by and expect from *a comfortable home*. My finidings
revealed to me how little we know about human behaviour in buildings, compared to
building physics.

Building science has improved massively in recent years. On the one hand, windows, doors,
and construction materials have become better at keeping us comfortable and healthy;
and on the other hand, software has become more powerful, accessible, and easier to use.
This means two things. First, that keeping a window open or closed makes a big difference
in a building performance; and also, that we can predict and understand the physical
effects of said open (or closed) window better than ever... and yet, is this window open
or closed?

You see, buildings are made for people, and not understanding people means we do not
understand the performance of buildings. Understanding *when* and *why* people choose to open
windows requires tools that will let us properly research and evaluate human comfort
and behaviour.

While creating a tool for reseraching and evaluating human behaviour and comfort
was the origin of `SIMPLE`, the objectives of this project also include other factors
related to the modernization of building performance simulation. Let me ellaborate:

## We need holistic simulation tools

The reason for this is trivial: when people get into a room, they just
*feel* it. They do not separate—as Software and building scientists do—the
Thermal from the Daylight from the Acoustic domains. So,`SIMPLE` aims to enable
holistic Building Performance Simulation. Therefore, if we want to trully incorporate
people's behaviour and comfort, we need to account for multiple domains at the
same time, **at run time** (this means that running three simulations, one for
each domain and without considering the interaction between these domains,
is not enough).

Being able to do this will, also, let us optimize multi-domain control algorithms
that might lead to more optimal performance of buildings.

## We need to model human behaviour

People are not simple. They do not just say "it is cold, I will turn the heater on"
in a deterministic way. They take into account things like budget, bills, whether
they are alone (or they have kids, for instance) and more. Modelling this kind of
behaviour calls for a much more flexible way of modelling control algorithms (yes, I am
treating human behaviour as a control algorithm).

## We need to allow for more complex control algorithms

As hinted above, modelling human behaviour would let us model much more complex
building control algorithms. These can be stochastic, multi-domain, model-predictive-control
algorithms that aim to improve performance while maintaining an environment that people
will find acceptable.

## Programs no longer just run on your PC

`SIMPLE` is a modern tool, written in a modern language, and that can run in
multiple environments.

It can be easily compiled for Windows, Mac and Linux for running locally in your
computer. It can also be compiled into Web Assembly, which means that it can [run
on a browser](http://buildingsforpeople.org/simple_demo/) without the need for
servers. It can also be deployed in [very small and secure containers](https://github.com/GoogleContainerTools/distroless)
for running at scale on the cloud. It can probably (I have not tested this) be
compiled into a small computer and be implemented as an Energy Management System in
an actual building, providing insights on what the best strategy is.
