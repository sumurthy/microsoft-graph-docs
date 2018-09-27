# workbookComment resource type
 
Represents a comment associated with the workbook.
 
 
## Methods
 
| Method                             | Return Type |Description|
|:---------------|:--------|:----------|
|[Get Comment](comment_get.md) | [WorkbookComment](workbookcommennt.md) |Read properties of Comment object.|
|[Create reply](workbookcomment_post_replies.md) |[WorkbookComment](workbookcomment.md)| Create a new reply on the comment thread.|
 
## Properties
| Property             | Type              |Description|
|:---------------|:--------|:----------|
|id|string|Unique ID associated with the comment. Read-only.|
|content|string|Comment content in the specified format.|
|contentType|string|Indicates format type of the comment content. Could be `plain`, `markdown`, or `delta`|
 
## Relationships
| Relationship | Type     |Description|
|:---------------|:--------|:----------|
|replies|[WorkbookComment](workbookcomment.md) collection|Represents a collection of comment replies. Read-only.|
 
## JSON representation
 
Here is a JSON representation of the resource.
 
<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookComment"
}-->
 
```json
{
  "id": "String (identifier)",
  "name": "String",
  "content": "String",
  "contentType": "String"
}
 
```
