---
share: true
---

On DNS Multitenant Setup

```
bench config dns_multitenant on
bench setup nginx
sudo service nginx reload

```

Connect  Custom Domain with site

```
bench setup add-domain [desired-domain]
Example: bench setup add-domain erp.aadhilpm.com


bench setup nginx
sudo service nginx reload


```


```
bench restart
sudo apt install snapd
sudo snap install core; sudo snap refresh core
sudo apt-get remove certbot
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo certbot --nginx

```

Then based on the option and question shown on the screen mention required details


<button> <a href="https://aadhilpm.com/ssl-on-frappe-site/">Blog Link</a></button>

