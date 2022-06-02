DISTek Software Craftsmanship Club 03 - Rover Obstacles
=======================================================

Coding Kata: [Mars Rover Kata on Katalyst](https://katalyst.codurance.com/mars-rover)

_Clean Code_ Chapter 4: Comments
--------------------------------
* Comments do not make up for bad code
* Explain yourself in code
* Good comments
  * Legal comments
  * Informative comments
  * Explanation of intent
  * Clarification
  * Warning of consequences
  * TODO comments
  * Amplification
  * Javadocs in public APIs
* Bad comments
  * Mumbling
  * Redundant comments
  * Misleading comments
  * Mandated comments
  * Journal comments
  * Noise comments
  * Scary noise
  * Don't use a comment when you can use a function or a variable
  * Position markers
  * Closing brace comments
  * Attributions and bylines
  * Commented-out code
  * HTML comments
  * Nonlocal information
  * Too much information
  * Inobvious connection
  * Function headers
  * Javadocs in nonpublic code

### Don't forget what you've already learned!
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)

Rover Obstacles Kata
--------------------

This is a continuation of the [rover kata we did in the last chapter](ch3-rover.md), except now we're adding a new twist: obstacles!

### Obstacles

The grid may have obstacles. If a given sequence of commands encounters an obstacle, the rover moves up to the last possible point and reports the obstacle by prefixing `O:` (capital O, not zero) to the position string that it returns. For instance, `O:1:1:N` would mean that the rover encountered an obstacle at position (1, 2).

#### Example

* given a grid with no obstacles, input `MMRMMLM` gives output `2:3:N`
* given a grid with no obstacles, input `MMMMMMMMMM` gives output `0:0:N` (due to wrap-around)
* given a grid with an obstacle at (0, 3), input `MMMM` gives output `O:0:2:N`

