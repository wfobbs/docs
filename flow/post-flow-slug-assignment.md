<!--
@title POST flow/:slug/assignment
@author Moltin Ltd
@description Assign a new field to a flow
@order 15.9

@sidebar 1
@family Flow
@rate No
@auth Yes
@format JSON
@http POST
@version beta
-->
You can add new assignments to any flow, including the default Moltin flows.

#### Resource URL
POST [{{ url }}flow/:slug/assignment]({{ url }}flow/:slug/assignment)

#### Paramaters
Key | Type | Description
--- | ---- | -----------
name | String | The name of the field
slug | String | The field slug
type | String | The type of field
options*optional* | Array | The options for this field type
required*optional* | Choice (1 or 0) | Is this field required?
unique*optional* | Choice (1 or 0) | Should this field be unique?

<!--code-->
#### Example Successful Response
``` json
{
    "status": true,
    "result": {
        "slug": "description",
        "name": "Description",
        "type": "text",
        "options": [],
        "required": false,
        "unique": false,
        "locked": false,
        "order": null
    }
}
```

#### Example Invalid Slug Response
``` json
{
    "status": false,
    "error": "Flow not found"
}
```
<!--/code-->