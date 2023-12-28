# Resetting server data

For the purpose of working through some more examples, let's see how to reset our server data using a provided endpoint.

This will allows us to run tests that require the data to have been reset first. This will come into its own later, when [running all tests in a Test Manager group](Running-all-group-tests.md).

## Steps

### New test configuration
- [Create a test configuration](Adding-a-test-configuration.md) called **Reset user data** in the Test Manager.
- Open it in the Test Editor and press the large blue **+** button to create a test.

### Endpoint configuration
- In the Endpoint component header, set the method to ```POST``` and the path to ```reset```.
- Add a JSON body in the request section and set the JSON to just ```{}``` so we have a valid body to post.
- Press the green play button to execute the request.

<img src="reset-users-ep.png" alt="reset users endpoint setup" width="800"/>

### Results
In the Execution Results component, you should see a ```200``` response with the message ```{"message":"Data was reset"}```.

<img src="reset-users-result.png" alt="reset user test results" width="800"/>

If you now switch back to the Get All users test and run it, you should see two default users that were created by the reset.

