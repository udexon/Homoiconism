## Homoiconism

We coin the term "homoiconism" to refer to the procedures, analyses and related topics where non-homoiconic program code is transformed into homoiconic form, as this subject has not been investigated extensively elsewhere. We believe we have invented a novel, generalized procedure for transforming programs written in ***ANY known programming language*** into a Forth like Reverse Polish Notation syntax, known as the ***Inverse Shunting Yard Algorithm (ISYA)***, thus making homoiconism accessible to a much wider audience than previously possible.

https://en.wikipedia.org/wiki/Homoiconicity

While Wikipedia and the few literature briefly explored some issues concerning homoiconicity, we believe they can be addressed systematically using ISYA.

:: eval() vs. others??

*ANY*

:: quote minimum text concerning topic to be discussed (whatever concerned homoiconicity) to that readers can follow and look up.

We shall illustrate our work with some code examples first, before delving into further theoretical discussions.

Although the term _homoiconic_ refers to the property of a programming language where code and data are represented using the same form (same="homo", form="icon"), the crux of the matter is _the ability of a program to analyze and process the code of another program (including itself) written in the same programming language_, although this motivation might not have been highlighted in existing literature.

Figures 1 and 2 show portions of code from `SensorHelper.java` from:

https://github.com/udexon/ReactiveSensors/blob/RxJava2.x/app/src/main/java/com/github/pwittchen/reactivesensors/app/SensorHelper.java

Phos is a _stack machine shell (smashlet)_ that employs Forth like Reverse Polish Notation, as shown in line 43 and 45 of figure 2.

https://github.com/udexon/ReactiveSensors/blob/RxJava2.x/app/src/main/java/com/udexon/smashlet/Phos.java

<p align="center"><a name="fig_1">Figure 1</a>
<img src="https://github.com/udexon/Homoiconism/blob/master/ReactiveSensors/import_Phos_2.png" width=700>

<p align="center"><a name="fig_2">Figure 2</a>
<img src="https://github.com/udexon/Homoiconism/blob/master/ReactiveSensors/Phos_F_2.png" width=700>

```
Phos.F(": now_sec now: colon: explode:   2 ia: ;");

            Phos.F("rae: t tk:  3 bzk:  " +
                    "t_exists_retrieve_t t tr: now_sec dup: t t:  fsub:");
                    
```

`Phos.F()` takes a space delimited string, pushes non-function tokens on to the stack, and execute functions in the host programming language (in this case, Java) mapped by fuction words (tokens). The previous sentence basically summarizes the operations of a stack machine shell (smashlet). Due to its simplicity, it can be implemented in all known programming languages. We have successfully implemented Phos Smashlet in PHP, JavaScript and Java.
