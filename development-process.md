# Development Process

* Definition of Done
  - Code is developed without static code analysis warnings or errors, and has been refactored if merited
  - Reasonable tests for functionality 
    - Unit tests - all logic-oriented code. This can exclude thin controllers, and data access code (better covered by integration)
	- Integration tests - key low-level interactions (i.e. queries with more than 1 constraint, saving complex objects, API testing)
	- End-to-end tests (AATs) - most critical full happy and unhappy paths through the software. There should be very few with high impact (~25-50)
	- Build & tests passing on CI server
	- Accepted by the client

* Development Process
  - Branch & PR for changes, reviewed before merged
  - Create PR when starting work 
  - Merge every 1-2 days, not based on feature completion (use isolated, stable code, feature switch, etc.). Code depended on in multiple places could diverge too much. 
  - Squash high number of commits about one thing (not when merging into master) 
  - Run tests before pushing 
  - After pushing
	  - Check pipeline 
  - After deployment
	  - Check Demo site 
  - Create issues for items that are not addressed right away. Reference them in the PR that addresses them.  

* Coding Standards 
  - Follow these C# Coding Guidelines, http://csharpguidelines.codeplex.com/downloads/get/540283
  - Follow these Microsoft C# Coding Conventions, https://msdn.microsoft.com/en-us/library/ff926074.aspx
  - Follow the principles of clean code & good Agile engineering. Some highlights include:
    - Methods <=20 lines, line length of <=120 lines
    - One level of abstraction per method 
    - Meaningful naming (long and descriptive over short and vague)
    - Little to no comments except on exceptional situations like hacks/workarounds, code to be used, etc.
    - One assert per test 
    - SOLID principles + DRY
    - Refactor often when finishing functionality 
    - The entire book Clean Code 
 
 * Tech to review
    - Architecture, how to run, models for each app
    
