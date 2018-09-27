# Create comment reply
Use this API to create a new reply comment on the comment thread.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).
 
|Permission type      | Permissions (from least to most privileged)              |
|:--------------------|:---------------------------------------------------------|
|Delegated (work or school account) | Files.ReadWrite    |
|Delegated (personal Microsoft account) | Not supported.    |
|Application | Not supported. |
 
## HTTP request
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/comments/{id}/replies
 
```
## Request headers
| Name       | Description|
|:---------------|:----------|
| Authorization  | Bearer {token}. Required. |
| Workbook-Session-Id  | Workbook session Id that determines if changes are persisted or not. Optional.|
 
## Request body
In the request body, supply a JSON representation of [WorkbookComment](../resources/workbookcomment.md) object.
 
## Response
 
If successful, this method returns `201 Created` response code and [WorkbookComment](../resources/workbookcomment.md) object in the response body.
 
## Example
##### Request
Here is an example of the request.
<!-- {
  "blockType": "request",
  "name": "create_reply"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/comments/123456789/replies
Content-type: application/json
Content-length: 81
 
{
  "comment": "This is a test reply.",
  "format": "plain"
}
```
In the request body, supply a JSON representation of [WorkbookComment](../resources/workbookcomment.md) object.
##### Response
Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookComment"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 81
 
{
  "id": 99,
  "comment": "This is a test reply.",
  "format": "plain"
}
```