### Homoiconic Pathfinding

[Pathfinding](https://en.wikipedia.org/wiki/Pathfinding) and homoiconicity are two fundamental topics in computer science. We propose a procedure, called "homoiconic transformation", to translate program code written in any high level programming language (C/C++, Java, Python, JavaScript, PHP, etc.) into Forth-like Reverse Polish Notation, essentially a list of tokens, know as _word list_. Pathfinding algorithms are then applied to the word list, to model the following:

- detection of runtime errors
- program modification
- program composition

Incidentally, both pathfinding and homoiconic transformation can be attributed to Edsger Wybe Dijkstra, the legendary Dutch pioneer of computer science. It would be a significant topic of research to investigate if the ideas proposed in this article have been explored by Dijkstra himself or others.

Conceptually or visually, it is tempting to represent the process of a human programmer composing a program, or metaprogramming, as a graph, of the similar nature the graph employed by Dijkstra in 1956 to determine the shortest distance between any two Dutch cities. This is because, if it can be done, then perhaps various theorems in graph theory can be applied to metaprogramming, potentially helping to advance computer science nearer to the final goal of Artificial General Intelligence.

However, the difficulties of representing metaprogramming as a graph seem to be the following:
- the edges in Dijkstra's shortest path first algorithm (DSPF) are distances between any two cities; the edges in metaprogramming are functions, or _words_ (as in Forth words), to which it may be problematic to associate a cost.

Nevertheless, having identified these difficulties may serve as a good starting point to develop our work on _homoiconic pathfinding_.

Our plan is as follows:

<ol type="a">

<li> We intend to develop rudimentary Dijkstra's type pathfinding in 2D or 3D using homoiconic transformation, i.e. to use Forth like (to be known as <em>Phos</em>) Reverse Polish Notation in <a href="https://github.com/udexon/Homoiconism/blob/master/Android_Java_Phos.md">stack machine shell (smashlet)</a> implemented in any high level host programming language. This is analogous to human babies or children learning about the physical world and physical actions.  Using the analogy of human learning at different ages, we shall develop Phos word database (function database) accordingly. </li>

<li> We wish to highlight our hypothesis that human programmers learn programming by copying, then modifying part of the code of a larger program. We will use this to model an Artificial General Intelligence (AGI) self, which is capable of performing metaprogramming using the Phos programming language outlined here. </li>


</ol>

<hr>
