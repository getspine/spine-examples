Wordpress
=========
<img src="https://upload.wikimedia.org/wikipedia/commons/2/20/WordPress_logo.svg" />

This is the popular [Wordpress](https://wordpress.com/) blogging application, backed by MySQL.

How to Run
==========

1. Add necessary credentials to the Vault:

```
spine vault add wordpress_mysql_password $(openssl rand -base64 32)
spine vault add wordpress_mysql_root_password $(openssl rand -base64 32)
```

2. Deploy the Backbone file:

```
spine deploy
```

3. Visit ```http://wordpress.<your subdomain>.spi.ne```
