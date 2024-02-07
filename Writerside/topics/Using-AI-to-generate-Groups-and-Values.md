# Using AI to generate Groups and Values

It can be helpful to ask Vizitest to generate group and value suggestions for your endpoint path and query parameter values.

If you look at the example below, you will see that the age parameter only has one group (Valid) and one value (30).

<img src="ai-endpoint-basic.png" width="500" alt="Endpoint"/>

Inside the highlighted box you will see the **AI** button. Press this to open the AI generation dialog.

<img src="ai-generation-dialog.png" width="600" alt="AI generation dialog"/>

## AI Generation Dialog
Vizitest passes the parameter name and its type to the AI. You can also provide additional information to provide more context.

### Instruction
If the parameter name (age in our example) is ambiguous then enter a short description in this field to help the AI understand the general context of the parameter. 

For example, if the parameter was called ```id``` and it was expected to contain UUIDs, then you might enter **Contains UUIDs**.

### Groups and Values
Indicates how many groups will generated and the maximum number of values in each group. You won't need to use all of these 

### Boundaries
You will often want to test boundary values for a parameter. For example if the minimum valid age is 18 and the maximum is 100, then you can ask the AI to generate values around these values.

### SQL Injection
Check the box if you want to generate SQL injection values.

## AI Results Dialog
When you press the Generate button, Vizitest will generate values and groups.

<img src="ai-results-pre.png" width="600" alt="AI generation results pre save"/>

You can now add items to the right hand column. Any values already configured in the endpoint component will be pre-populated.

- You can drag and drop or double click groups to add them to the right column.
- You can drag individual values anywhere.
- You can delete groups and values using the trash icon.

<img src="ai-results-post.png" width="600" alt="AI generation results pre save"/>

The final result might look like this for the age example. Note how we have not taken all groups and values. We have just added the ones that we think are useful (see below).

## Avoid too many groups and values
It makes sense to only include useful groups and values. If add unnecessary or redundant values and you use the Instant Configuration or Automatic test case generation, then you can end up with a large number of test cases. This will result in longer execution times when you run all test cases.

## The final result
When you press save, the groups and values from the right column are transferred to the endpoint component.

<img src="ai-endpoints-post.png" width="400" alt="AI generation results pre save"/>

