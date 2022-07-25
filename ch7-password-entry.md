DISTek Software Craftsmanship Club 07 - Passwords
=================================================

Kata: [This page!](ch7-password-entry.md)


_Clean Code_ Chapter 7: Error Handling
--------------------------------------
* Use exceptions rather than return codes
* Write your try-catch-finally statement first
* Use unchecked exceptions
* Provide context with exceptions
* Define exception classes in terms of a caller's needs
* Define the normal flow
* Don't return null
* Don't pass null


### Don't forget what you've already learned!

* [_Clean Code_ Chapter 6: "Objects & Data Structures"](ch6-passworddb.md)
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)


Passwords
---------

Add some rules to `SetPassword()` from the last kata, such that an error is thrown when the given password or username doesn't meet the Username and Password Rules (specified below).


### Username & Password Constraints

There are constraints on what the Username and password can contain. If any of these constraints are broken, when trying to add a new user or password (through `SetPassword()` -- again, that function should create a new user if the given user doesn't exist), an error should be thrown that tells the caller in what way the username or password is not acceptable.

It's OK to just throw the first error that is encountered (i.e., you don't need to try to throw multiple errors at the same time or any such nonsense).


#### Username Constraints

* Must be at least 3 characters long and no longer than 31 characters
* Must be alphanumeric only
* Must start with an alphabetic character


#### PasswordObject Constraints

* Must be between 8 and 255 characters long
* Must contain at least one:
  * lowercase alphabetic character
  * uppercase alphabetic character
  * digit
  * special character from the group:
    ```
    !@#$%^&*()-_=+
    ```
* Must not contain the Username, _regardless of case_


### Errors

#### Username Errors

Write an error for each of the above Username constraints. For example (you definitely don't need to use these exact
names for your errors):

* `UsernameTooShort`
* `UsernameTooLong`
* `UsernameBadCharacters`
* `UsernameStartsWithANumber`


#### PasswordObject Errors

Write an error for each of the above password constraints, e.g.:

* `PasswordTooShort`
* `PasswordTooLong`
* `PasswordBadCharacters`
* `PasswordNoLowerAlpha`
* `PasswordNoUpperAlpha`
* `PasswordNoDigit`
* `PasswordNoSpecialChar`
* `PasswordContainsUsername`


### Bonus Points If

These extra criteria are not at all required, and are only given as an extra challenge if the above kata was too easy,
or if you're one of those people who need to finish absolutely everything. 🤪

* You hash the password values in storage so they're not stored in plaintext.
* You create an interface where the Username and password can be given on the command line, with the password blanked 
  out or shown as `*`s when being typed in.
