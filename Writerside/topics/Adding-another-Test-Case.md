# Adding another Test Case

Let's now go back to our POST Add user test and do some more testing.

This time, we are going to create a test that tests addin a new users twice. The first test cases should successfully create a new users. The second case, which will use tha same request body, should fail as the user id will now exist.

This test assumes that the server data was reset beforehand as explained on the previous page.

Open the test configuration from the **recents** list of by going back to the Test Manager.

1. Your Endpoint component should now look like this. We configured this in the [POST a new user](POST-add-new-user.md) example.
2. Make sure the Test Case Table is shown, which it should be already. If not, press the **Show Test Cases** button in the Endpoint or Execution Results component. We configured this In the [Basic Testing](Basic-Testing.md) example. 
3. Before you run the test, we will add a new test case. To do this, press the + icon in the top of the **Test Cases** component.
4. We will now configure the test so expect a ```200``` from **Test Case** and a ```409``` from **Test Case 1**. Feel free to rename the test cases to anything you like by clicking on the test case name.
5. You will see a **>All** button in the left most column. This will run all the test in the test case table. Press it and you should see that both tests have passed.
6. In the Execution Results table, click anywhere in a row to expand or collapse the request and response data in detail. 
7. Now run all test cases again. This time, the first test case fails, as the user already exists. The second one passes as it was expecting it to fail with a ```409```.



