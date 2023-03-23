# OOP

## Overview

At its core OOP is the combination of encapsulation, polymorphism, and dynamic binding. In an OOP codebase, objects shouldn’t try to determine the concrete representation of the objects they interact with and instead interact with other objects solely through polymorphic interfaces. As part of this, state and primitive values are either absent or hidden inside of objects.

None of this depends on the presence or absence of classes. It’s very possible to write OOP code without classes, or to write imperative or non-OOP FP code using classes.

### React

I would say that React, in general, does not lean towards OOP. A large amount of state is global, not encapsulated inside of objects. Components are usually coupled to specific implementations of other components by name, not to interchangeable interfaces. Data is generally represented as trees of unencapsulated primitive values. One could make the argument that components can be OO because they conform to a shared interface, but I think this is outweighed by the anti-OO aspects of the system as a whole.

All that said: I have not used React in quite a while, so someone with a fresher memory may be able to contradict me.

## Access modifiers

PHP has three access modifiers: public, protected, and private.
