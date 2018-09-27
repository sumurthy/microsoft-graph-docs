# Workbook resource type
 
Workbook is the top level object which contains related workbook objects such as worksheets, tables, ranges, etc.
 
## JSON representation
 
Here is a JSON representation of the resource
 
<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbook"
}-->
 
```json
{
  "names": [{"@odata.type": "microsoft.graph.workbookNamedItem"}],
  "tables": [{"@odata.type": "microsoft.graph.workbookTable"}],
  "worksheets": [{"@odata.type": "microsoft.graph.workbookWorksheet"}],
  "comments": [{"@odata.type": "microsoft.graph.workbookComment"}]
}
```
 
## Properties
None
 
## Methods
 
| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[**List comments**](workbook_list_comments.md) |[WorkbookComment](workbookcomment.md) collection| Get a comment object collection.| 
 
## Relationships
| Relationship | Type     |Description|
|:---------------|:--------|:----------|
|**comments**|[WorkbookComment](workbookcomment.md) collection|Represents a collection of comments associated with the workbook. Read-only.|
```
