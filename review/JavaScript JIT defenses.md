Q1 What problem is this work addressing?
5 Points
Grading comment:
JIT compiler have a hard time trying to make the correct analysis over the range, due to complex JS specification over numbers. Adding checks/guards for each of these memory access is inefficient while aggressively removing them have left various bugs behind. A better way to solving this issue is critical as the rapid develop of Web tech
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
Author provide a system, VeRA for verifying range analysis in JIT. It has divided the range analysis into two parts: inrange identify whether the value fits the Range definition, and the wellForm test if the Range definition is valid in the context. The authro also provide a DSL, VeRA C++ for this sepcific verification needs, and provide the IR from the C++ code. It then converted to SMT terms that replicates the C++ semantics. The overall performance is better when verified version is used in firefox.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
Some limitation imposed are e.g. unbounded/space is too large to verify, and the generated bound may not be the tightest. I believe for this research purposes, this problem has beautifully solved, for me I would just fuzzing for large space verification so that we may have some backup for this kind of situation
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
I believe the part where evaluating correctness and the division of inRange and wellFormed is pretty interesting. These are new concepts to me and I won't bother reasoning that part myself.
