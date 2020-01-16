# Copy Account custom field value to ticket's custom field

## Description
On ticket creation, the custom field value of an account is copied to the ticket's custom field.


### Module : Tickets
### Workflow Trigger : On Create
Create workflow in Tickets module. 

<img src="images/createWf.png" alt="createWf" width="400"/>

### Workflow Action
<img src="images/wfAction.png" alt="wfAction" width="400"/>

### Arguments : 
* ticketId - Choose Ticket Id
* accountCustomField - Choose Account Custom Field

<img src="images/arg_ticketId.png" alt="argTicketId" width="400"/>
<img src="images/arg_cf.png" alt="argCf" width="400"/>

## Deluge Script
```javascript
ORGID = 123456; // Replace OrgId
ticketCustomFieldApiName = "cf_my_ticket_custom_field";
mapData = {"cf":{ticketCustomFieldApiName : accountCustomField}};
response = zoho.desk.update(ORGID,"tickets",ticketId,mapData);
```

## Notes
This function uses Desk Integration Task for updating the ticket.

## FAQ
### How to get OrgId?
see [Organizations API](https://desk.zoho.com/support/APIDocument.do#Organizations)

### How to get custom field API name?
Goto Setup > Layouts and Fields > Fields List
Choose the module

<img src="images/fieldsList.png" alt="FieldsListSetup" width="4600"/>



## Help Urls
[Deluge Script](https://www.zoho.com/deluge/help/)

[DRE Functions](https://dre.zoho.com/help/)

[Desk API Documentation](https://desk.zoho.com/support/APIDocument.do)

[Desk Integration Tasks](https://www.zoho.com/deluge/help/desk-tasks.html)
