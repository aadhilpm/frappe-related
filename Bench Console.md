---
share: true
---

Bench console command for deleting stock and gl entry and marking the Sales Invoice into draft


 ```python

frappe.db.sql(""" delete from `tabStock Ledger Entry` where voucher_no = "AO21/0331" """)

frappe.db.sql(""" delete from`tabGL Entry` where voucher_no = "AO21/0331" """)

frappe.db.commit()

frappe.db.set_value("Sales Invoice Item", {"parent":"AO21/0331"}, "docstatus", 0)

frappe.db.set_value("Sales Invoice", "AO21/0331", "docstatus", 0)

frappe.db.commit()

```

```python

frappe.db.sql(""" update `tabStock Ledger Entry` set stock_value_difference = 0 where item_code = '4031' and warehouse ='Store - PC' """)
   
frappe.db.commit()

```
