---
share: true
---

This is the cache error while clearing session Job. 

![error](https://user-images.githubusercontent.com/36843795/211985489-4e6f76b1-5ea2-4f28-b97f-198beba71c5a.jpeg)


To Manuualy triger:

```
 bench destroy-all-sessions
```

Another best solution is to enable Scheduled jobs  so that clear-expired sessions job will be excuted

```
bench --site [site-name] enable-scheduler

```

