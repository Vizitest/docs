# Splitting a test configuration

There are cases when it makes more sense to split a configuration into two or more configurations.

The Credit Check example is actually a good illustration of when this can make sense.

If you look at ```/play-server/server/routes/check_credit.py``` in the [Test Server](The-Test-Server.md) source, you will see the following logic.

```Python
if age<18:
        return {"msg": "We only offer credit to 18 and older"}, 400, CONTENT_TYPE_JSON

    if age>100:
        return {"msg": "We do not offer credit to anyone older than 100"}, 400, CONTENT_TYPE_JSON         
       
    if age<26: 
      if creditSought>1000: 
        return {"msg": "We only offer up to 1000 of credit for 18 to 25 year olds"}, 400, CONTENT_TYPE_JSON
      if duration>24:
         return {"msg": "We offer max 24 months of credit for 18 to 25 year olds" }, 400, CONTENT_TYPE_JSON
      return {"msg": "Credit approved!!!"}, 200, CONTENT_TYPE_JSON

    if creditSought>10000:
       return {"msg": "We only offer up to 10000 of credit if 26 or older"}, 400, CONTENT_TYPE_JSON
    if duration>48:
       return {"msg": "We offer max 48 months of credit if 26 or older" }, 400, CONTENT_TYPE_JSON
    
    return {"msg": "Credit approved!!!"}, 200, CONTENT_TYPE_JSON
```

You can see that there are different rules relating to ```credit-sought``` and ```duration``` depending on the age.

Testing this in a single test is difficult using Vizitest's Instant Configuration or Generate Test cases. The only way you could accomplish this is by creating all of the test cases manually.

To get around this, it is much easier to create two separate configurations in a Group in the Test Manager. You can then do thorough tests (boundary values) for each age range.

<img src="cc-split-1.png" alt="split test first endpoint" width="800"/>

Note how we are testing the age's boundary values. Using the Instant Configuration button, this will generate 8 test cass that test all relevant combinations.

<img src="cc-split-tct.png" alt="split test first endpoint" width="800"/>

You would then create a second test configuration to test the age range of ```26``` to ```100```.

## Running the tests from the Group
If you look at the following screenshot, you can see how we've created three tests in a Test Manager group. You can press the play button to execute all tests in the group.

<img src="cc-split-group.png" alt="split test group" width="300"/>

You will then see the following execution report. You can drill into the results.

<img src="cc-group-execution-results.png" alt="group execution results" width="800"/>

