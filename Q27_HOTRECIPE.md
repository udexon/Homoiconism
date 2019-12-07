### Homoiconic Token Recursive Search and Replace (HOTRECIPE)

https://groups.google.com/forum/#!topic/comp.lang.forth/wMSmDMCY_8I

Forth has given me plenty of inspirations, leading to the following algorithm.

I would like to share it with the world first via comp.lang.forth, also to see if anyone has worked on similar algorithms, or may comment on it.


1. --- pseudo code starts ---

Recursive search and replace RPN function selection

For i in word list  
  Extract sublist 0 .. i, run test 
  Until error occurs at token i  
  Recurse into token i

Assume word list gives no error up to token i, runs as expected.

if Token i is another word list, recurse continuously into it. 

When recursion stops, find token j from database to replace token i, to eliminate errors. 

--- pseudo code ends ---

This is one of those inspirations that comes during sleep and got written down immediately after waking up.

At first look, readers may find it so generic that it might have been from some text books. So this is where you can help to eliminate this possibility.

I would also need to do some deep thinking to see if there are serious loopholes or pitfalls behind this naive looking pseudo code.

Otherwise, this might be the biggest eureka moment in human history. Sharing it with the world would also make it foolproof if proven true.


2. My code repo:

https://github.com/udexon/Homoiconism/blob/master/Android_Java_Phos.md


3. Reference to similar work:

Practical program repair via bytecode mutation
A Ghanbari, S Benton, L Zhang - Proceedings of the 28th ACM SIGSOFT …, 2019 - dl.acm.org
… Second, bytecode-level repair avoids messing up the source code in unexpected ways, and can
even be applicable for fixing code without source code information, eg … of the syntax of a specific
target programming language, and applicable to different Java versions and …
Cited by 12 Related articles All 4 versions 
