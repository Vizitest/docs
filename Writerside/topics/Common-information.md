# Common information

The following information is common to all languages.

## Script creation and location
You can create your scripts in any location on your PC. However, it is recommended that you store your scripts in the main project folder in the /scripts folder provided. This is a convenient location so that scripts are properly checked into the Git repository.

## Requirements
You are free to create your script in any programming language. The only requirements are

- The script is callable from the command line.
- The process returns a ```0``` if successful or a ```1``` if unsuccessful.
- Your script accepts either ```-request``` or ```-response``` as an argument followed by an accompanying argument containing the corresponding JSON data.
- Your script returns the manipulated data, also in JSON format.

## Request
Your script should parse the ```-request``` argument followed by the JSON data provided by the Vizitest service. It will have the following structure.

TODO : Discuss and finalise request and response

``` JSON
{
  "testExecutions": [
    {
      "testCaseId": "31e99398-3ece-4089-99a3-e4b942fe582f",
      "request": {
        "pathVariables": [
          {
            "key": "firstName",
            "value": "John"
          },
          {
            "key": "lastName",
            "value": "Brook"
          }
        ],
        "queryParameters": [
          {
            "key": "firstName",
            "value": "John"
          },
          {
            "key": "lastName",
            "value": "Brook"
          }
        ],
        "body": {
          "body": { "name": "Freddy", "surname": "May" }
        },
        "dataMimeType": "application/json",
        "headers": [
          {
            "key": "header-1",
            "value": "header value"
          },
          {
            "key": "header-2",
            "value": "header value"
          }
        ],
        "cookies": [
          {
            "key": "cookie-1",
            "value": "cookie value"
          },
          {
            "key": "cookie-2",
            "value": "cookie value"
          }
        ],
        "security": []
      }
    }
  ]
}
```

## Response
The 


```JSON 
{
    "testExecutions": [
        {
            "testCaseId": "31e99398-3ece-4089-99a3-e4b942fe582f",
            "response": {
                "responseData": {
                    "status": 200,
                    "data": "{\"db-987\":{\"name\":\"Daniel\",\"surname\":\"Bauer\"},\"fm-123\":{\"name\":\"Freddy\",\"surname\":\"May\"},\"jf-666\":{\"name\":\"Jakob\",\"surname\":\"Faschinger\"},\"user1\":{\"name\":\"Max\",\"surname\":\"Mustermann\"},\"user2\":{\"name\":\"Franz\",\"surname\":\"Lohrbeerbaum\"}}",
                    "dataMimeType": "application/json",
                    "headers": [
                        {
                            "key": "Header1",
                            "value": "Python/3.10.6"
                        },
                        {
                            "key": "Content-Type",
                            "value": "application/json"
                        }
                    ],
                    "cookies": []
                },
                "expectedData": {
                    "status": 200,
                    "data": null,
                    "dataMimeType": null,
                    "headers": [],
                    "cookies": []
                },
                "result": {
                    "start": "2023-12-26T13:59:10.222Z",
                    "end": "2023-12-26T13:59:10.284Z",
                    "operationId": "",
                    "path": "/server/freddy/users",
                    "method": "GET",
                    "namedEndpointName": "Endpoint 1",
                    "testCaseName": "Test Case",
                    "successful": true
                }
            }
        }
    ]
}
```
