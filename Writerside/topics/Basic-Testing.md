# Basic Testing

Up to now, we've not really tested. We've just called an endpoint with some data and seen what response we got back.

We'll now look at an actual test, albeit a very simple one.

1. With the **POST Add user** test configuration opened, press the green play button again and examine the Execution Results component. You'll see we got a ```409``` status code as the user id already exists.
2. In either the Endpoint or Execution Results component, press the Show Test Cases button. At this point the Test Case Table will appear. You'll notice that the request values are already selected. However, the Expected Response values have not been set. The value in the STATUS CODE row is marked as **-- don't test --**. 
3. Click on this and select the Valid value of 200.
4. You can now run this Test Case by pressing the green play button at the top of the test case column (or by pressing the green button in the Endpoint component).
5. In the Execution Results component, you can now see that the test failed. Hover over the red icon in the Response - Status code section and it will tell you it expected a 200 (but it got a 409). 

## Adding an Invalid equivalence class
We'll now discuss equivalence classes for the first time. They are simple but very powerful in a testing context.

The idea is that the Valid equivalence class contains all possible valid responses. But what about invalid ones?

1. We can add a new **Invalid** equivalence class in the Endpoint component by hovering over the top row, as shown below, and pressing the **+Equivalence Class** button. A popup will appear and you can choose between **Valid** and **Invalid**. Choose **Invalid**. 
2. You can now see that the new class has been created with a default value. Edit this value and change to ```409```.
3. Run the test again and you can see that the test case expected a ```409``` and got a ```409``` as expected, so the test passed.
