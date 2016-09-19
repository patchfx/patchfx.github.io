---
layout: post
title:  "First Milestone Reached"
date:   2016-09-16 09:00:00 +0100
---
It's been two weeks since I wrote about the game I have been working on over the
summer. Last week I completed my first pre-alpha milestone. With much of the
core engine worked on over the summer, I have been able to focus solely on the
gameplay mechanics. Over the last fortnight I have completed 23
[trello](http://trello.com) tickets and now have a very basic run through of
placing an order through to fulfilment.

On the surface this seems very basic but under-the-hood there is quite a bit
going on. The engine is modeled around an Entity Component System, everything in
the game is an entity (a struct containing a UID) which has components attached
to it. Systems run every update loop, fetching entities containing the right set
of components that the system needs. A rendering system gets all entities that
have a position component and a sprite component, ignoring all other entities
that don't have those two components. I can make an object hidden by removing
one of those components.

The ordering system works in the same way, various components representing the
lifetime of an order are attached and removed depending on it's current state.
This causes animations to fire and various other behaviours. It's coming
together well and gives me a very flexible engine to work with when expanding
the gameplay further.

Here is a slightly laggy gif from the end of Milestone 1:
<img class="img-responsive" src="/assets/milestone_one_anim.gif" alt="">

The next milestone will start to flesh out the ordering process and fulfillment
some more with reputation, expertise and receiving money for a completed order.
I want to add some more items too, currently there is only one.

I would love any feedback on the above or any features you would like to see go
into this game!
