Q1 What problem is this work addressing?
5 Points
Grading comment:
In order to counter side-channeling attack such as Spectre, OS and hardware has evolve several mitigation method such as state flushing. However, all of these method will bring performance penalty and some are pretty huge that be default they are not enabled. Finding a light and robust mitigation would be necessary for the long run.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The paper proposed unmapped speculation contract, USC in short, so that any unmapped physical memory cannot be access speculatively. The paper also present WARD, a kernel that maintains separate kernel memory mappings for each process, and ensures that the memory mapped in the kernel of a process does not contain any data that must be kept secret from that process. However, if the operation strictly require to access shared memory, kernel will explicit switch to separated mapping like any idea mitigation. WARD transparently switches from Q- to K-domain through page faults, uses temporary mappings to access un-mapped physical pages, and splits data structures into public and private parts.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
This is a fine-grind control over the existing implementation to cut as many overhead as possible under different scenario. However, some functionalities still have to fall back to expensive mitigation. Still, I believe this is a practical solution unless a full rewrite of specs.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The part about thread mitigation is pretty interesting. Using Different data structure and separation for such scenario and reach better performance, this paper has consider a lot more aspect that other method has done.
