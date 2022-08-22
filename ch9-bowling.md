DISTek Software Craftsmanship Club 09 - Bowling
===============================================

[Bowling kata on Coding Dojo](https://codingdojo.org/kata/Bowling)


_Clean Code_ Chapter 9: Unit Tests
----------------------------------
* Three Laws of TDD
  * You may not write production code until you have written a failing unit test.
  * You may not write more of a unit test than is sufficient to fail (and not compiling is failing).
  * You may not write more production code than is sufficient to pass the currently failing test.
* Keeping tests clean
  * Dirty tests worse than no tests
  * Test code is just as important as production code!
    * Tests enable the -ilities
      * Flexibility, maintainability, reusability
      * Without tests every change is a possible bug
* Clean tests
  * Readability is what makes tests clean!
  * "Build-Operate-Check" pattern
  * Domain-specific testing language
  * A dual standard
    * Test code has different standards than production code, but _it does have standards!_
* One assert per test
  * Single concept per test
    * Not necessarily one assert, strictly speaking, but one "thing" that is being tested
      (even if multiple asserts are necessary)
* F.I.R.S.T.
  * Fast
  * Independent
  * Repeatable
  * Self-validating (either pass or fail)
  * Timely (written _just before_ code to make them pass)


### Don't forget what you've already learned!

* [_Clean Code_ Chapter 8: "Boundaries"](ch8-rover-password.md)
* [_Clean Code_ Chapter 7: "Error Handling"](ch7-password-entry.md)
* [_Clean Code_ Chapter 6: "Objects & Data Structures"](ch6-passworddb.md)
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)


Bowling
-------
Create a program, which, given a valid sequence of rolls for one line of American Ten-Pin Bowling, produces the total
score for the game. Here are some things that the program will not do:

* We will not check for valid rolls.
* We will not check for correct number of rolls and frames.
* We will not provide scores for intermediate frames.
* Depending on the application, this might or might not be a valid way to define a complete story, but we do it here for 
  purposes of keeping the kata light. I think you’ll see that improvements like those above would go in readily if they
  were needed for real.

We can briefly summarize the scoring for this form of bowling:

* Each game, or “line” of bowling, includes ten turns, or “frames” for the bowler.
* In each frame, the bowler gets up to two tries to knock down all the pins.
* If in two tries, he fails to knock them all down, his score for that frame is the total number of pins knocked down in
  his two tries.
* If in two tries he knocks them all down, this is called a “spare” and his score for the frame is ten plus the number
  of pins knocked down on his next throw (in his next turn).
* If on his first try in the frame he knocks down all the pins, this is called a “strike”. His turn is over, and his
  score for the frame is ten plus the simple total of the pins knocked down in his next two rolls.
* If he gets a spare or strike in the last (tenth) frame, the bowler gets to throw one or two more bonus balls,
  respectively. These bonus throws are taken as part of the same turn. If the bonus throws knock down all the pins, the
  process does not repeat: the bonus throws are only used to calculate the score of the final frame.
* The game score is the total of all frame scores.

More info on the rules at: [How to ScoreGame for Bowling](http://www.topendsports.com/sport/tenpin/scoring.htm)

### Clues
What makes this game interesting to score is the lookahead in the scoring for strike and spare. At the time we throw a
strike or spare, we cannot calculate the frame score: we have to wait one or two frames to find out what the bonus is.

### Some Suggested (Final) Test Cases
Note that these test cases are not the unit test cases you need to write -- those should be written to cover each line
of code before you write it, as Robert Martin lays out in Chapter 9. These test cases just highlight some things you
want to account for in your code (but not everything, of course...).

(When scoring “X” indicates a strike, “/” indicates a spare, “-” indicates a miss)

* X X X X X X X X X X X X (12 rolls: 12 strikes) = 10 frames * 30 points = 300
* 9- 9- 9- 9- 9- 9- 9- 9- 9- 9- (20 rolls: 10 pairs of 9 and miss) = 10 frames * 9 points = 90
* 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/ 5/5 (21 rolls: 10 pairs of 5 and spare, with a final 5) = 10 frames * 15 points = 150