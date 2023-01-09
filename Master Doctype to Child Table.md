---
share: true
---

```Javascript

frappe.ui.form.on('Purchase Order', {
	onload(frm) {
		frm.events.cost_center(frm); 
	},
	cost_center:function(frm){
		var items = frm.doc.items;
		items.forEach(i =>{
			i.cost_center = frm.doc.cost_center;
		});
	}
});

```