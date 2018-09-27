# Document comments

Office documents allow comments to be added to parts/sections of the documents. So far, the comments have been part of the document with limited interactive capability. 
A new initiative is trying to make commenting aspect of document more accessible to external applications and hence make commenting more modern and interactive. 
- RAM (Reply-At-Mention) will allow @mentions to trigger emails to mentioned person and in-turn allow that person to reply to the comment and persist the reply in the document. 

Above interactions require following additions to REST APIs
- Addition of PowerPoint and Word APIs to MS Graph service 
- Introduction of modern commenting APIs to Excel, Word and PowerPoint documents

## API scenarios 
For the current scope, we want to enable commenting APIs at the document level and addition of comments in a generic fashion that allows for common pattern across Excel, Word and PowerPoint.

1.	Read Comments collection at document level (comment threads).
2.	Get comment (comment thread).
3.	Reply to comment (comment can only have 1 level of nesting – parent/child).

## Usage 

1.	From within the application, user will @mention a colleague with an ask/question.
2.	Document places comment thread in the @mention location and notifies ODSP of comment request action.
3.	That triggers an email through ODSP framework into mentioned contact’s inbox with context and comment-reply information  within the document. The comment `id` is provided along with the email. 
4.	Email response with comment will trigger a workflow that’ll insert a comment reply to the specific comment thread.

## Roadmap

For the time being, the requested APIs are intended for first party consumption only. In the future these APIs will be available for external developers. 


