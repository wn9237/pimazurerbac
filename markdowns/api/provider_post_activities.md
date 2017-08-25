# Create activity

Use this API to create a new activity.
### Prerequisites
The following **scopes** are required to execute this API: 
### HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /providers/<id>/activities

```
### Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {code}|
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|

### Request body
In the request body, supply a JSON representation of [activity](../resources/activity.md) object.


### Response
If successful, this method returns `201, Created` response code and [activity](../resources/activity.md) object in the response body.

### Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_activity_from_provider"
}-->
```http
POST https://graph.microsoft.com/beta/providers('00000000-0000-0000-0000-000000000002')/providers/<id>/activities
Content-type: application/json
Content-length: 203

{
  "correlationId": "correlationId-value",
  "createdDateTime": "datetime-value",
  "expirationDateTime": "datetime-value",
  "operationType": "operationType-value",
  "resourceId": "resourceId-value"
}
```
In the request body, supply a JSON representation of [activity](../resources/activity.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.activity"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 223

{
  "id": "id-value",
  "correlationId": "correlationId-value",
  "createdDateTime": "datetime-value",
  "expirationDateTime": "datetime-value",
  "operationType": "operationType-value",
  "resourceId": "resourceId-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create activity",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->