# Instant Configuration

This powerful features carries out the following operations in a single button press.

1. Automatically generates test cases based on your request setup. You will find the generated test cases in the Test Case Table below the Endpoint component. If the Test Case Table is not visible, it will be upon completion of this operation.
2. Executes all of those test cases against the endpoint URL
3. It set the expected response values in the test case table.

When you press the button, you will be shown the following dialog.

<img src="instant-configuration.png" alt="instant configuration dialog" width="400"/>

The checkboxes let you specify which expected values you want to set as expected values and therefore test against.

By default, it will only generate expected values for the response status code.

## Example
Using the [Check Credit configuration](Check-Credit.md) we can see this action.

Here's how the endpoint component is configured. The **Instant Configuration** button is circled.

<img src="cc-endpoint-instant-config-circled.png" alt="instant configuration endpoint" width="800"/>

Below is an example of the canvas after you have run the Instant Configuration.

<img src="cc-instant-configuration-result.png" alt="instant configuration result" width="800"/>

You can see

- The **Test Case Table** - several automatically generated test cases (scrollable). Note how the status code was automatically set based upon the actual response received when the test case was automatically run.
- The **Execution Results** - there is an entry for each test case execution. You can click on each row to see the full request and response details.

