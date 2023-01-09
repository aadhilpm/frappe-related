---
share: true
---
```Javascript

function compose_mail(frm,inv,pdf,email_ids) { 
	var composer = new frappe.views.CommunicationComposer({ doc: inv, frm: frm, recipients: email_ids, subject: "Your Invoice : " + String(inv.name), attach_document_print: true, }); composer.dialog.set_value('infra_pdf_template', pdf); 
	}


```
https://discuss.erpnext.com/t/autopopulate-to-field-in-email-dialog/97216/3