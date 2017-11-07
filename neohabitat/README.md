The Neoclassical Habitat Server
===============================
<img src="https://frandallfarmer.github.io/neohabitat-doc/docs/images/Habitat_cover.jpg" width="291" height="400">

This launches the [Neoclassical Habitat](http://neohabitat.org) server, a recreation of the world's first MMO, Lucasfilm's Habitat.

How to Run
----------

1. Add necessary credentials to the Vault:

```
spine vault add neohabitat_mysql_password $(openssl rand -base64 32)
spine vault add neohabitat_mysql_root_password $(openssl rand -base64 32)
```

2. Deploy the Backbone file:

```
spine deploy
```

3. Follow the client setup instructions in the official Getting Started guide:

https://github.com/frandallfarmer/neohabitat

During **Step 1 - Download and Configure Vice**, replace the IP provided with the IP of your Balancer.
