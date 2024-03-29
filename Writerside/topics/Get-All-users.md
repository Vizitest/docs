# Get all users - a simple GET request

## Steps

To follow this example yourself, please install the [Test Server](The-Test-Server.md).

Our first test is very basic. We'll just get a list of all users. 

### Create test configuration
[Create a test configuration](Adding-a-test-configuration.md) called **Get all users** in the Test Manager. Hover on the new test configuration and press the pencil icon to open it in the Test Editor. 

<img src="get-all-users-tm.png" alt="edit test configuration" width="400"/>

### Create an endpoint test
Press the large blue + button and select the server you want to test against. We only have one, so select it.

<img src="get-all-users-empty.png" alt="add endpoint test" width="800"/>

Vizitest now adds two components. 

<img src="get-all-users-added.png" alt="added endpoint" width="800"/>

- On the left is the **Referencer component**. This references the API Configuration and shows the selected server as well as headers, cookies and security defaults. You can select any of these to be included in your test.
- On the right is the **Endpoint component**. This is where the bulk of the configuration takes place.

### Anatomy of the Endpoint component
Double click the header of the Endpoint component to zoom in on it. 

<img src="get-all-users-endpoint.png" alt="endpoint anatomy" width="800"/>


   1. An automatically generated unique name. You can rename this.
   2. The API configuration name.
   3. The Method type (GET, POST, DELETE, PUT, PATCH).
   4. The endpoint path. Will always start with a / even if you don't explicitly add it.
   5. The Quick Play button that executes the endpoint with the first value in each configured request.response section.

<img src="endpoint-buttons.png" alt="endpoint buttons" width="400"/>

- **Execute** - executes test cases. If you have just configured the endpoint, then it will be called and the results shown. If you have previously generated test cases, then all test cases are executed and all results shown.
- **Instant Configuration** - this is a very powerful and major time saving feature. [Click here](Instant-Configuration.md) for more information.
- **Test Case Table** - this hides or shows the test case table.
- **Help** - open the help drawer where you will find a video and useful docs links.

### Set REST method and Path
Modify the Endpoint **method** and **path**. We'll use a ```GET``` request and ```users``` as the path.


### Execute
Press the **Execute** button (see above) to test your endpoint. As soon as you do this, the results of the request will appear in the Execution Results component. 

You can clearly see the request and response data.

<img src="get-all-users-results.png" alt="quick play results" width="800"/>

- Click anywhere in the top level row to expand and collapse the details.
- You can click the blue Endpoint name to zoom directly to the Endpoint component.

We'll try something more adventurous in the next example.

