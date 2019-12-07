### Homoiconic Token Recursive Search and Replace (HOTRECIPE)

https://groups.google.com/forum/#!topic/comp.lang.forth/wMSmDMCY_8I

Forth has given me plenty of inspirations, leading to the following algorithm.

I would like to share it with the world first via comp.lang.forth, also to see if anyone has worked on similar algorithms, or may comment on it.


1. --- pseudo code starts ---


```
For i in word list  
  Extract sublist 0 .. i, run test 
  Until error occurs at token i  
  Recurse into token i

Assume word list gives no error up to token i, runs as expected.

if Token i is another word list, recurse continuously into it. 

When recursion stops, find token j from database to replace token i, to eliminate errors. 
```
--- pseudo code ends ---

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

As such, any reader with some engineering or scientific knowledge might have asked, "Is it possible to write a program that has the ability to generate the code of another program?" Such question is known as metaprogramming. Unfortunately, metaprogrammming is field that has received significantly less attention compared to other areas of AI research, perhaps due to its difficulties and lack of interesting discoveries in recent years.

The AI research community and industry are perhaps guilty of self-censorship and self-congratulatory, driven by "human nature" (pun intended!!) as with other fields of human activities, by avoiding to highlight areas such as metaprogramming that MAY lead to signficiant breakthrough.


#### Why has Forth not become more popular?

As digital archives have preserved most of the history of computin itself, we now have substantial references to look at various historical questions, such as:

- Why has Forth not become more popular?

I suppose Intel 386 and its descendants defined much of today's computing landscape. After the launch of Intel 386, Microsoft Windows and Linux dominated the world, powered by GNU C Compiler, forcing Microsoft to embrace C/C++ too. In the ensuing decades, programmers did not have the habit to use multiple programming languages, until the era of web servers created the PHP+JavaScript+MySQL ecosystems, resulting in the multilingual environment that we have today.

During this period, Forth did not have apparet advantages compared to the more popular programming languages. We believe our work in generalizing the Inverse Shunting Yard Algorithm (ISYA) will make Forth an essential candidate for all to learn in the programming ecosystems as our Phos stack machine shell could become a universal interface to all known programming languages:

https://github.com/udexon/Homoiconism/blob/master/Q23_Phos_Smashlet.md



3. Reference to similar work:

Practical program repair via bytecode mutation
A Ghanbari, S Benton, L Zhang - Proceedings of the 28th ACM SIGSOFT …, 2019 - dl.acm.org
… Second, bytecode-level repair avoids messing up the source code in unexpected ways, and can
even be applicable for fixing code without source code information, eg … of the syntax of a specific
target programming language, and applicable to different Java versions and …
Cited by 12 Related articles All 4 versions 
