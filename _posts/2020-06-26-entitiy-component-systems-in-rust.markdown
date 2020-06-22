---
layout: post
title:  "Entity Component Systems in Rust"
description: "Introduction to entity component systems in Rust"
tags: rust gamedev
date:   2020-06-26 09:00:00 +0100
---

In this tutorial, we will explore Entity Component Systems (ECS)
in Rust.

# What is an Entity Component System?

Entity Component Systems is an architectural design pattern that
favors composition over inheritance. The main difference between
these approaches is that inheritance tightly couples your classes
and objects. Makind changes to the parent class can often break
your sub-classes. Composition is loosely coupled, which means that
making changes is unlikely (or shouldn't) break any existing
functionality in the code that uses them. This makes it an ideal
approach for games development in particular.

# The problem with inheritance

Imagine you are designing your objects for a few animals. You might
create an `Animal` class, then have each type of animal inherit from
that.

```
class Animal
    .poop()

class Dog < Animal
    .bark()

class Duck < Animal
    .quack()
```

So the above code looks clean enough. Both the dog and the duck can poop,
they also can quak and bark. Changing the behaviour of pooping will be
reflected in both of our animals. A nice abstraction!

Now we want to introduce some dangerous animals that can kill. 

```
class Snake < Animal
    .kill()

class Lion < Animal
    .kill()

```

We have some duplication again, we don't want to add the kill functionality
to `Animal`, because we don't want our ducks to start killing things. So lets
create a `KillerAnimal` class.

```
class KillerAnimal < Animal
    .kill()

class Snake < KillerAnimal

class Lion < KillerAnimal
```

So now our Snake and Lion both inherit from `KillerAnimal`, which itself inherits
from `Animal`.

We then decide that it would be cool if the player could cast a spell that creates
a spirit like object of an animal. It needs to have all of the behaviour of it's
parent animal.

```
class SpiritLion < Lion
class SpiritDog < Dog
```

Except, we don't want our spirit animals to poop! But this has been inherited. We
obviously can just ignore this functionality, make it error or not return nil. But
this just feels like bad design.

# Composition






# Hello World ECS


