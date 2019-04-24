# Technical Debt
---
## Project inspection
1. Unclear, unreadable code: **+** 
2. Duplicate code: **+** 
3. Lack of test automation, build automation, deployment automation: **+** 
4. Tangled architecture & unnecessarily complex dependencies: **-** 
5. Slow, ineffective code: **+**
6. Uncommitted code & long-lived branches: **-** 
7. Important technical documentation that is missing or out-of-date: **-** 
8. Unnecessary technical documentation that is being maintained and keep up-to-data: **-**
9. Lack of test environments: **+**
10. Long build-test cycle & lack of continuous integration: **-**  
## The solution to technical debt 
1. Code refactoring: **STOP WRITING CRAPPY CODE AND GRADUALLY CLEAN UP THE OLD ONE.** (ID 15):
   * lack of duplicate code, spend less time to work with code;
   * value: 15.
2. Add tests environments (ID 16):
    * tests should cover main functionality(this features have story metric value more than 20 points);
    * value: 15.
3. Add automation deployment (ID 17):
    * reduction of time to deployment;
    * value: 20.    
## Technical debt vs not implemented features and Conclusion
The curve of total technical debt of our project is in area between debt baseline and debt ceiling.
We can continuing implement our features, but in this case our debt hits "red" line. This fact will 
stop project development. To avoid delays and increase speed development our team scheduled the list of events 
(changes has been added to scrum board) that will execute in next sprint. 
