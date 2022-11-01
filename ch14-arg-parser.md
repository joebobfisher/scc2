DISTek Software Craftsmanship Club 14 - Command-Line Argument Parser
====================================================================
Coding Kata: this kata!

_Clean Code_ Chapter 14: Successive Refinement
----------------------------------------------
* Args implementation
  * How did I do this?
* Args: the rough draft
  * So I stopped
  * On incrementalism
* String arguments

### Don't forget what you've already learned!
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

Command-Line Argument Parser
----------------------------
Implement a parser of command-line arguments, similar to the parser that is discussed in the chapter.

The interface to the argument parser should ___roughly___ look like this below. Note that you should modify the
interface not just for your language, but based on your implementation's needs (i.e., this is just a guideline).

```java
public interface ArgParser {
    public ArgParser(String[] args);
    public int Cardinality();
    public String Usage();
    public boolean GetBoolean(char arg);
    public String GetString(char arg);
    public int GetInt(char arg);
    public double GetDouble(char arg);
    public boolean has(char arg);
};
```
