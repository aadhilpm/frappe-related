---
share: true
---

```Javascript
for invoice in frappe.get_list("Sales Invoice"): 
		invoice = frappe.get_doc("Sales Invoice", invoice.name)
		invoice.cancel() 
		invoice.delete() 
		frappe.db.commit()

```


```mysql

frappe.db.sql(""" update `tabStock Ledger Entry` set stock_value_difference = 0 where item_code = '4031' and warehouse ='Doha Store - PC' """)
   
frappe.db.commit()

```

