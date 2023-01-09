---
share: true
---

```js

frappe.ui.form.on("Sales Invoice", {
    before_save(frm) {
        if(frm.doc.__islocal == 1){
            if(frm.doc.is_return == 1){
                (frm.set_value('naming_series', 'CN-.####'));
            }else{
                (frm.set_value('naming_series', 'SI-.####'));
            }
        }
        
    }
    
});

```