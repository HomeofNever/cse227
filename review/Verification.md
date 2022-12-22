Q1 What problem is this work addressing?
5 Points
Grading comment:
The OS kernel is the most important part of a computer system, while it correctness is hard to prove. Most of them are implemented in C which has lots of undefined behavior to reason. Most of the OS’s interface are not finite, e.g. fd may have unlimited amount of numbers and they should be unique among process. Large scale formal prove is hard to be done while it should be done.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The paper introduce a new OS kernel called hyper kernel. It redesign the interface with finite in mind, and also integrate high level declaratively specification with python and corresponded C handler complied into LLVM IR into SMT solver. As limited into finite set, all symbolic execution are fully unrolled and explored when verifying, and address space are mapped into physical one in hardware virtualization. The author also have done works on trapping undefined behavior with various attempts to cover as many cases as possible. Still some of the interface, worth mentioning, are infinite e.g. mmap.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
This is a pretty big issue but changing both kernel interface and having a large non-verified set of code base is hard from ideal. Also its verifying does not cover C code since different interpreters may produce different IR. This problem may be considered from language level perspective i.e. Rust for memory safety guarantees.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
Verifying with hardware virtualization and mapping physical for checking is pretty interesting, and the performance are also great in comparison of the number of code being formally verified.
