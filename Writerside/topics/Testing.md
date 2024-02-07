# Testing

Vizitest excels at testing and automatically generating test cases. It's worth reading this section carefully.

There are various options available to you. These are explained in more detail on the next tow pages.

## Instant Configuration
This is a very powerful feature that can save a lot of time. With a single button press it generates test cases, executes the endpoint call for each one and, finally, sets expected response values.

## The Test Case Table
This is a canvas component that handles all test cases and each one's request and expected response settings.

## Generate Test Cases
This performs the same action as the first step of the Instant Configuration. This does not need to be used if you have already run the Instant Configuration unless you add new values to the request data. Even then, you can re-rerun the Instant Configuration.

## Manually adding test cases
In some cases, you may want to create test cases individually. You can do this from the very start or after you've used the Instant Configuration feature or pressed the Generate Test Cases button.

## Delete Test Cases
You can delete test cases as follows.

- Delete all test cases.
- Delete a single test case.

## Setting expected response values
You can specify the values that each test case expects to receive. When the tests then execute, it will use expected response values to evaluate the response and manage the actual assertion.

## Resetting expected response values
You might want to reset one or all expected response values in the test case table back to the **don't test** state.