# DELETE a user

This test will delete a user by its id. 

To set this up correctly, first run the [Resetting server data test](Resetting-server-data.md) we created earlier and then the [POST a new user](POST-add-new-user.md) test.

We'll later look at how you can automate the [setting/resetting from a Test Manager Group](Running-all-group-tests.md).

1. [Create a test configuration](Adding-a-test-configuration.md) called **Delete user** in the Test Manager and open it in the Test Editor.
2. Select the DELETE method and set the endpoint path to ```user/abc-123```, where ```abc-123``` is the id of the user that gets created in the **POST Add user** test. Note that you could also set the path to ```user/{uid}``` and then set the path variable to ```abc-123``` in the PATH VARIABLES section.
3. You can now execute the test in the normal way and the user should be deleted.
4. Open the [GET all users](Get-All-users.md) test to check it is really deleted.
