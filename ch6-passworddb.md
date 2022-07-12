DISTek Software Craftsmanship Club 06 - Password DB
===================================================

Coding Kata: [Mars Rover Kata on Katalyst](https://katalyst.codurance.com/mars-rover)


_Clean Code_ Chapter 6: Objects and Data Structures
---------------------------------------------------
* Data abstraction
* Data/object anti-symmetry
* The Law of Demeter
	* Train wrecks
	* Hybrids
	* Hiding Structure
* Data transfer objects
	* Active record


### Don't forget what you've already learned!
* [_Clean Code_ Chapter 5: "Formatting"](ch5-rover-refactor.md)
* [_Clean Code_ Chapter 4: "Comments"](ch4-rover-obstacles.md)
* [_Clean Code_ Chapter 3: "Functions"](ch3-rover.md)
* [_Clean Code_ Chapter 2: "Meaningful Names"](ch2-fizzbuzz.md)


Password DB Kata
----------------

Taking a slight detour from the `rover` project, in this kata we want to build a password database, that we will use in the future to get and set passwords. This will not be a strict relational database per se, but we do want to store the passwords in some sort of non-volatile storage so that we remember them on a power cycle (i.e., save them to a file).


### Separate project

We're going to write the Password DB as a separate project for now, so don't include it with your `rover` project. This means you'll probably need a new `main()` function (or whatever in Go) in this project as well.


### Passwords API

"Passwords" in this kata will be made up of a username + its associated password + some other associated data. The API will allow users to:

* Set a password for a given user (creating the user in the process, if they don't exist already),
* Test whether a given username and password match an entry that exists in the database,
* Get a list of users (but not their passwords!),
* Get the time the password was last changed, for a given user, and
* Delete a user, if the correct password for that user can be given.

Those APIs should look something roughly like this:

```c++
void SetPassword(username, newPassword);
bool TestPassword(username, passwordToTry);
string[] GetUsers(void);
Date GetLastPasswordChange(username);
void DeleteUser(username, passwordToTry);
```


### Password Records

The database should be made up of password records. The password record should be made up of:

* A username string,
* A password string,
* A timestamp ("Date") of the last time the password was updated.

The timestamp can be a string, an actual `Date` object (if you're in C#), the number of seconds since 1970, whatever you like -- so long as it is updated when the password is updated.

Take care whether you implement the aforementioned record as an Object or as a Data Structure! Either way is acceptable.

Also, feel free to implement the file format however you like. If you're looking for inspiration, you can always check out [how passwords work in Linux](https://www.computernetworkingnotes.com/linux-tutorials/etc-shadow-file-in-linux-explained-with-examples.html).


### Database File

Make sure you read existing password records combinations from the file at program startup, and create/update/delete them to the file whenever a creating/updating/deleting API is called.
