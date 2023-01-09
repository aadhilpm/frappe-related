---
share: true
---

```js
frappe.ui.form.on('Item', { 
	button_field_name: function(frm) { 
		var openlink = window.open(frm.doc.your_data_field);
	} 
});
```

Button: button_field_name  
Data field: your_data_field

When the user pastes the URL in the Data field and then clicks the Button then will open the link according.

https://discuss.erpnext.com/t/add-button-to-form-to-open-hyperlink-for-item/96466