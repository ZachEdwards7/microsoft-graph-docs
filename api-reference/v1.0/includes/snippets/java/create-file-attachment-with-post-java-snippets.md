---
description: "Automatically generated file. DO NOT MODIFY"
---

```java

IGraphServiceClient graphClient = GraphServiceClient.builder().authenticationProvider( authProvider ).buildClient();

Post post = new Post();
ItemBody body = new ItemBody();
body.contentType = BodyType.TEXT;
body.content = "Which quarter does that file cover? See my attachment.";
post.body = body;
LinkedList<Attachment> attachmentsList = new LinkedList<Attachment>();
Attachment attachments = new Attachment();
attachments.additionalDataManager().put("@odata.type", new JsonPrimitive("#microsoft.graph.fileAttachment"));
attachments.name = "Another file as attachment";
attachments.contentBytes = "VGhpcyBpcyBhIGZpbGUgdG8gYmUgYXR0YWNoZWQu";
attachmentsList.add(attachments);
post.attachments = attachmentsList;

graphClient.groups("1848753d-185d-4c08-a4e4-6ee40521d115").threads("AAQkADJUdfolA==")
	.reply(post)
	.buildRequest()
	.post();

```