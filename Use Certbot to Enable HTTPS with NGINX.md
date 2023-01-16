---
share: true
---

When Certbot runs, it requests and installs certificate file along with a private key file. When used with the [NGINX plugin](https://certbot.eff.org/docs/using.html#nginx) (`--nginx`), Certbot also automatically edits the configuration files for NGINX, which dramatically simplifies configuring HTTPS for your web server. If you prefer to manually adjust the configuration files, you can run Certbot using the `certonly` command.

```
sudo certbot --nginx
```