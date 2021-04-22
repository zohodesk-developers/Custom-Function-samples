# Send mail with a sample attachment file

## Description
Sample script to demonstrate sending email with an image


## Deluge Script
```javascript
attachmentUrl = "https://picsum.photos/200/300"; // Some random image url
downloadFile = invokeurl
[
	url :attachmentUrl
	type :GET
];
sendmail
[
	from :zoho.adminuserid
	to :"toemail@example.com"
	subject :"Subject of the email"
	message :"Find the attachment"
	Attachments :file:downloadFile
]
```


## Help Urls
[Deluge Script](https://www.zoho.com/deluge/help/)

[DRE Functions](https://dre.zoho.com/help/)

[Desk API Documentation](https://desk.zoho.com/support/APIDocument.do)

[Desk Integration Tasks](https://www.zoho.com/deluge/help/desk-tasks.html)