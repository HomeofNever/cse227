Q1 What problem is this work addressing?
5 Points
Grading comment:
Trying to limit third party libraries' bug/flaw affects program's behavior. Targeted protection including data flow, control flow safety, as well as data validation. In browser settings, each of the domain with its resources are untrusted, and various libraries are used, so a lightweight solution without changing existing code need to be developed.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
They proposed RLBox, a lightweight sandbox that helps developer isolate library call from program process. It uses taint trait to keep track of what could be used by the sandbox libraries and register only APIs that could be used from the callback functions. It also provide various guideline on how to correctly use it since data validations could only be done by the developer. Race condition and shared memory TOCTOU issue also needs to be handled correctly. They also shown that this approach has less performance penalty.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
I believe this is a brilliant solution toward this issue. Making use of the fact that the program itself could make changes with best practice and wrap access of library calls. Most of the solution I came up would be like remote machine rendered to local canvas. This solution is not really possible with stable Internet access.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The part it analyze what kind of issue they have encountered when developing this tools. There are lots of pitfalls on how to properly wrap stuff and TOCTOU issue on multi process environment.
