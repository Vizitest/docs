# Testing the response body

You can run a test on the response body. 

1. [Create a test configuration](Adding-a-test-configuration.md) called **Final users check** in the Test Manager. Hover on the new test configuration and press the pencil icon to open it in the Test Editor.

2. In the Test Editor canvas, press the large blue + button and select the server you want to test against.
3. Set the method to GET and set the endpoint path to users.
4. Run the test with the green play button and examine the results.
5. You can copy the JSON received in the response body by pressing the copy icon.
6. In the Endpoint component, hover on the RESPONSE DATA section and press the +Response Data button. Paste the JSON you just copied into the JSON value field.
7. Open the Test Cases component and in teh BODY row, click on -- don't test -- and select the value you just added.
8. Run the test case and it should pass.
9. If you make a small change to the expected response body data and run again, it should fail. Change the data back again to the correct value for the next example.

