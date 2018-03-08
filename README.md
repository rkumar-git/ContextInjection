# ContextInjection
==============================================================================
Context Injection - For Steps reusability with SpecFlow and Selenium WebDriver.
==============================================================================
Automated Acceptance testing is important milestone in Acceptance Test Driven Development. 
The automation tools like SpecFlow and Selenium playing an active role in automated acceptance driven test scenarios in the Agile projects.

Problem Statement:
In the Acceptance Test Driven Development with SpecFlow and WebDriver, throwing exception during the test run, which indicates the non-availability of WebDriver to perform the Test. Since, once the instance of WebDriver shared across the step definitions for execution, WebDriver  availability is getting nullified and getting "WebDriver" not available exception. Regression and Integration test executions will be seriously affected with these exception and its a nightmare to the long run test executions.

Solution:
SpecFlow have the luxury of "Context Injection" feature, which support to share the WebDriver instance across the step definition. The Context Injection feature will instantiate and inject class instance for the scenarios. It groups the shared state to Context-classes, and inject them into every binding class that is interested in that shared state. The context injection designed to share data between two step definitions. 

The two most important rule for Context Injection are
•	The life time of an injected object is limited to the scenarios execution. If the injected object is implemented IDisposible, they will be disposed after the scenario execution.
•	Within one scenario execution, same instance of the object will be shared across the step definitions.
===============================================================================================