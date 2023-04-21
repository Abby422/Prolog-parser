# Prolog Parser

This is a simple prolog parser that was created using jacc, a parser generator for Java. The parser can check if a given prolog code is valid or not, according to the syntax rules of prolog.

## How to use

To run this code, you need to have jacc installed on your system. You can download it from [here](http://web.cecs.pdx.edu/~mpj/jacc/).

Once you have jacc installed, you can clone this repository or download the jacc file from [here](https://github.com/arbitroy/Prolog-parser/blob/master/prolog.jacc).

In the same directory where you saved the jacc file, open a terminal and run the following command:

jacc prolog.jacc
```

This will generate two Java classes: `PrologParser` and  `PrologTokens.java`

Next, compile the Java classes with this command:

```
javac *.java
```

Now you can run the parser with this command:

```
java PrologParser
```

The parser will prompt you to enter a prolog code. You can type your code and press enter. The parser will tell you if the code is valid or not. If the code is valid, it will print "OK". If the code is invalid, it will print "Syntax error" and indicate the line and column where the error occurred.

You can enter multiple prolog codes, one per line. To exit the parser, press Ctrl+C.

## Example

Here is an example of a valid prolog code:

```
likes(john, mary).
likes(mary, john).
likes(john, pizza).
likes(mary, pasta).
likes(X, Y) :- likes(Y, X).
```

The parser will output:

```
no output will show 
```

Here is an example of an invalid prolog code:

```
likes(john mary).
likes(mary john).
likes(john pizza).
likes(mary pasta).
likes(X Y) :- likes(Y X).
```

The parser will output:

```
error
```
