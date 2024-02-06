# Add new user - a POST request

It will help if you've already read the Get all users example on the previous page.

## Steps

### Create test configuration
[Create a test configuration](Adding-a-test-configuration.md) called **Add new user** in the Test Manager then open it in the Test Editor.

### Create an endpoint test
In the Test Editor canvas, press the large blue + button and select the server you want to test against. You probably only have one at this point, so click it.

### Set REST method
In the top of the Endpoint component, click the Endpoint **method** (GET by default) and select ```POST```.

### Set the Path
The endpoint for adding a new user is ```user/{uid}``` where uid is a string value which will be the ID assigned to our new user. Enter ```user/{uid}``` in the header. 

The Endpoint component should now look like this.

You'll notice a path variable has automatically been created and a default group **Valid** has been created with a default value of ```default```. We'll explain groups in a later example.

Click in the value field and change from ```default``` to some uid (string) for our new user. Try ```abc-123```.

<img src="add-user-header.png" alt="added endpoint with method and path" width="800"/>

### Execute
Press the Execute button (first icon on the buttons group). If you look at the execution result you will see you get a 415 error. This is because we did not provide a body with the new user's data.

<img src="add-user-no-body.png" alt="added endpoint with method and path" width="800"/>


### Set the Body
The POST requests requires a body, so let's provide one. Hover over the Body section and press the **+Body** button that appears. This will add a default group and a default value.

<img src="add-user-body-add.png" alt="add request body" width="500"/>

You will now see the following screen.

<img src="add-user-empty-json.png" alt="empty json" width="500"/>

Hover over the newly added, but empty, value and click on the pencil icon that appears. Click on the Raw tab and enter the following JSON :  ```{"name":"Mary","surname":"Meadows"}```.

<img src="add-user-enter-raw-json.png" alt="enter raw json json" width="500"/>

Press save to return to the canvas, where you will see the JSON in the value field. You can edit this at any time by pressing the pencil icon again.

<img src="add-user-body-json.png" alt="added empty body" width="400"/>

### Execute again
Press the **Execute** button again. You should now see a ```200``` status code in the Execution Results as well as ```Mary Meadows``` in the response body.

<img src="add-user-added-result.png" alt="add request body" width="800"/>


### Check Get all users
From the recents list in the left sidebar, go back to the **Get All Users** test configuration and run it again. You will now see ```Mary Meadows``` in the response body.
