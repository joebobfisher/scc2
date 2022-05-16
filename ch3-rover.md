DISTek Software Craftsmanship Club 02 - Rover
=============================================

Coding Kata: [Simple Mars Rover Kata on Katalyst](https://katalyst.codurance.com/simple-mars-rover)

_Clean Code_ Chapter 3: Functions
---------------------------------
* Small!
  * Blocks and Indenting
    * Should be one line long
    * Indent level should not be greater than one or two.
* Do one thing
  * Functions that do one thing can't be divided into sections!
* One level of abstraction per function!
  * Reading code from top to bottom: the Stepdown Rule
    * Follow up a function with the functions in the next level of abstraction
* Switch statements
  * Encapsulate switch statements in Abstract Factories
    * Return the right polymorphic type that calls the right method
* Use descriptive names
  * Be consistent in your names!
* Function arguments
  * Priority of preference
    * Ideal: zero arguments ("niladic" function)
    * Next: one argument ("monadic" function)
    * Next: two arguments ("dyadic" function)
    * Three arguments ("triadic") or more should be avoided!
  * Common monadic forms
    * Return value
      * Asking a question about an argument and returning the answer
      * Operating on the argument and returning a result
    * No return value
      * Events: use input to alter state of system
    * Avoid monadic functions that don't follow these forms
  * Don't use flag arguments!
  * Dyadic functions
    * Sometimes appropriate, but not as often as you think!
      * E.g., cartesian point coordinates == appropriate
        * However, better would be a single object with two parts!
  * Again, triads are bad!
  * Argument objects
    * If you think you need more than 2 or 3, some may need to be wrapped in a class
    ```c++
    Circle makeCircle(double x, double y, double radius); // ok...
    Circle makeCircle(Point center, double radius); // Better!
    ```
  * Argument Lists
    * Functions that take multiple args that are the same sort of thing are often really monads or dyads.
    ```c++
    // this is actually dyadic!
    String.format("%s worked %.2f hours.", name, hours);
    public String format(String format, Object... args)     // equivalent definition
    ```
    ```c++
    void monad(Integer... args);
    void dyad(String name, Integer... args);
    void triad(String name, int count, Integer... args);
    ```
  * Verbs and keywords
    * Consider `writeField(name)` instead of `write(name)`.
    * Consider `assertExpectedEqualsActual(expected, actual)` instead of `assertEquals(expected, actual)`.
* Have no side effects
  * Output arguments
    * Avoid making readers do a double-take!
    * `report.appendFooter()` is better than `appendFooter(report)`.
* Command-Query separation
  * Functions should either do something or answer something, **not both**.
* Prefer exceptions to returning error codes!
  * Extract try/catch blocks
  * Error handling is One Thing
    * If `try` is in your function, it should be first thing and `catch/finally` block should be last!
* Don't Repeat Yourself (DRY)
* Structured Programming
  * Dijkstra: every block should have one entry & one exit!
  * This rule serves little benefit when functions are small though
    * Still no `goto`s tho.
* Start with "bad" functions, work your way towards "good"!

### Don't forget what you've already learned!
* [_Clean Code_ Chapter 2: "Meaningful Names"](../rover/README.md)

Rover Kata
----------
A squad of robotic rovers are to be landed by NASA on a plateau on Mars.

This plateau, which is curiously rectangular, must be navigated by the rovers so that their onboard cameras can get a complete view of the surrounding terrain to send back to Earth.

Your task is to develop an API that moves the rovers around on the plateau.

In this API, the plateau is represented as a 10x10 grid, and a rover has state consisting of two parts:

* its position on the grid (represented by an X,Y coordinate pair)
* the compass direction it's facing (represented by a letter, one of `N`, `S`, `E`, `W`)

### Input
The input to the program is a string of one-character move commands:

* `L` and `R` rotate the direction the rover is facing
* `M` moves the rover one grid square forward in the direction it is currently facing

If a rover reaches the end of the plateau, it wraps around the end of the grid.

### Output
The program's output is the final position of the rover after all the move commands have been executed. The position is represented as a coordinate pair and a direction, joined by colons to form a string. For example: a rover whose position is `2:3:W` is at square (2,3), facing west.

### Examples
* given an input `MMRMMLM` then the output should be `2:3:N`
* given an input `MMMMMMMMMM` gives output `0:0:N` (due to wrap-around)

### Interface
There are no restrictions on the design of the public interface.

A public interface to the API could look something like this:

```c++
public class MarsRover 
{
    public string Execute(string command);
}
```

### Rules
* The rover receives a char array of commands e.g. `RMMLM` and returns the finishing point after the moves e.g. `2:1:N`
* The rover wraps around if it reaches the end of the grid.
