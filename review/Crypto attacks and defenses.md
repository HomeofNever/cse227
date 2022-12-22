Q1 What problem is this work addressing?
5 Points
Grading comment:
SSL has been widely used in browser environment. However, this technology is also used in various non-browser environment, such as SDK and APIs; and these libraries, which are not actively under public testing, has various misuse and misinterpretation over the lower level APIs from SSL libraries.
Q2 How did the author(s) address the problem?
5 Points
Grading comment:
The author provide an in-depth analysis this problem on various libraries, including payment gateway SDK, browsers, etc. Most of the error would be misuse of API parameters, failed to correctly follow the specs to evaluate the host-name correctness, intentionally use outdated or unsafe method, etc. This expose various security concerns including but not limits to leaking credentials, sensitive data. While some SDK are widely used by various Apps, one flaw may put the a bunch of apps in security concerns.
Q3 Would you have solved the problem differently? If so, how?
5 Points
Grading comment:
Most of the logic found are logic bugs, such changing the API of these SSL libraries to be more intuitive and providing correct sample codes, be more secure by default would help a lot. Adding notes to common pitfalls and warn user about unsafe actions should also be in place.
Q4 What is the most interesting part of the paper?
5 Points
Grading comment:
Developers should be more careful about SDKs they use and they could not assume that these code would be safe by default. It is interesting to get this facts.
