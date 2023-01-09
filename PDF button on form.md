---
share: true
---

```js

frappe.ui.form.on("Sales Invoice", "refresh", function(frm){
	frm.add_custom_button("PDF", function(){
			var myWin = window.open('http://domain.com/api/method/frappe.utils.print_format.download_pdf?doctype=Sales%20Invoice&name='+cur_frm.doc.name+'&format=PDF%20Sales%20Invoice&no_letterhead=0&letterhead=main&settings=%7B%7D&_lang=en-US');
	});
});

```
