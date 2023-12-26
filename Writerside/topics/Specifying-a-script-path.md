# Specifying a script path

You can specify a script path for the **Request** and/or the **Response**. The scripting checkbox is found at the bottom of the Endpoint component request and response sections.

## Specifying a Request/Response script
If you want your script to be called before the test cases are run, check the **Request script** box and then specify the path to the script in the provided input field.

The Response script is called once the tests have been run. You will have access to the response data and can then examine or manipulate the data in order to handle your own test assertions.

If your script can be found in your projects ```/scripts folder``` (recommended), then the path is treated as relative. An absolute path can be provided, however.

You also do not need to specify a script name, in which case Vizitest will expect to find a script called ```index.js``` or ```index.ts```.

If you are using any language other than Javascript or Typescript, then you should provide the name of the script executable.

If checked, Vizitest will call the script just before and/or just after then API calls have been made for all test cases. 

## Request manipulations
You are free to inspect the request test cases data that will be executed. At this point you could

- Write information to a file for post execution examination.
- Read information from environment variables and modify the request data.
- Remove and add test cases as you require.

If you want Vizitest to work with manipulated test case data, then you should write the manipulated test case data to ```stdout``` and return a 0 process code. Otherwise just exit with a 0 process code with nothing written to ```stdout```.

## Response manipulations
Once Vizitest has run all test cases, your script will be called with the --response argument followed by the accompanying JSON data. 

At this point you can examine or manipulate the response data. You might

- Read information from a file or database to help determine an expected outcome.
- Modify the response data or expected data accordingly.
- Set the ```result.successful``` flag to ```true``` or ```false``` so it can be reviewed in the **Api Execution Results** table in the Vizitest UI. 

If you want Vizitest to work with manipulated test case response data, then you should write the manipulated test case data to  ```stdout``` and return a 0 process exit code. Otherwise just exit with a 0 process code with nothing written to ```stdout```.

