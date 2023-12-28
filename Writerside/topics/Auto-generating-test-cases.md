# Auto generating test cases

We'll now create a more interesting test using multiple equivalence classes and values.

We'll then ask Vizitest to generate the test cases for us.

This example is fairly basic. If you have more equivalence classes and values, Vizitest's auto generation capability becomes more powerful as it calculates combinations to test.

This said, you should avoid creating unnecessary equivalence classes and values that do not actually add value, as these will require output value macthing and take longer to execute.

## Steps

### Create test

- [Create a test configuration](Adding-a-test-configuration.md) called **Query users** in the Test Manager.
- Open it in the Test Editor and press the large blue **+** button to create a test.
- Set the Endpoint component to ```GET``` and the path to ```users```.

### Add a query parameter
- Add a new query parameter by hovering on the QUERY PARAMETERS bar and pressing **+Query Parameter**.
- Change the parameter name to surname.
- Modify the existing value to ```Brook``` and press the green Quick Play button to run the test.
- You should get a ```200``` response.
- Add another valid value ```Packer```.

<img src="autogen-endpoint.png" alt="endpoint component" width="800"/>

### Add Invalid Equivalence Class for Query Parameter
- Create an Invalid equivalence class and change the value to ```xxxxx```.

<img src="autogen-invalid-query.png" alt="added invalid query equivalence class" width="800"/>


### Configure Status Code
- In the response's STATUS CODE section, create equivalence classes and values as shown below.

<img src="autogen-status-ecs.png" alt="Status code configuration" width="800"/>


### Generating Test Cases
We can now ask Vizitest to create test cases for us.

- Make sure the Test Case Table is shown. If it's not, press the **Show Test Cases** button in the Endpoint or Execution Results component.
- As always, there is a Test Case present with the first Request values pre-selected
- Press the suitcase icon to have Vizitest generate test cases for you. It uses an algorithm to combine request values to give a set of test cases, which can then be edited.

<img src="autogen-gen-cases.png" alt="generate test cases" width="800"/>


### Match response data
- You should examine each test case and select the expected output for each case. See the image below. 
- Note that you can delete individual test cases by pressing the delete icon. You can also manually add new cases with the + icon. Note that the e Positive 2 test cases does not need to be tested, so you could consider deleting it.
- Press the **>All** icon to run all the tests and the Execution Results component will show you the results.

<img src="autogen-match-cases.png" alt="match expected output" width="800"/>

