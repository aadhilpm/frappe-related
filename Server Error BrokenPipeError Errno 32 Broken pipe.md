---
share: true
---

This is the cache error while clearing session Job. 

![[Pasted image 20230112083118.png]]

To Manuualy triger:

```
 bench destroy-all-sessions
```

Another best solution is to enable Scheduled jobs  so that clear-expired sessions job will be excuted

```
bench --site [site-name] enable-scheduler

```

