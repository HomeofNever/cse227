Q1 What problem is this work addressing?
5 Points
Grading comment:
The paper tried to find a way to prevent programming errors that would lead to unauthorized acquisition of privileges, since not all actions done by the program need to be under privileges, while some of the "unprivileged code" error could help attackers win full access of the system. A way to confine these code is necessary.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The author proposed a generic, extensive framework of how to separate unprivileged code with privileged part. The program will first spawn a monitor and may have several unprivileged slave for various task needs no privilege. When they encounter situations that they need to have access to information they don't have privilege to access, they send a request to the monitor, which has privilege to do so. The monitor then verify the request and send back the file descriptor. For changing identity, the author also proposed a way for memory sharing so parent could wait for current child to exit after state exported, and monitor would spawn a slave to appropriate permission and import state back. The monitor would also keep a list of allowed permission and keep a state machine so that only specific order of permission could be called, and further reduce the attack surface.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
i believe this is a pretty elegant solution, although being limited by the OS, the change of identity is a little bit complicated. I think maybe some research could be done on the OS kernel side as it seems to be some pretty common use case of principle of least privilege.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The author also gave statement about the framework they given would make the code be more organized and clean. Could it also limits the way the program being written? e.g. wrapping all functions with privilege seems to be a burden. No clear data seems to be given for this statement.
