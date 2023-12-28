# Basic Testing

Up to now, we've not really tested. We've just called an endpoint with some data and looked at the response.

We'll now look at an actual test, albeit a very simple one.

## Steps

### Quick Play
With the **Add new user** test configuration opened, press the green play button again and examine the Execution Results component. 

You'll see we get a ```409``` status code. This is because the user id already exists from the last time we ran this test.

<img src="basic-testing-user-exists.png" alt="response data" width="800"/>

### Show Test Cases
In the Endpoint and Execution Results components is a **Show Test Cases** button. Press it and the Test Case Table will appear. 

<img src="basic-testing-tct.png" alt="test cases table" width="800"/>


### Response matching
You'll notice that the request values are already selected. However, the Expected Response values need to be set by the user.

- The value in the STATUS CODE row is marked as **-- don't test --**.
- Click on this and select the Valid value ```200```.

<img src="basic-testing-tct-status-set.png" alt="test cases table" width="800"/>

### Run Test Case
You can now run this Test Case by pressing the green play button (circled above) at the top of the test case column (or by pressing the green button in the Endpoint component).

In the Execution Results component, you can now see that the test failed. Hover over the red icon in the Response - Status code section and it will tell you it expected a 200 (but it got a 409). 

<img src="basic-testing-tct-execute-1.png" alt="test cases table" width="800"/>

### Adding an Invalid "Equivalence Class" to the Reesponse Status Code
We'll now briefly discuss equivalence classes. They are simple but very powerful in a testing context. We won't go into much detail as it's not really necessary at this stage.

For now, just think of an equivalence class as a set of values all of which belong to the parent and have the same meaning as the equivalence class name. 

Often you'll just be working with **Valid** and **Invalid** values. But you may want to have group your values in a more complex way later. This comes into its own if you want Vizitest to [auto-generate test cases](Auto-generating-test-cases.md) for you,

<img src="basic-testing-add-invalid-ec.png" alt="add invalid equivalence class" width="800"/>

We can add a new **Invalid** equivalence class tp the Status Code section in the Endpoint component.

- Hover over the top row with the section, as shown above and the **+Equivalence Class** button will appear. Choose **Invalid values** from the popup.
- You can now see that the new class has been created with a default value. Edit this value and change to ```409```.

<img src="basic-testing-set-invalid-ec-value.png" alt="set invalid value 409" width="800"/>

### Change expected Status Code
In the test case table, change the expected status code to ```409```.

<img src="basic-testing-change-expected-value.png" alt="changed expected value" width="800"/>


### Execute test again
From the test case table, Run the test again. You can see that the test case expected a ```409``` and got a ```409``` as expected, so the test passed.

<img src="basic-testing-passed.png" alt="test passed" width="800"/>


