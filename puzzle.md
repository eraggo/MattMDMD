# Matt Parker MDMD Challence
Matt Parker did [youtube video](https://www.youtube.com/watch?v=AXfl_e33Gt4) and challenged viewers to make such arrangement of numbers 1 to 9 so that each pair summed together is a prime. 

As for an example numbers 1-5 can be arranged as such: 5 2 1 4 3, making each pair of numbers as prime; 5+2=7, 2+1=3, 1+4=5, 4+3=7.

## Thinking about solution
First thing coming in the mind - of course - is that there is **no** 2 even numbers summed together making sum prime. To make sure this is clear even (E) plus even (E) always get even result. Also odd(O)+odd(O) is always even. There are only 4 even numbers between 1 to 9

Therefore resulting string of numbers have to go in this way:
* O E O E O E O E O

Where E stands for even and O as odd like said early.

## Eliminating digits as possible pairs
We know that each number pair is considered as odd+even pair like said above. There are, however restrictions how these pairs can be divided. Pairs should be such as sum is prime, so as example 3+6 is not allowed since 9 is not prime.

Getting sums as primes are sometimes tricky by hand. So let's eliminate digits on following this small array. Array has each cell marked as if "x" is prime of x and y axis.

x+y| 2 | 4 | 6 | 8
-|-|-|-|-
1|x|x|x||
3|x|x||x|
5|x||x|x|
7||x|x||
9|x|x||x|

Looking at table it seems like that 7 is most restricted number on the sequence making it middleish number. These 7+6=13 and 7+4=11 cleans that line. That why we know that sequence consists **476** in some order. Again 4+7 and 7+6 equals as a prime.


Let's delete 7 line: 
x+y| 2 | 4 | 6 | 8
-|-|-|-|-
1|x|x|x||
3|x|x||x|
5|x||x|x|
9|x|x||x|

Let's also remove 6 column; **4765**
x+y| 2 | 4 | 8
-|-|-|-|
1|x|x||
3|x||x|
5|x||x|
9|x||x|

Now we can see that number 4 can be only paired with 1; hence sequence is **14765**
x+y| 2 | 8
-|-|
1|x||
3|x|x|
5|x|x|
9|x|x|

**214765**

x+y| 2 | 8
-|-|
3|x|x|
5|x|x|
9|x|x|

One solution **921476583**

If however challenge was to make sequence from 1 to 10, just insert 10 at the start. **10921476583**





























