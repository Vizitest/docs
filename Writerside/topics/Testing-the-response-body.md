# Testing the response body

You can run a test on the response body. 

## Steps

### Setup
- [Create a test configuration](Adding-a-test-configuration.md) called **Final users check** in the Test Manager. 
- Open it in the Test Editor.
- In the Test Editor canvas, press the large blue + button and select the server.
- Set the method to ```GET``` and set the endpoint path to ```users```.

<img src="response-body-config.png" alt="endpoint configuration" width="800"/>

### Execute
- Run the test with the green Quick Play button and examine the results.

<img src="response-body-first-run.png" alt="test results" width="800"/>


### Copy JSON
- Copy the JSON received in the response body by pressing the copy icon (circled above).
- Press the blue Endpoint pill to zoom to the Endpoint component.
- In the Endpoint component, hover on the RESPONSE DATA section and press the **+Response Data** button. Paste the JSON you just copied into the JSON value field.

<img src="response-body-json-response.png" alt="reconfigured json response" width="800"/>

### Test Case Table
- Ensure the test cases are shown by pressing the Show Test Cases in the top of the Endpoint or Executions results component.
- In the Test Cases component, in the BODY row, click on **-- don't test --** and select the value you just added.
- Select ```200``` for the expected status code.

<img src="response-body-tct.png" alt="test case configuration" width="600"/>

### Run test case
- Run the test case and it should pass.
- Note the two values we tested for are green, indicating the expected response was received.
- If you make a small change to the expected response body data and run again, it should fail. Change the data back again to the correct value for the next example.

<img src="response-body-second-run.png" alt="test case configuration" width="800"/>
