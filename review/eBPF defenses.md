Q1 What problem is this work addressing?
5 Points
Grading comment:
Linux kernel, instead of using a interpreter, has now move onto JIT mode, since it helps prevent various side channel attack, and has performance gain. However, JIT mode also means that the kernel would also need to do the code generation, and it means things will become complicated for both verification and implementation side. BFP now has to first check if the program is valid from the code perspective, but also has to find a way to make sure that the JIT generated code is also comply with the standard.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The author designed Jitterbug, which focus on deployability. Kernel does not need to change API for adoption and it could automatic verification in a rapid speed. The final artifacts could be audit separately without prior knowledge about BFP etc. The idea here is to verify the final product, the step-by-step specification instead of the JIT or the code itself. The author also made a DSL, which is a subset of the C with limited types, and speed up the verification process.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
I believe this would be a great approach since they have workaround the most complex and unreachable area of the verification field. Yet still make verification process possible by abstraction on the DSL level and made a generic approach to verify various JIT implementations.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The way the choose what to verify and what don't is interesting, they have also stated some of the idea about how to finalize their range
