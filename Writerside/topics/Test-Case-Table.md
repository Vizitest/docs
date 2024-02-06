# Test Case Table

The Test Case Table displays all test cases and the associated request and response values used.

## Anatomy
<img src="cc-test-case-table.png" alt="test case table" width="800"/>

1. **Test case column** - there will always be at least one test case. Vizitest populates the first test cases with the first value from each response section.
2. **Execute All** - executes all test cases and displays the requests and responses in the Execution Results component.
3. **Execute Test Case** - executes this test case only displays the request and response in the Execution Results component.
4. **Request Sections** - these are automatically picked up from any configured request sections in the endpoint component.
5. **Request Values** - for each request values, the chosen request value is disiplayed. If yo udon't want to test a particular value, you can click on it and select **don't test** from the dropdown. Note that required values will need to have a value selected.
6. **Response Section** - these are automatically picked up from any configured response sections in the endpoint component.
7. **Don't Test for row** - press this button to set the expected response values to **don't test** for the entire row.
8. **Auto generate test cases** - this will automatically generate new test cases. If you have already run an [Instant Configuration](Instant-Configuration.md) then this will have no effect. However, if you have added new values to the endpoint, then this will augment the test case table with any new cases it sees as missing.
9. **Add single test case** - adds a single test case. You will then need to set the request and response values to use for that case.
10. **Delete all test cases** - deletes all test cases. It will leave one test case remaining, which will be set to the first value for each request item.
11. **Scroll** - this indicates that there are more test cases to the right. Click to scroll You can also use your touchpad. There is a corresponding scroll indicator on the left side.



