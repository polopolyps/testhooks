testhooks
=========

Contains hook interfaces for tasks to be carried out before and after tests. Used as a bridge between testbase and other test frameworks to inject code before and after tests are run.

Example:

To create a hook that is executed before tests are run implement the interface method BeforeTestHook.doBeforeTest() and add the code that you need inside that method. Then, using the ServiceLocator pattern, add a file named com.polopoly.test.hooks.BeforeTestHook in the META-INF/services folder of your Testbase plugin module. In this file, enter the implementation classes of the BeforeTestHook interface (there can be several entries). 

Test base will automatically instantiate the classes declared in this file using the ServiceLocator pattern and execute your code before the test is run. 
