---
share: true
---

error: <class 'PermissionError'>, [Errno 13] Permission denied: file: /usr/lib/python3/dist-packages/supervisor/xmlrpc.py line: 560

In this example we are considering user as frappe. Please change accordingly 

```
chmod -R o+rx /home/frappe

sudo nano /etc/supervisor/supervisord.conf


```

(Add these lines under [unix_http_server])

```
chmod=0760
chown=frappe:frappe

```

Restart the supervisor
```
sudo -A systemctl restart supervisor

```



