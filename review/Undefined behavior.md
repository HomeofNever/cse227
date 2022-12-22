Q1 What problem is this work addressing?
5 Points
Grading comment:
The paper tried to accommodate the issue of multiple deferred undef type (undef and poison) would cause various end-to-end miscompilcations happened in LLVM IR, as they are not justify in every optimization. Even though some optimizations cases miscomplications will be reported to LLVM and get fixed, others which affected large existing code will not be accepted.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The author proposed a new instruction, freeze and drop the undef var (replaced by poison), along with some changes on breaching/operation behavior over freeze/poison. After the changes, by putting freeze instruction in the right place, this kind of miscomplication will be fixed, and is acceptable (nearly no effects over compilation).
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
As usual, I don't really have much experience in complication but the things under undef behavior and their approach sounds pretty well. I like the idea of freeze and less defer vars, while some cases like vector still needs lots of adoption, I am not sure if this will be the best options for such big changes.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The cases mentioned about various hoisting optimization and cases where it doesn't work are pretty amazing, and also shown the widespread of how optimization are not handle correctly for these problem.
