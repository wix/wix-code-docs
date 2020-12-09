# Error Handling

What can we say, sh*t happens!  (JUST KIDDING, THIS IS A TEST)

## About Corvid Errors

### Types of Errors


#### HTTP Errors
4xx Client errors... fix your mistake
5xx Server Errors... contact support

These break into application errors, validation errors... 

#### Corvid Server Errors (or can these also be called "domain errors?")


#### Javascript Errors 

### What Info Do You Get

My wish list! 

{
 "code": "402",
 “text”: “Payment Required”, 
 "message": “<short text>”,
 “description”: “<long text>”, 
 “severity”: “error”|“warning”|“info”,
 “type”: “validation”|“application”|“system”|“server”|“js”,
 “validationIssue”: “Invalid Email”  \\ If “type” is “validation”,
 “application” : “Bookings”|“Stores”|“Editor Elements”|”General”,
 "infoURL" : <link to docs>
}

### Where You See Them

Corvid console and Browser Developer Tools

### How to Catch Them in Your Code

You can handle errors by adding a `catch()` in your code, such as at the end of a then() chain. 
The `catch()` receives the error.

    import wixData from 'wix-data';

    $w.onReady( function () {
      wixData.query("myCollection")
        .find()
        .then(results => $w("#myTable").rows = results.items)
        .catch(error => {
            // handle your error here
            switch(expression) {
              case x:
                  // code block
                  break;
              case y:
                  // code block
                  break;
              default:
                  // code block
         }
        } );
    } );


## Handling Standard HTTP Error Codes

| Status Code | Text              | Message                                       |
| ------ | -----------------------  | ---------------------------------------------- |
| 200  | OK                       | Success! |
| 400  | Bad Request              | One or more parameters is incorrect, missing, or did not pass validation for some other reason. |
| 401  | Unauthorized             | The system was not able to authenticate.|
| 403  | Forbidden                | Authenticated succeeded but the correct permissions are lacking. |
| 404  | Not Found                | The entity is not found or does not exist. |
| 409  | Conflict                 | The entity already exists. |
| 429  | Too Many Requests        | Resource usage was exhausted. |
| 500  | Internal Server Error    | A Wix internal error occurred. Try again later. |
| 501  | Not Implemented          | This API is not yet available. |
| 503  | Service Unavailable      | The API/Server is temporarily unavailable. Try again later. |
| 504  | Gateway Timeout          | The API did not respond in a timely manner. Try again later. |



## Handling JavaScript Errors

Explaining JavaScript errors is out of scope --- see <link>.


## Handling Corvid Server (API-specific) Errors

In addition to standard errors available to all APIs, some APIs will issue their own errors. 

See the return values for each API. 

![alt_text](../media/gettingStarted2.png)


