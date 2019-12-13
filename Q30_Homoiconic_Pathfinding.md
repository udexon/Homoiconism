### Homoiconic Pathfinding

[Pathfinding](https://en.wikipedia.org/wiki/Pathfinding) and homoiconicity are two fundamental topics in computer science. We propose a procedure, called "homoiconic transformation", to translate program code written in any high level programming language (C/C++, Java, Python, JavaScript, PHP, etc.) into Forth-like Reverse Polish Notation, essentially a list of tokens, know as _word list_. Pathfinding algorithms are then applied to the word list, to model the following:

- detection of runtime errors
- program modification
- program composition

Incidentally, both pathfinding and homoiconic transformation can be attributed to Edsger Wybe Dijkstra, the legendary Dutch pioneer of computer science. It would be a significant topic of research to investigate if the ideas proposed in this article have been explored by Dijkstra himself or others.

Conceptually or visually, it is tempting to represent the process of a human programmer composing a program, or metaprogramming, as a graph, of the similar nature the graph employed by Dijkstra in 1956 to determine the shortest distance between any two Dutch cities. This is because, if it can be done, then perhaps various theorems in graph theory can be applied to metaprogramming, potentially helping to advance computer science nearer to the final goal of Artificial General Intelligence.


https://github.com/udexon/Homoiconism/blob/master/Q23_Phos_Smashlet.md

- We shall demonstrate how a token or a Phos or Forth word corresponds to a node (vertex) or an edge (line) in graph theory -- one of the most fundamental theories in mathematics that can be used to construct other mathematical theories as well as programming languages.

- Relate graph theory and Phos word list to pathfinding.

- Homoiconic Pathfinding (HIPF): Finding Alternative Routes in Map

Generalize Finding Alternative Routes in Map (FARM) to programming and problem solving using homoiconic transformation?

Start with small goal: artificial maze, find alternative routes.

Generalize goals to greater goals: find food, energy sources, money, land, resources, etc.

- Homoiconism is a model that allows pathfinding to be generalized to greater goals in programming and problem solving.

Program test is a special case of goal matching, defined by test function.

Program execution without test is implicit test for runtime errors, defaulting the program to halt at runtime error. Modelling program execution using HTDC / HIPF allows pathfinding to be generalized to program execution, with or without test ("without test" == default halt at runtime error).

Tests and finding routes in maps (are a subset) Pathfinding.

Stack machine represents a program as a list of tokens. Forth colon definition allows two or more tokens to be collapsed into one, where one or more tokens can be data or non-function. As such, tokens sharing a root function, with different parameters, can be categorized and compared. If they belong to the same category, various equivalence or distance functions can be applied to determine their characteristics, with respect to the preceding and subsequent tokens in the list, i.e. in relation to other functions in the program.

- Hypothesis 1: Human programmers learn programming by copying existing code, and learn how to debug; then use the acquired knowledge to compose new code. Hence the following Homoiconic Token Debugging and Composition (HTDC) algorithm:-

#### Debugging
```
For i in word list  
  Extract sublist 0 .. i, run test 
  Until error occurs at token i  
  Recurse into token i

Assume word list gives no error up to token i, runs as expected.

if Token i is another word list, recurse continuously into it. 

When recursion stops, find token j from database to replace token i, to eliminate errors. 
```

#### Program Composition
```
For j in word database  
  Add token to word list; run test 
  Until goal is achieved at token i  
```

#### Automatic Debugging for Existing Software Repositories

All AI programs deployed or in research are large and complex programs that have lots of runtime errors, managed by human researchers. Hence they are captive market to test HTDC.

Let's consider GitHub programmers who maintain repositories of AI projects. As of now, maintaining the repositories is a completely manual process. What if the maintainers add a Phos stack machine shell HTDC algorithm to the AI repository? The Phos stack machine shell (Smashlet) is a non-disruptive component that can be added to projects written in ANY programming language. 

As we now have a Forth like environment (Phos stack machine shell) to build up Forth like words, which are mapped to the functions in the host programming language, as can be analyzed using Forth like methodologies, we are hoping that we may discover some consistent patterns within the debugger simulator when we build up around 500 Forth like (Phos) words. Of course this number is just a wild guess as we do not have prior samples. But this is a breakthrough in that we now have a theoretical framework upon which to build a Forth like word database for automated debugging.

At this stage, we may have more sample words and data to investigate if Forth words and Phos words exhibit similar behaviour, as far as debugging is concerned. This has not been attempted previously, simply because:

- there was simply no theory or attempt to build a high level "software Forth" stack machine shell, as Forth programmers are too busy making their own money;

- without the above, there are simply not enough new Forth converts to investigate this critical issue, or not one realized it exists as it has not been formalized.

Debug and composition are duals. Debug finds the first runtime error from list of words. Composition find the next word to add to list, can do bottom up or top down (work backwards from goal). 

Composition may involve only very small number of words in word list, but very deep nesting and large number of candidate words in database. Hence need to debugger simulation first. 

This is one of those inspirations that comes during sleep and got written down immediately after waking up.

At first look, readers may find it so generic that it might have been from some text books. So this is where you can help to eliminate this possibility.

I would also need to do some deep thinking to see if there are serious loopholes or pitfalls behind this naive looking pseudo code.

Otherwise, this might be the biggest eureka moment in human history. Sharing it with the world would also make it foolproof if proven true.


1.2. My code repo:

https://github.com/udexon/Homoiconism/blob/master/Android_Java_Phos.md


1.3. Who else has the highest prospect to achieve Artificial General Intelligence?

Readers may compare any claim to AGI with Google's various AI projects as they have the highest profile and exposure in recent years.

Despite Google's efforts and attempts by various researchers, one area remains unexplored -- homoiconicity.

Homoiconism, which is central to the algorithm we proposed above, can compliment many of the major AI algorithms in use today. 

We intend to create an algorithm that mimics the operations of human programmers, as a first attempt to model artificial general intelligence.

A program, written in a high level programming language such as C++ or Java, is basically a series of function calls, separated by semicolons. Syntax errors are usually detected during compile time. Run time errors are errors that occur during execution, whose code are correctly written and no error was detected during compile time. 

We have conceived an inverse Shunting Yard Algorithm which converts Forth like Reverse Polish Notation into function calls in host programming language, such as C++, Java or equivalent, thereby enabling code written in any known existing programming language be transformed into reverse Polish notation.

As such, a program written in a high level programming language can be transformed into space delimited reverse Polish notation. Debugging can be considered as a process where a human programmer uses a debugger to detect run time errors of a running program. Usually, a program will execute with errors until one instance of the code gives rise to the first run time error. Based on this assumption, we have devised HOTRECIPE algorithm as described above. In summary, the essence of simulating the debugging process consists of detecting the first run time error in the program.

#### Debugging as AGI Skill

In the analysis above, we have made an assumption that debugging represents an essential AGI skill that can be further developed into human level AGI.

Although all known artificial intelligence algorithms can be divided into various fields such as robotics, image processing, expert systems etc., they are invariably implemented as programs written in some programming languages.

As such, any reader with some engineering or scientific knowledge might have asked, "Is it possible to write a program that has the ability to generate the code of another program?" Such question is known as metaprogramming. Unfortunately, metaprogrammming is a field that has received significantly less attention compared to other areas of AI research, perhaps due to its difficulties and lack of interesting discoveries in recent years.

The AI research community and industry are perhaps guilty of self-censorship and self-congratulatory, driven by "human nature" (pun intended!!) as with other fields of human activities, by avoiding to highlight areas such as metaprogramming that MAY lead to signficiant breakthrough.


#### Why has Forth not become more popular?

As digital archives have preserved most of the history of computin itself, we now have substantial references to look at various historical questions, such as:

- Why has Forth not become more popular?

I suppose Intel 386 and its descendants defined much of today's computing landscape. After the launch of Intel 386, Microsoft Windows and Linux dominated the world, powered by GNU C Compiler, forcing Microsoft to embrace C/C++ too. In the ensuing decades, programmers did not have the habit to use multiple programming languages, until the era of web servers created the PHP+JavaScript+MySQL ecosystems, resulting in the multilingual environment that we have today.

During this period, Forth did not have apparet advantages compared to the more popular programming languages. We believe our work in generalizing the Inverse Shunting Yard Algorithm (ISYA) will make Forth an essential candidate for all to learn in the programming ecosystems as our Phos stack machine shell could become a universal interface to all known programming languages:

https://github.com/udexon/Homoiconism/blob/master/Q23_Phos_Smashlet.md


- Can HOTRECIPE be implemented in non-homoiconic high level programming languages, such as C++ or Java? 

Phos stack machine shell (Smashlet) fundamentally change the concept of "writing a program in programming language X", as theoretically, the Inverse Shunting Yard Algorithm, the inverse of Dijkstra's now legendary Shunting Yard Algorithm (DSYA), can be implemented in any known programming language.

- How can we prove that "the Inverse Shunting Yard Algorithm can be implemented in any known programming language"?

- How can we prove that "Phos stack machine shell could become a universal interface to all known programming languages"?

3. Reference to similar work:

Practical program repair via bytecode mutation
A Ghanbari, S Benton, L Zhang - Proceedings of the 28th ACM SIGSOFT …, 2019 - dl.acm.org
… Second, bytecode-level repair avoids messing up the source code in unexpected ways, and can
even be applicable for fixing code without source code information, eg … of the syntax of a specific
target programming language, and applicable to different Java versions and …
Cited by 12 Related articles All 4 versions 

4. Original post:

https://groups.google.com/forum/#!topic/comp.lang.forth/wMSmDMCY_8I

Forth has given me plenty of inspirations, leading to the following algorithm.

I would like to share it with the world first via comp.lang.forth, also to see if anyone has worked on similar algorithms, or may comment on it.
