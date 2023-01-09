---
share: true
---

```javascript

frappe.ui.form.on("Purchase Order", {
        "supplier": function(frm){
                if(frm.doc.__islocal == 1){
                        if(frm.doc.supplier == "Cash Supplier"){
                                frm.set_value("naming_series", "CP-CPO-.YY.-.MM.-");
                                
                        }else {
                                frm.set_value("naming_series", "CP-PO-.YY.-.MM.-");
                               
                        }
                }
        }
})
```

Before Save Validation

```javascript

frappe.ui.form.on("Purchase Order", {
        "before_save": function(frm){
                if(frm.doc.__islocal == 1){
                        if(frm.doc.supplier == "Cash Supplier"){
                                frm.set_value("naming_series", "CP-CPO-.YY.-.MM.-");
                                
                        }else {
                                frm.set_value("naming_series", "CP-PO-.YY.-.MM.-");
                               
                        }
                }
        }
})

```