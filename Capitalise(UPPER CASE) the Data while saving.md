---
share: true
---

```python

def validate(self):
	zbn = frappe.get_meta(self.doctype)
	fieldnames =[x.fieldname for x in zbn.get("fields") if x.fieldtype in ["Data"]]
	if fieldnames:
		for fields in fieldnames:
			if self.get(fields):
				self.set(fields, str(self.get(fields)).upper())
```


The custom python function for Capitalise/making UPPER CASE while saving a document is adding below :

https://discuss.erpnext.com/t/custom-function-for-capitalise-upper-case-the-data-while-saving/97130
