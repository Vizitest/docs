# Resetting server data

For the purpose of working through some more examples, let's see how to reset our server data.

1. [Create a test configuration](Adding-a-test-configuration.md) called **POST Reset data** in the Test Manager.
2. Open it in the Test Editor and press the large blue **+** button to create a test.
3. In the Endpoint component header, set the method to ```POST``` and the path to ```reset```.
4. Add a JSON body in the request section and set the JSON to just ```{}``` so we have a valid body to post.
5. Press the green play button to execute the request.
6. In the Execution Results component, you should see a ```200``` response with the message ```{"message":"Data was reset"}```.
7. If you now swtch back the the GET All users test and run it, you should see two default users that were created when resetting.

