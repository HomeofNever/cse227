Q1 What problem is this work addressing?
5 Points
Grading comment:
The ways of vulnerability mitigation on memory-related bugs are becoming challenging in order to fit in consensus hardware. Some implemented to avoid application-level source-code modification and compartmentalization requires changes of source code and adds more complexity to the software. All stronger protection is now layered over weaker substrates. A tendency to move these protections to lower level is clear.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The paper presents CHERI, a conventional RISC ISA, compiler and operating system to support fine-grained, capability-based memory protection. CHERI uses in-address-space protection model for efficient protection-domain switching but still supporting UNIX process model and C-language stacks. It also integrates the object-capability model for the application compartmentalization and is able to mitigates boarder range of attack. All of these ideas have implemented and have done performance testing on various popular software, with evaluation on protection over historic vulnerabilities for security measurements.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
This paper starts from re-evaluate memory-protection mitigation from ISA level which is pretty amazing. However, they also includes many new supply chain product such as compilers and new TCBs. The ISA is also a prototype without mature/in the wild evaluation. I believe it would be something great to have but hard to be accept by general public, which making it effectively theory. Small steps for conversion would be better, like canary.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The TCBs and ISA for capabilities is pretty interesting idea. Most of the time those are believed to be done by the programmer or the static/dynamic check by compilers.
