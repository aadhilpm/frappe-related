---
share: true
---

```Javascript

frappe.ui.form.on("Payment Entry", "payment_type", function(frm) { if(frm.doc.payment_type == "Receive") { set_field_options("naming_series", ["ACC-REC-"]) cur_frm.set_value("naming_series", "ACC-REC-") }
});

```