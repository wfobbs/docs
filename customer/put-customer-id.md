<!--
@title PUT customer/:id
@author Moltin Ltd
@description Updates a customer with the given ID

@sidebar 1
@family Customer
@rate No
@auth Yes
@format JSON
@http PUT
@version beta
-->
This call edits a customer with a given ID. There are no minumum required paramaters and only those differing from current values will be updated, as such you can pass all or one of the fields and there will be no difference.


#### Resource URL
PUT [{{ url }}customer/:id]({{ url }}customer/:id)


#### Paramaters {#paramaters}
Key | Type | Description
--- | ---- | -----------
first_name*optional* | String | The customer's first name
last_name*optional* | String | The customer's last name
email*optional* | String | The customer's email

<!--code-->
#### Example Successful Response  {#success}
``` json
{
  "status": true,
  "result": {
    "id": "142",
    "first_name": "John",
    "last_name": "Moltin",
    "email": "john@example.com",
    "history": {
      "orders": 0,
      "value": 0
    }
  }
}
```


### Example Failed Response {#error}
``` json
{
  "status": false,
  "errors": [
    "'johnatexample.com' is not a valid email address"
  ]
}
```
<!--/code-->