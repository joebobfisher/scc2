DISTek Software Craftsmanship Club 12 - Count k-Primes
======================================================
Coding Kata: [k-Primes](https://codwars.com/kata/5726f813c8dcebf5ed000a6b)

_Clean Code_ Chapter 12: Emergence
----------------------------------
* Getting clean via emergent design
* Simple Design Rule 1: Runs all the tests
* Simple Design Rule 2: No Duplication
* Simple Design Rule 3: Expressive
* Simple Design Rule 4: Minimal classes and methods

### Don't forget what you've already learned!
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

Counting k-Primes
-----------------
A natural number is called k-prime if it has exactly k prime factors, counted with multiplicity. For example:

```
k = 2  -->  4, 6, 9, 10, 14, 15, 21, 22, ... (i.e., 2*2, 2*3, 3*3, 2*5, 2*7, 3*5, 3*7, 2*11, ...)
k = 3  -->  8, 12, 18, 20, 27, 28, 30, ... (i.e., 2*2*2, 2*2*3, 2*3*3, 2*2*5, 3*3*3, 2*2*7, 2*3*5, ...)
k = 5  -->  32, 48, 72, 80, 108, 112, ... (i.e., 2*2*2*2*2, 2*2*2*2*3, 2*2*2*3*3, ...)
```

A natural number is thus prime if and only if it is 1-prime.

### Task
Complete the function, which is given parameters `k`, `start`, `end` (or `nd`) and returns an **array** (or a list or a
string depending on the language) of the k-primes between `start` (inclusive) and
`end` (inclusive).

### Example
```
countKprimes(5, 500, 600) --> [500, 520, 552, 567, 588, 592, 594]
```

### Notes
* The first function would have been better named: findKprimes or kPrimes :-)
* In C some helper functions are given.
* For Go: nil slice is expected when there are no k-primes between start and end.

Extra Credit: puzzle
--------------------
Given a positive integer `s`, find the total number of solutions of the equation `a + b + c = s`, where `a` is 1-prime,
`b` is 3-prime, and `c` is 7-prime.

Call this function `puzzle(s)`.

### Examples
```
puzzle(138)  -->  1  because [2 + 8 + 128] is the only solution
puzzle(143)  -->  2  because [3 + 12 + 128] and [7 + 8 + 128] are the solutions
```
