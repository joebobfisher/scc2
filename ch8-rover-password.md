DISTek Software Craftsmanship Club 08 - Rover Passwords
=======================================================

Kata: [This page!](ch8-rover-password.md)


_Clean Code_ Chapter 8: Boundaries
----------------------------------
* Using third-party code
  * Encapsulate extra functionality you don't need/want in a class
    * E.g., "Sensors" HashMap
* Exploring & learning boundaries
  * Use "learning tests" to discover boundaries in 3rd-party code
  * E.g., learning `log4j`
* Learning tests are better than free
  * We have to learn API anyway, and now we have regression tests for that library!
* Using code that does not yet exist
  * Define your own interfaces and stub out implementations for later
* Don't let too much of your codebase rely on 3rd-party stuff
  * Then a lot has to change if those libraries change!
  * Encapsulate into a thing _you_ control.


### Don't forget what you've already learned!

* [_Clean Code_ Chapter 7: "Error Handling"](ch7-password-entry.md)
* [_Clean Code_ Chapter 6: "Objects & Data Structures"](ch6-passworddb.md)
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)


Rover Passwords
---------------
Integrate your password code into your rover app!

We want our rover to ask for a username and password before running any commands
given to it. To do this, incorporate the password database functionality you
developed over the last couple of katas. You can pick any username and password
combination, but the rover should utilize your password API to check it, and
only execute the commands if the given username and password checks out.

Encapsulate the APIs you're using so that they are not affected by other changes
to the password module in the future.