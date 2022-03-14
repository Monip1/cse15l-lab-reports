[Back](https://monip1.github.io/cse15l-lab-reports/)
---
Elena Tomson
---
Lab Report #5 Week 10

I used diff to differentiate the files. 

![difference](Pictures/diff.png)

When we look at the results file from class we find 
![results](Pictures/results.png)

List of differences in numbered .md files --
--- 
From file 494:
line 878 has `[\(foo\)]`

From file 495:
line 880 has `[foo(and(bar))]`

From file 496:
line 882 has `[]`

From file 497:
line 884 has `[]`

From file 498:
line 886 has `[]`


My results file showed

![myResults](Pictures/myresults.png)

From file 494:
line 878 has `[\(foo\]`

From file 495:
line 880 has `[foo(and(bar]`

From file 496:
line 882 has `[foo(and(bar]`

From file 497:
line 884 has `[foo\(and\(bar\]`

From file 498:
line 886 has `[<foo(and(bar]`

The actual outputs are
stacked 494 as the bottom error, 495 as middle, and the equal 497 amd 498 link on top.
496 has no link

![494](Pictures/494.png)
So
------------------------------------- Joe's code ------------- myCode --------------- Actual

From file 494: 
line 878 has---`[\(foo\)]`--------------`[\(foo\]`---------------`[(foo)]`


From file 495: 
line 880 has---`[foo(and(bar))]`---`[foo(and(bar]`------`[foo(and(bar))]`

From file 496: 
line 882 has---`[]`---------------------------`[foo(and(bar]`------`[]`

From file 497: 
line 884 has---`[]`---------------------------`[foo\(and\(bar\]`---`[foo(and(bar)]`

From file 498: 
line 886 has---`[]`---------------------------`[<foo(and(bar]`-----`[foo(and(bar)]`


For my 2 files I choose file 494 and 496.

Int file 494, both the lab code and my own code were incorrect.

One fix is that my code is missing the last parentheses

![paren](Pictures/closedParen.png)

This method is not accurately tracking the parantheses and if it used a Stack, it could better keep count of parentheses within the link.

