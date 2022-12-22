Q1 What problem is this work addressing?
5 Points
Grading comment:
Author tried to tackle the supply-chain attack. Examples here are JS library, some with C++ modules in use. Covered attacks include obfuscation and run malicious code at certain condition, withdrawn(take down) with no-op. Also, the same level of correctness and efficiency is preserved, while the privilege reduction is kept.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The author proposed HARP system, an ALG system for string processing. This module make use of active learning to learn the target library and generate HARP DSL. The DSL is then passed for type check as well as compared with ground truth for soundness. The selected DSL is then converted to real implementation with observed behavior. The reference (original) code is running in an isolated environment, and side-effect (e.g. process, network) will either no triggered during process, or quickly aborted since these are not yet supported by the system.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
The concept of regeneration for side effect elimination made this approach has limited usable scope. I would think if it is possible to test and record library's behavior during the process, with some symbolic analysis, to trigger and evaluate what kind of side effects/privileges libraries have. It is still possible to miss some malicious behavior while it could be quickly and better adopted on different fields.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The active learning part could actually reproduce the function of the library from the generated input, which has lots of potential and maybe more use case could be found.
