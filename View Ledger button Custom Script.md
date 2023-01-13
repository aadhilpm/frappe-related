---
share: true
---

```Javascript

frappe.ui.form.on('Expense Entry', {
	refresh(frm) {
	if(frm.doc.docstatus > 0) {
			frm.add_custom_button(__('Ledger'), function() {
				frappe.route_options = {
					"voucher_no": frm.doc.name,
					"from_date": frm.doc.posting_date,
					"to_date": moment(frm.doc.modified).format('YYYY-MM-DD'),
					"company": frm.doc.company,
					"finance_book": frm.doc.finance_book,
					"group_by": 'Group by Voucher (Consolidated)',
					"show_cancelled_entries": frm.doc.docstatus === 2
				};
				frappe.set_route("query-report", "General Ledger");
			});
		}

	
	}
})

```
