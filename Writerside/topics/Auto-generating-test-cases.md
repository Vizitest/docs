# Auto generating test cases

We'll now create a more interesting test using multiple equivalence classes and values and asking Vizitest to generate the test cases for us.

## Create a test with query parameters

1. [Create a test configuration](Adding-a-test-configuration.md) called **GET Query users** in the Test Manager.
2. Open it in the Test Editor and press the large blue **+** button to create a test.
3. Set the Endpoint component to ```GET``` and the path to ```users```.
4. Add a new query parameter by hovering on the QUERY PARAMETERS bar and pressing **+Query Parameter**.
5. Change the parameter name to surname.
6. Modify the existing value to Brook and run the test. You should get a ```200``` response.
7. Now add another valid value ```Packer```.
8. Create an Invalid equivalence class and change the value to ```xxxxx```.
9. In the response's STATUS CODE section, create equivalence classes and values as shown below.

## Generating Test Cases
We can now let Vizitest create test cases for us. 

1. Make sure the Test Case Table is shown. If it's not, press the **Show Test Cases** button in the Endpoint or Execution Results component.
2. As always, there is always a Test Case present with the first Request values pre-selected. Press the suitcase icon to have Vizitest generate test cases for you. It uses an algorithm to combine request values to give a set of test cases, which can then be edited.
3. You should examine each test case and select the expected output for each case. It should look like this. 
4. Note that you can delete individual test cases by pressing the delete icon. You can also manually add new cases with the + icon. 
5. Press the **>All** icon to run all the tests and the Execution Results component will show you the results.

