# Adding another Test Case

Let's now go back to our Add new user test and do some more testing.

This time, we are going to create a test that tests adding the same new user twice. 

The first test cases should successfully create a new user, assuming there was. The second case, which will use tha same request body, should fail as the user id will now exist.

This test assumes that the server data was reset beforehand as explained on the previous page.

## Steps

### Reset the user data
Open and run the Reset user data test, so we have a clean starting point.

### Open the 'Add new user' test
Open the Add new user test. The Endpoint component should already look like this.

<img src="add-test-case-endpoint.png" alt="endpoint component" width="800"/>

### Add a new test case
**Before** you run the test, we will add a new test case. To do this, press the + icon in the top of the **Test Cases** component.

<img src="add-test-case-new-case.png" alt="Add new test case" width="800"/>

### Configure the new test case
We will now configure the test, as shown below, to expect 
- ```200``` from **Test Case** and 
- ```409``` from **Test Case 1**.


<img src="add-test-case-configured.png" alt="configure new test case" width="800"/>

<tip>
    <p>
        Feel free to rename the test cases by clicking on the test case name at the top of each column.
    </p>
</tip>

### Run all test cases
You will see a **>All** button in the left most column. This will run all the tests in the test case table. Press it, and you should see that both tests have passed.

<img src="add-test-case-run-all.png" alt="execute all test cases" width="800"/>

In the Execution Results table, click anywhere in a row to expand or collapse the request and response data in detail. 

### Run again to see a failed test case
Now run all test cases again. 

- The first test case fails, as the user already exists after the first run. 
- The second test case passes as it was **expecting** it to fail with a ```409```.

<img src="add-test-case-run-all-again.png" alt="execute all test cases" width="800"/>


