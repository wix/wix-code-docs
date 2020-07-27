# Error Handling

What can we say, sh*t happens!  (JUST KIDDING, THIS IS A TEST)

## About Corvid Errors

### Types of Errors

#### HTTP/RPC Errors
4xx Client errors... fix your mistake
5xx Server Errors... contact support

#### Corvid Server Errors


#### Javascript Errors 

### What Info Do You Get




### Where You See Them
### How to Catch Them in Your Code

## Standard Codes

| Code   | Text              | Message                                       |
| ------ | -----------------------  | ---------------------------------------------- |
| `200`  | OK                       | Success! |
| "400"  | Bad Request              | One or more parameters is incorrect, missing, or did not pass validation for some other reason. |
| 401  | Unauthorized             | The system was not able to authenticate you.|
| 403  | Forbidden                | You are authenticated but you do not have permissions. |
| 404  | Not Found                | The entity is not found or does not exist. |
| 409  | Conflict                 | The entity already exists. |
| 429  | Too Many Requests        | Resource usage was exhausted. |
| 500  | Internal Server Error    | A Wix internal error occurred. Try again later. |
| 501  | Not Implemented          | This API is not yet available. |
| 503  | Service Unavailable      | The API/Server is temporarily unavailable. Try again later. |
| 504  | Gateway Timeout          | The API did not respond in a timely manner. Try again later. |


## API-specific Errors

In addition to standard errors available to all APIs, some APIs will issue their own errors. 

See the return values for each API. 

![alt_text](../media/gettingStarted2.png)


