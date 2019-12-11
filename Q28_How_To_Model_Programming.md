### #GOQ_Q28 
- How do we model programming?
#### A Homoiconic Model of Metaprogramming

"How to model programming" refers to a technical description outlining the steps and analysis involved when a human programmer attempts to write a program. It is different from the topic ["programming model"](https://en.wikipedia.org/wiki/Programming_model) described in Wikipedia.

Despite the long history of computer programming since the launch of [Fortran](https://en.wikipedia.org/wiki/Fortran) on IBM 704 in 1957, more than 60 years ago, _modelling programming_ lies at the very core of artificial intelligence, which eluded attempts by many great minds since, as we shall elaborate in this article.

We shall begin to describe modelling programming using a simple example, a Python program to print "Hello":

```
print("Hello")
```

Behind this trivial example are many issues that remain open for decades, such as:
- Why would the programmer want to write this program?
- How do we model the programmer's motivations, including his (her) intention to write this program?

It is beyond the scope of this article to give a comprehensive treatment to the questions above. They however serve as useful introduction. 

In order to define our model of programming, two significant breakthroughs are required:
- homoiconic transformation
- [homoiconic token debugging and composition](https://github.com/udexon/Homoiconism/blob/master/Q27_HOTRECIPE.md)

#### [Homoiconic Transformation](https://github.com/udexon/GOEHDOM/blob/master/Homoiconicity.md#homoiconic-transformation)


"Homoiconic transformation"  refers to process of transforming non-homoiconic code into homoiconic form, involving the use DYSA and ISYA:

- [Dijkstra's Shunting Yard Algorithm (DSYA)](https://en.wikipedia.org/wiki/Shunting-yard_algorithm) might be regarded as the common ancestor of subsequent programming languages. It was central to the design of ALGOL, which influenced all other modern programming languages. 

- Although the Forth programming language has been implemented in many host Programming Languages in the past, I believe I was the first to coin the term ***Inverse Shunting Yard Algorithm (ISYA)*** as a generalization of *translating reverse Polish notation into a host (high level, "third generation") programming language,* which is effectively the inverse of Dijkstra's now legendary Shunting Yard Algorithm (DSYA). In summary, the steps include:
  - parsing a list of tokens in the Reverse Polish Notation, 
  - pushing non-function tokens on to the stack, and 
  - executing a function upon reading a function token. 
