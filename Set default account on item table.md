---
share: true
---
validate before save

```js

frappe.ui.form.on("Sales Invoice", {
    before_save(frm) {
        update_item(frm);
    }
    
});

function update_item(frm){
        let items = frm.doc.items;
        if(frm.doc.is_return == 1){
                for(let i in items){
                        frappe.model.set_value(items[i].doctype, items[i].name, "income_account", "Sales Return - ZT");
                }
        }
}


```