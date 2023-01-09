---
share: true
---

```Javascript

frappe.listview_settings['Lead'] = { 
	refresh: function(listview) { 
		$(".comment-count").hide(); 
		$(".frappe-timestamp").hide(); 
		$(".avatar-small").hide(); 
	} 
};

```
Please try to remove these fields through below code. Use status field class name in below code and then try to refresh the page.

https://discuss.erpnext.com/t/hide-docstatus-in-listview/10274/6