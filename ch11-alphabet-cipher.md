DISTek Software Craftsmanship Club 11 - Alphabet Cipher
=======================================================
Kata: [Alphabet Cipher on GitHub](https://github.com/mathias-brandewinder/wonderland-fsharp-katas/blob/master/wonderland-fsharp-katas/alphabet-cipher.md)

_Clean Code_ Chapter 11: Systems
--------------------------------
* How would you build a city?
* Separate constructing a system from using it
  * Separation of Main
  * Factories
  * Dependency Injection
* Scaling up
  * Cross-cutting concerns
* Java proxies
* Pure Java AOP frameworks
* AspectJ aspects
* Test-drive the system architecture
* Optimize decision-making
* Use standards wisely, when they add _demonstrable_ value
* Systems need domain-specific languages

### Don't forget what you've already learned!

* _Clean Code_ Chapter 10: "Classes"
* [_Clean Code_ Chapter 9: "Unit Tests"](ch9-bowling.md)
* [_Clean Code_ Chapter 8: "Boundaries"](ch8-rover-password.md)
* [_Clean Code_ Chapter 7: "Error Handling"](ch7-password-entry.md)
* [_Clean Code_ Chapter 6: "Objects & Data Structures"](ch6-passworddb.md)
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)

Alphabet Cipher
---------------
Lewis Carroll published a cipher known as The Alphabet Cipher.

This Alphabet Cipher involves alphabet substitution using a keyword.

First you must make a substitution chart like this, where each row of the alphabet is rotated by one as each letter goes down the chart.

```
  ABCDEFGHIJKLMNOPQRSTUVWXYZ
A abcdefghijklmnopqrstuvwxyz
B bcdefghijklmnopqrstuvwxyza
C cdefghijklmnopqrstuvwxyzab
D defghijklmnopqrstuvwxyzabc
E efghijklmnopqrstuvwxyzabcd
F fghijklmnopqrstuvwxyzabcde
G ghijklmnopqrstuvwxyzabcdef
H hijklmnopqrstuvwxyzabcdefg
I ijklmnopqrstuvwxyzabcdefgh
J jklmnopqrstuvwxyzabcdefghi
K klmnopqrstuvwxyzabcdefghij
L lmnopqrstuvwxyzabcdefghijk
M mnopqrstuvwxyzabcdefghijkl
N nopqrstuvwxyzabcdefghijklm
O opqrstuvwxyzabcdefghijklmn
P pqrstuvwxyzabcdefghijklmno
Q qrstuvwxyzabcdefghijklmnop
R rstuvwxyzabcdefghijklmnopq
S stuvwxyzabcdefghijklmnopqr
T tuvwxyzabcdefghijklmnopqrs
U uvwxyzabcdefghijklmnopqrst
V vwxyzabcdefghijklmnopqrstu
W wxyzabcdefghijklmnopqrstuv
X xyzabcdefghijklmnopqrstuvw
Y yzabcdefghijklmnopqrstuvwx
Z zabcdefghijklmnopqrstuvwxy
```

Both parties need to decide on a secret keyword. This keyword is not written down anywhere, but memorized.

To encode the message, first write down the message.

```
meetmebythetree
```

Then, write the keyword, (which in this case is scones), repeated as many times as necessary.

```
sconessconessco
meetmebythetree
```

Now you can look up the column S in the table and follow it down until it meets the M row. The value at the intersection is the letter e. All the letters would be thus encoded.

```
sconessconessco
meetmebythetree
egsgqwtahuiljgs
```

The encoded message is now `egsgqwtahuiljgs`

To decode, the person would use the secret keyword and do the opposite.
