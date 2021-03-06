# Lab Report 4 Week 8

[Link to my markdown-parse repository](https://github.com/cbcielo/markdown-parser)

[Link to the reviewed repository from week 7 lab](https://github.com/aliciadaniellet/markdown-parser)

## Snippet 1
* Expected Output: [`google.com, google.com, ucsd.edu]

* Created Test:
![Image](snip1test.png)

* My Implementation Output:
![Image](snippet1.2.png)

* Week 7 Output:
![Image](snippet1.png)

## Snippet 2
* Expected Output: [b.com, a.com(()), example.com]

* Created Test:
![Image](snip2test.png)
* My Implementation Output:
![Image](snip2.png)
* Week 7 Output:
![Image](snippet2.2.png)

## Snippet 3
* Expected Output: [https://www.twitter.com, https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedu, https://cse.ucsd.edu]
* Created Test:
![Image](snip3test.png)
* My Implementation Output:
![Image](snip3.png)
* Week 7 Output:
![Image](snippet3.3.png)

## Questions to be Answered
1. Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

> Answer: Yes, you could use small code changes by adding 2 if statements (if there is a back tick after a close bracket to ignore the bracket and continue to seaarch for a valid closing bracket, and if there is a backtick before an open bracket to ignore the link inside and continue through the loop).

2. Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
> Answer: Yes, you could use small code changes by adding 2 if statements (in there is a `/` before a close bracket to ignore the bracket itself, and if there is a `/` before the open bracket to ignore the open bracket).

3. Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
> Answer: I do not think that in order to handle the `indexOutOfBounds` error can be fixed  with small code changes. This is because I think that I would need to use some sort while loop to prevent the index from going out of bounds which would most likely take up more than 10 lines of code. 
