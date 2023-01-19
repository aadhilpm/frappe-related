---
share: true
---

## Port based multitenancy

You can create a new site and make run it on a different port (while the first one runs on port 80).

-   Create a new site
    
    `bench new-site site2name`
    
-   Set port
    
    `bench set-nginx-port site2name 82`
    
-   Re generate nginx config
    
    `bench setup nginx`
    
-   Reload nginx
    
    `sudo service nginx reload`


https://github.com/frappe/bench/wiki/Multitenant-Setup

https://aadhilpm.com/multitenant-setup-for-frappe-sites/
