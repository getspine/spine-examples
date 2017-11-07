Etherpad
========
![Etherpad Logo](http://etherpad.org/img/logo.svg)

This is the popular [Etherpad](http://etherpad.org/) collaborative editing service.

How to Run
----------

1. Add necessary credentials to the Vault:

```
spine vault add etherpad_mysql_password $(openssl rand -base64 32)
spine vault add etherpad_mysql_root_password $(openssl rand -base64 32)
```

2. Deploy the Backbone file:

```
spine deploy
```

3. Visit ```http://etherpad-<your subdomain>.spi.ne```
