### Phos Smashlet for Android Java

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

In line 45, the Phos statement is:

```
rae: t tk:  3 bzk:  
            t_exists_retrieve_t t tr: 
            now_sec dup: t t:  fsub:
```

Words with a colon suffix are function words that maps to functions in the host programming language. For example, `rae:` maps to `S.removeAllElements()` in line 1894, as shown in figure 3:

<p align="center"><a name="fig_3">Figure 3</a></p>
       
<img src="https://github.com/udexon/Homoiconism/blob/master/ReactiveSensors/Phos_rae.png" width=500>


| Word  | Definition  |   |   |   |
|---|---|---|---|---|
| `rae:`  | `S.removeAllElements()`  |   |   |   |
| `t tk:`   | if key `t` exists  |   |   |   |
| `k bzk:`  | branch forward by `k` tokens if zero  |   |   |   |
| `t tr:`   | read from key `t`  |   |   |   |
| `now_sec`   | alias as defined in line 43  |   |   |   |
| `dup:`   | duplicate top of stack  |   |   |   |
| `x v t:`  | store `x` in variable `v`  |   |   |   |
| `fsub:`   | float substract  |   |   |   |

       
The complete definitions for Phos function words are given in `Phos.java`.

Just like Forth, the result of an operation is pushed back on to the stack.

In summary, the pseudo code for line 45 is:

```
remove all elements on stack 
    ( this is necessary as createSubscription() is called every time a sensor value 
    is updated. )
    
check if key t (time) exists in tree T
    if not, branch forward by 3 tokens
    if t exists, read t and store the result on stack
    
get current time, store it in T['t']

substract previous value of T['t'] from current time

store the result on stack, to be read by line 49
```
