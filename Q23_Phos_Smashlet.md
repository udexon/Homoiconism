### Mastering Computer Programming and Abstract Mathematics _One Token At A Time_ with Phos Stack Machine Shell Language (Smashlet)

Computer programming and abstract mathematics have the same origin. Over the years, specialization has resulted in separation of disciplines, although occasionally we witness cross fertilization of the two fields, especially in computer algebra system.  

We have rediscovered the secret formula linking computer programming and abstract mathematics, which has several very important practical applications:
- enabling learners to learn computer programming AND abstract mathematics using one line of code at a time
- enabling programmers, from novice to experts, to collaborate on complex programs and systems globally, with one line of code at a time.

We call this system Phos -- it is a shell programming language based on stack machine. It is abbreviated as Smashlet -- stack machine shell language engine terminal.

- _Phos Smashlet takes a space delimited string, pushes non-function tokens on to the stack, and execute functions in the host programming language mapped by fuction words (tokens)._

The previous sentence basically summarizes the operations of a stack machine shell (smashlet). Due to its simplicity, it can be implemented in all known programming languages. We have successfully implemented Phos Smashlet in PHP, JavaScript and Java:

- [Phos Smashlet in PHP and JavaScript](https://github.com/udexon/GOEHDOM/blob/master/Phos_Smashlet.md)
- [Phos Smashlet in Android Java](https://github.com/udexon/Homoiconism/blob/master/README.md)


The creation of Phos Smashlet is based on the Forth programming language, a relatively unknown programming language nowadays, launched in 1968 by Charles H. Moore. Although not much is known about the relationships between Charles Moore and Gordon Moore, the co-founder of Intel whose name gave rose to the Moore's law, some fans of Charles Moore believe that Charles's contribution to computing may one day outshine that of Gordon's, as we shall explore in this article.

Forth has been implemented on almost all know microprocessor architecture ("hardware Forth"). Below is a list of Forth implementations as a module within a high level programming language ("software Forth"), similar to Phos Smashlet, but with their features as well as limitations:

- https://github.com/udexon/GOEHDOM/blob/master/Forth_ports.md

The features of "software Forth" compared to Phos mainly concern with faithfully cloning hardware Forth "words" (functions), but their limitations lie largely in being a separate module, not well integrated with the host programming language, and having a bigger footprint. Nevertheless, the footprint that we are concerned here are merely several hundred to several thousand lines of code in the host programming language, with Phos consuming as little as 20 lines of code in the host programming language for its basic functionalities. It is a far cry from the multiple GBs involved in typical node.js / npm installations these days.

Instead of calling Forth an artificial creation, some may describe it as a "discovery", much like the discovery of mathematical and physical laws. With Forth, or its extension Phos, we may continue to explore the mysteries of abstract mathematics and computer programming. 

We use the name Phos as it rhymes with Forth, and it means "light" in Greek.

#### _One Token At A Time_ or _One Line At A Time_?

Acute readers may notice the difference in the title of the article and the introduction where we stated _"one token at a time"_ and _"one line at a time"_.

They are not contradictory. 

_Token_, in the modern (i.e. after Forth) definition, refers to the output of the C function `strtok()`, where a line of text, with words separated by delimiters are broken into words. Incidentally, _word_ is the original term in the Forth programming language which became _token_ in programming languages after C.

We shall demonstrate how a _token_ or a Phos or Forth _word_ corresponds to a node (vertex) or an edge (line) in graph theory -- one of the most fundamental theories in mathematics that can be used to construct other mathematical theories as well as programming languages.

_A line of code_, usually refers to the unit of code separated by a semicolon ('`;`') in C or similar programming languages. Increasingly, some modern implementations of programming languages such as JavaScript and Kotlin have dropped the use of semicolon and line break is used instead.

Strictly, there is no line break in Forth and Phos type of stack machine programming languages, as we shall learn later. We use the phrase _"one line at a time"_ to appeal to readers for the sake of convenience.

- [How does the Phos programming language address the challenges of non-Latin programming languages?](https://github.com/udexon/Homoiconism/blob/master/Q22_OBOR_Scratch.md#goq_q24)
  + [Unicode definition names and multilingual programming](https://groups.google.com/forum/#!topic/comp.lang.forth/n4NiapCht-I)

- [Upstream / Downstream Supply Chain Model for Programming Language](https://github.com/udexon/Homoiconism/blob/master/Q19_HIP_Advantages.md#2-upstream--downstream-supply-chain-model-for-programming-language)

<!-- need preceding two spaces for nested indent to work!! -->

* Compare Scratch, Blockly and Logo
  - https://github.com/udexon/Homoiconism/blob/master/Q20_Homogotchi_CAS.md
  - https://github.com/udexon/Homoiconism/blob/master/Q21_Compare_Logo.md
  - [How does Phos overcome the side effects of too many programming languages?](https://github.com/udexon/Homoiconism/blob/master/Q22_OBOR_Scratch.md#goq_q26)

- [Unifying Programming and Mathematics](https://github.com/udexon/Homoiconism/blob/master/Q19_HIP_Advantages.md#3-unifying-programming-and-mathematics)

<hr>
