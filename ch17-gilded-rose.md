DISTek Software Craftsmanship Club 17 - Gilded Rose Kata
========================================================
Coding Kata: [Gilded Rose Kata on GitHub](https://github.com/joebobfisher/GildedRose-Refactoring-Kata)

_Clean Code_ Chapter 17: Smells and Heuristics
----------------------------------------------
* Comments
  * C1: Inappropriate information
  * C2: Obsolete comment
  * C3: Redundant comment
  * C4: Poorly written comment
  * C5: Commented-out code
* Environment
  * E1: Build requires more than one step
  * E2: Tests require more than one step
* Functions
  * F1: Too many arguments
  * F2: Output arguments
  * F3: Flag arguments
  * F4: Dead function
* General
  * G1: Multiple languages in one source file
  * G2: Obvious behavior is unimplemented
  * G3: Incorrect behavior is unimplemented
  * G4: Overridden safeties
  * G5: Duplication
  * G6: Code at wrong level of abstraction
  * G7: Base classes depending on their derivatives
  * G8: Too much information
  * G9: Dead code
  * G10: Vertical separation
  * G11: Inconsistency
  * G12: Clutter
  * G13: Artificial coupling
  * G14: Feature envy
  * G15: Selector arguments
  * G16: Obscured intent
  * G17: Misplaced responsibility
  * G18: Inappropriate static
  * G19: Use explanatory variables
  * G20: Function names should say what they do
  * G21: Understand the algorithm
  * G22: Make logical dependencies physical
  * G23: Prefer polymorphism to if/else or switch/case
  * G24: Follow standard conventions
  * G25: Replace magic numbers with named constants
  * G26: Be precise
  * G27: Structure over convention
  * G28: Encapsulate conditionals
  * G29: Avoid negative conditionals
  * G30: Functions should do one thing
  * G31: Hidden temporal couplings
  * G32: Don't be arbitrary
  * G33: Encapsulate boundary conditions
  * G34: Functions should descend only one level of abstraction
  * G35: Keep configurable data at high levels
  * G36: Avoid transitive navigation
* Java
  * J1: Avoid long import lists by using wildcards
  * J2: Don't inherit constants
  * J3: Constants vs. enums
* Names
  * N1: Choose descriptive names
  * N2: Choose names at the appropriate level of abstraction
  * N3: Use standard nomenclature where possible
  * N4: Unambiguous names
  * N5: Use long names for long scopes
  * N6: Avoid encodings
  * N7: Names should describe side effects
* Tests
  * T1: Insufficient tests
  * T2: Use a coverage tool!
  * T3: Don't skip trivial tests
  * T4: An ignored test is a question about an ambiguity
  * T5: Test boundary conditions
  * T6: Exhaustively test near bugs
  * T7: Patterns of failure are revealing
  * T8: Test coverage patters can be revealing
  * T9: Tests should be fast

### Don't forget what you've already learned!
* [_Clean_Code_ Chapter 14: "Successive Refinement"](ch14-arg-parser.md)
* [_Clean Code_ Chapter 13: "Concurrency"](ch13-kprimes-concurrent.md)
* [_Clean Code_ Chapter 12: "Emergence"](ch12-kprimes.md)
* [_Clean Code_ Chapter 11: "Systems"](ch11-alphabet-cipher.md)
* _Clean Code_ Chapter 10: "Classes"
* [_Clean Code_ Chapter 9: "Unit Tests"](ch9-bowling.md)
* [_Clean Code_ Chapter 8: "Boundaries"](ch8-rover-password.md)
* [_Clean Code_ Chapter 7: "Error Handling"](ch7-password-entry.md)
* [_Clean Code_ Chapter 6: "Objects & Data Structures"](ch6-passworddb.md)
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)

The Gilded Rose Kata
--------------------
Instead of refactoring the rover project one more time, we're going to switch things up a bit. This kata is designed to
force you to deal with test and design decisions as you refactor somebody else's _admittedly messy_ code. See the kata
link above for details! However, when you attack this kata, try to place a heavy emphasis on:

1) The smells and heuristics that Robert Martin lays out in Chapter 17, and
2) what you've already learned in the previous chapters

Make sure you choose the folder containing the code for your language (or if you're feeling really adventurous, try a
new one!).

Finally, for this kata, the total progress is not what's important (there is no "done refactoring"), rather it's the
experience that counts. See the below section for more on the experience we want to have in this last kata, together.

### Important Twist

We're going to attack this kata a little differently than the ones we've done in the past sessions. Instead of meeting
together to review each other's work, I strongly urge you to start with a partner in true pairing style! That is, try
working on this kata _synchronously_ with a partner (i.e. at the same time), and trade off who write code on the
keyboard and who "navigates" or provides direction (talking through the problem with the driver). 

Hop on Gather in a separate room, or use Visual Studio Code's LiveShare feature, etc. If you can make this happen, even
just to _start_ working through the kata, please do so -- you won't regret the experience, even if it seems a bit
awkward at first!

The End
-------
You did it! You made it to the end of the book! Congrats, and keep practicing what you've learned both in your
professional and personal code -- code craftsmanship takes a lifetime to master.
