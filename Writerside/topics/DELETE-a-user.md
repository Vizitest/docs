# Delete a user

This test will delete a user by user id. 

## Steps

### Prep
- First run the [Reset user data test](Resetting-server-data.md) we created earlier.
- Then the [Add new user](POST-add-new-user.md) test to add the user we are going to delete with this test.

We'll later look at how you can automate the [setting/resetting from a Test Manager Group](Running-all-group-tests.md).

### Configure Endpoint component
- [Create a test configuration](Adding-a-test-configuration.md) called **Delete user** in the Test Manager and open it in the Test Editor.
- Select the DELETE method and set the endpoint path to ```user/abc-123```, where ```abc-123``` is the id of the user that gets created in the **POST Add user** test.
<tip>
        Note that you could, instead, set the path to <pre><code>user/{uid}</code></pre> and then set the path variable to <pre><code>abc-123</code></pre> in the PATH VARIABLES section.
</tip>

<img src="delete-config.png" alt="configure endpoint component" width="800"/>

### Adjust the status code
Change the expected status code to ```204``` as shown above. 

### Test Case
- Create a test for this and test for the status code returning ```204```.

<img src="delete-tct.png" alt="test case table" width="600"/>


### Execute and review
- You can now execute the test in the normal way and the user should be deleted.
- If you run the test twice, you would get an error the second time as the user had already been deleted.
- Open the [Get all users](Get-All-users.md) test to check it is really deleted.

<img src="delete-execute.png" alt="test case table" width="600"/>