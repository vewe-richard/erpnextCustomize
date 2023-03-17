# ErpNext Installation and Customization

## References
https://github.com/frappe/bench

https://letsencrypt.org/docs/challenge-types/

## Steps
### 1. Preparation 
```
$ git clone https://github.com/frappe/frappe_docker.git
$ cd frappe_docker
$ git checkout e2bfa36acd59d73bc78b36db3d44e96db2512e74
$ wget https://raw.githubusercontent.com/frappe/bench/develop/easy-install.py

# Open easy-install.py, and delete line "default=["site1.localhost"],"
Note: If this line is not deleted, letsencrypt will try to get certification   
for this local site [site1.localhost], but obviously will get failed.
```

### 2. Setup Https
As our domain is host in cloudflare, proxied and in full strict mode.  
We must need set http-challenge in cloudflare. Below are the steps.
* Enter cloudflare dashboard, select the domain
* Select SSL/TLS => 'Edge Certificates'
* Disable 'Always Use Https'
* Select Rules => 'Create Page Rule'
* URL is set:  \*$YOURSITE/.well-known/acme-challenge/\*
* 'Pick a Setting (required)' => ssl
* 'Select SSL/TLS encryption mode' => off

### 3. Install
```
$ python3 easy-install.py -p --email your@email -n demo -s your-site
# find password
$ cat $HOME/passwords.txt |grep ADMINISTRATOR_PASSWORDw
```

# Email Setting
https://github.com/vewe-richard/erpnextCustomize/blob/main/doc/email_setting.md


