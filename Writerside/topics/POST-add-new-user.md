# Add new user - a POST request

It will help if you've already read the Get all users example on the previous page.


## Create test configuration
[Create a test configuration](Adding-a-test-configuration.md) called **Add new user** in the Test Manager then open it in the Test Editor.

## Create an endpoint test
In the Test Editor canvas, press the large blue + button and select the server you want to test against. You probably only have one at this point, so click it.

## Set REST method
In the top of the Endpoint component, click the Endpoint **method** (GET by default) and select ```POST```.

## Set the Path
The endpoint for adding a new user is ```user/{uid}``` where uid is a string value which will be the ID assigned to our new user. Enter ```user/{uid}``` in the header. 

The Endpoint component should now look like this.

You'll notice a path variable has automatically been created and a default equivalence class **Valid** has been created with a default value of ```default```. We'll explain equivalence classes in a later example.

Click in the value field and change from ```default``` to some uid (string) for our new user. Try ```abc-123```.

<img src="add-user-header.png" alt="added endpoint with method and path" width="800"/>

## Quick Play
Press the green Quick Play icon in the top of the Endpoint component to test it. You will get an error because we did not provide a body.

<img src="add-user-no-body.png" alt="added endpoint with method and path" width="800"/>


## Set the Body
POST requests require a body, so let's provide one. Hover over the Body section and press the **+Body** button that appears. This will add a default equivalence class and a default value.

<img src="add-user-body-add.png" alt="add request body" width="500"/>

Click in the JSON field and enter ```{"name":"Mary","surname":"Meadows"}```. 

<img src="add-user-body-json.png" alt="added empty body" width="800"/>

## Quick Play again
Press the play button again. You should now see a ```200``` status code in the Execution Results as well as ```Mary Meadows``` in the response body.

<img src="add-user-added-result.png" alt="add request body" width="800"/>


## Check Get all users
From the recents list in the left sidebar, go back to the **Get All Users** test configuration and run it again. You should see ```Mary Meadows``` in the returned list.
