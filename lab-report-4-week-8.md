# Week 6 Lab Report
*By Luis Velediaz*

Welcome once again to CSE 15L. Glad to have you here! For each snippet, we will add a test both to our implementation of markdown-parse, and the implementation we reviewed in week 7. Run the tests and show the results of running the tests on each. This means we added a total of 6test methods 


```
**Snippet 1**
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```
```
**Snippet 2**
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
```
**Snippet 3**
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

**Here are the links to both markdown-parse repositorys.**

My groups [markdown-parse repository.](https://github.com/bchoUCSD/markdown-parser)

Link to the [markdown-parse repositorys we reviewed in week 7.](https://github.com/KristinEbu/markdown-parser)

*READY? Lets go!*


***SNIPPET 1***
**What is the expected output?** 
-  ![produce1](produce1.png)

**The code in MarkdownParseTest.java for how I turned it into a test.**
- ![test1](test1.png)

1) *Snippet 1 Our Repository*
- For your implementation, the corresponding output when running the tests didn’t pass and here is the specific part of the JUnit output that shows the test failure.
-  ![ourTest1](ourTest1.png)


2) *Snippet 1 Reviewed Repository*
- For the implementation you reviewed in Week 7, the corresponding didn’t pass and here is the specific part of the JUnit output that shows the test failure.
- ![otherTest1](otherTest1.png)


***SNIPPET 2***
**What is the expected output?** 
- ![produce2](produce2.png)

**The code in MarkdownParseTest.java for how I turned it into a test.**
- ![test2](test2.png)

3) *Snippet 2 Our Repository*
- For our implementation, the corresponding output when running the tests, passed.

4) *Snippet 2 Reviewed Repository*
- For the implementation we reviewed in Week 7, the corresponding output when running the tests passed.

***SNIPPET 3***
**What is the expected output?** 
- ![produce3](produce3.png)

**The code in MarkdownParseTest.java for how I turned it into a test.**
- ![test3](test3.png)

5) *Snippet 3 Our Repository*
- For our implementation, the corresponding output when running the tests didn’t pass and here is the specific part of the JUnit output that shows the test failure.

-  ![ourTest3](ourTest3.png)


6) *Snippet 3 Reviewed Repository*
- For the implementation you reviewed in Week 7, the corresponding didn’t pass and here is the specific part of the JUnit output that shows the test failure.
- ![otherTest3](otherTest3.png)


***REVIEW QUESTIONS***
1) Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

- In my opion I believe that a small code change would make the program work for snippet 1 that uses incline code with backticks. This is because I think that as long as the backtick goes after the bracket or parenthesis, the image format will override it. So for this code we will basically add an if statment that checks for the backtick if it goes before the "[ " and then doesn't add this string to the list. 


2) Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.
- In my opion I believe that a small code change would make the program work for snippet 2 that uses incline code with nested parenthesis and brackets. This is because I think that as of right now we have the code mostly functioning as during our tests, it passed. However I believe that we can improve it a little bit by making sure our code through the usage of if statements checks for the format "[]()" and will restart the check if it sees that format inside of [].


3) Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.
- I think a small code change will be needed to make the program work for snippet 3 andall the related cases with newlines in brackets and parenthesis. I believe that the code must simply check for an empyt line, which breaks the md format of a link. We should be able to use and if statement that makes sure that there is no full line break since we already solved the issue of checking for specefically the format "[]()".If that format is broken or there is an entire line of blank code (line break) then the link wont be added.

