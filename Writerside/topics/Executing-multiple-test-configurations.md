# Executing multiple test configurations

You can execute multiple test configurations sequentially from the Test Manager.

This allows you to manage setup and tear down so that tests can reliably execute.

A good example of this is where you test the adding of a new user. If the user already exists, then you will get an error when you run the same **Add new user** test twice.

To avoid this, you can have a test configuration that resets the data just before the **Add new user** script executes. 

## Steps

### Test Manager Groups
To use this, you should create a group in the Test Manager that contains the sequentially arranged test configurations.

You can reorder your test configurations by hovering over an item and then dragging it into position.

Below is an example that contains the scripts we created earlier. Drag the test configurations into the order shown below.

<img src="tm-all-tests-group.png" alt="Test manager group" width="400"/>

### Execute
Press the play button (circled above) to execute all tests in the Group. They will execute in sequence and once complete, you will see a report. Each test configuration is listed at the top level.

<img src="tm-all-tests-run-1.png" alt="Execution report" width="800"/>

You can drill down to see full details.

<img src="tm-all-tests-drill-down.png" alt="Execution report" width="800"/>

### Errors
If any of the test configurations failed, you will see a red icon. We can demonstrate this by changing the order of the test configurations.

<img src="tm-all-tests-group-fail.png" alt="Test manager group for deliberate fail" width="400"/>

Drag the delete test as shown above, so it follows the data reset. At this point, we will not have added the new user that we subsequently delete.

Run the test and you will see the following report.

<img src="tm-all-tests-fail.png" alt="Execution report" width="800"/>

Note how the **Delete user** test failed and also the **Final users check**, as it eas expected that user added by **Add new user** was subsequently deleted.
