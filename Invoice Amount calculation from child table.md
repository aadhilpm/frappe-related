---
share: true
---

Doctype: JobCard
Child Doctype field name on parent : invoice_item


```js
frappe.ui.form.on('JobCard', {
    validate: function(frm,cdt,cdn) {
        set_total_invoice(frm);
    }
});

function set_total_invoice(frm) {
    var doc = locals[frm.doc.doctype][frm.doc.name];
    var total_invoice = 0;
    $.each(doc.invoice_item, function(i, d) {
        total_invoice += flt(d.amount);
    });
    frm.set_value("invoice_total",total_invoice);
}

```

