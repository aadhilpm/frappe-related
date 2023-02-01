---
share: true
---

```
frappe.ui.form.on('Sales Order', {
	refresh(frm) { 
	setTimeout(() => {
		frm.remove_custom_button('Update Items'); 
		frm.remove_custom_button('Close', 'Status');
		}, 10);
	}
})

```