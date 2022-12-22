Q1 What problem is this work addressing?
5 Points
Grading comment:
Nowadays Web Apps has more and more third party integrations for platform to extend their capabilities. However, these integrations often requires many permissions and read/write sensitive user data, while users at the time have little or no idea what is happening behind the scene. Apps developers often hand-craft control access but these won't make sure that information will not be pass to external party (remote servers).
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
Author propose a new framework Hails, which use an architecture MPVC where policy limits the data flow. MP is the part talk with the database but it cannot interact with user, while VC is the part where user interact with but they cannot directly access data. The data flow between these components must have matching labels so it will be passed by the proxy. Multiple level of isolation are in use. OS level isolation to prevent program from accessing network or consume too much resources. While a HTTP client is provided so that program may only send data label necessary for external communication to specific destination. Language level are also harden so that no type coercion will happen and broke the isolation. Browser extension is also in place to prevent unauthorized resources being fetch or data leaks.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
I think this paper has cover pretty much every aspect of the generic third-party integration platform data flow process. While it turn out the business process is much more complicated and most of the data access is still happening externally and cannot be traced since then. We may also have some way marking our information aka provide a generic information packing standard so that user may keep track of ownership transfer of information. But this might be a different field.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
The extension of MC and VC part. It make use of existing framework and adding this extra part to include data security aspect, and also the browser extension idea is also pretty new to me. I do not realize this part will also be targeted before.
