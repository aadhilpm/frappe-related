---
share: true
---

```javascript

frappe.ui.form.on('Doctype', { parent_field: function(frm) { if (!frm.doc.parent_field) { frm.set_value('child_table_fieldname', []); frm.refresh_field('child_table_fieldname'); } } });

```
https://discuss.erpnext.com/t/how-to-delete-refresh-clear-child-table-entries-data-from-parent-doctype-while-updating/97063