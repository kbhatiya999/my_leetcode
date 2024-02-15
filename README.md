# my_leetcode

## https://leetcode.com/problems/4-keys-keyboard/editorial/?envType=study-plan-v2&envId=dynamic-programming-grandmaster
```Semi-Formed Thoughts
Single 'A' at the Beginning:  After selecting and copying some text, there's no point in ever typing a single 'A' again.  We can always achieve the same result by pasting. This lets us assume we type one 'A' to start things off.

1) DO NOT copy single A as you can just write A instead of CTRL+V while saving CTRL+A, CTRL+C for 2 extra AA
2) At 7th point in table below
How do we decide [2 A's with 3 paste = 8] OR [3 A's with 2 paste = 9] using previous values.
Do we use 6,5,4,3,2,1 value
For pasting we need to select and copy - that is 2 steps. And atleast 1 for paste.
So for using paste atleast once we need 7th, 6th, 5th keypress.
So we check:
i  )  4 + 1paste
ii )  3 + 2 paste
iii)  2 + 3 paste
... so on
So how far behind we will see? or do we see forward? definitely forward
3) As per the editorial:
i) After initial few A's that we write manually we need to copy paste
ii)



kepress | max A
----------------------------------
1       | A
2       | AA
3       | AA A
4       | AA AA
5       | AA AAA | NO - Following 1) and using CTRL+A, CTRL+C and CTRL+V you will get AAAA. You can have 5 A's by typing.
6       | AA AAAA | NO - ALL are equal just type A. You can copy [2 A's with 2 paste = 6] OR [3 A's with 1 paste = 6]. 
7       | AA AAAAA | [2 A's with 3 paste = 8] OR [3 A's with 2 paste = 9]




```
