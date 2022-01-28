# **Lab Report #2**
## 28th Jan 2021

[List of all Lab Reports](https://abijitj.github.io/cse15l-lab-reports/)

#  Error #1: 
## Logical Error: Parser shouldn't parse image files

![Image](Logical_Error.png)
Link to failing md file -> [Failing test case](https://github.com/abijitj/markdown-parse/blob/main/fail_test.md)

Symptom of error: 

![Image](logicalerror.png)

The symptom of this error was that the output showed something that was not a link. In this case, it was because the syntax for including an image was very similar to a hyperlink. The only difference being an exclamation mark appearing before the `[` in the markdown file for images. Therefore, the bug in our program was that it did not differentiate between images and links. We fixed this by adding an if statement differentiating by the exclamation mark.   

# Error #2: 
## Technical Error: Infinite Loop when the file ends with `]`
![Image](infiniteloopcommit.png)
Link to failing md file -> [Failing test case](https://github.com/abijitj/markdown-parse/blob/main/fail_test.md)

Symptom of error: 

![Image](infiniteloop.png)

The symptom of this error was that the program took exceedingly long to run and in the end resulted in a `java.lang.OutOfMemoryError`. This is often a sign of an infinite loop, which in this case was the bug because we didn't account for the file ending in a `]` leading to the loop infinitely running. 

# Error #3
