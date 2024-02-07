# Check Credit

Let's create a new test configuration that tests the endpoint ```/check-credit``` in our [Test Server](The-Test-Server.md).

<note>
We will use this configuration in the following pages in this section to demonstrate Vizitest's testing capabilities.

To see the simple logic for this endpoint, please look at ```/play-server/server/routes/check_credit.py``` in the source code.
</note>

From the Test Manager, create a new test configuration called **Credit Check** and edit it.

Press the blue + button to add a new endpoint component.

Go to the QUERY PARAMETERS section and add three query parameters by clicking on the **+ Query Parameter** button that appears when you hover over the green title bar.

- **age** (integer)
- **credit-sought** (number)
- **duration** (integer)

Add the values as shown in the screenshot below. Hover over the parameter row and press the **+ Group** to add the invalid group.

<img src="cc-endpoint-config.png" alt="add request body" width="800"/>

## Execute
Press the Execute button (first icon on the buttons group). This will execute the first endpint using the first value from each query parameter. You should see the following output.

<img src="cc-execute-tc1.png" alt="execute basic test case" width="800"/>




