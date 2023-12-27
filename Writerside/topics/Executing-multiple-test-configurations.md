# Executing multiple test configurations

You can execute multiple test configurations seuqentially from the Test Manager.

This allows you to manage setup and teardown exactly so that tests can reliably execute without unwanted errors.

A good example of this is where you test the adding of a new user. If the user already exists, then you will always get an error when you try to add the same user.

To avoid this, you can have one test configuration reset the data just before the Add user script executes. 

## Test Manager Groups
To use this, you should create a group in the Test Manager that contains the sequentially arranged test configurations.

You can reorder your test configurations by hovering over an item and then dragging it into position.

Below is an example that contains the scripts we created earlier.

## Execute
Press the play button to execute all tests in the Group. They will execute in sequence and once complete, you will see a report. Each test configuration is listed at the top level.

If any of the test configurations failed, you will see a red icon. 

You can drill down into each test configuration and the test case contained therein.






