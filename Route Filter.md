---
share: true
---

 frappe.listview_settings['Workflow Action'] = {
	onload: function(listview) { 
			frappe.route_options = {
				"status": ["=", "Open"],
				"workflow_state":["not like","Approved"],
				"completed_by":["is","not set"]
			};
	}
};