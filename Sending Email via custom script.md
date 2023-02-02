---
share: true
---

Below custom script allows to send cc and bcc also

```

frappe.call({
	method: "frappe.core.doctype.communication.email.make",
	args: {
		recipients: "my_email@mail.com",
		cc: "cc@mail.com",
		bcc: "bcc@mail.com",
		content: d,
		subject: "Test",
		doctype: "Panel",
		name: cur_frm.doc.name,
		send_email: 1,
		communication_medium: "Email",
	}, 
	async: false,
	callback: function(rh){
		console.log("mail sent")
	}
});

```