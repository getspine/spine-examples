Rocket Chat
===========
<img src="https://rocket.chat/images/logo/logo-dark.svg?v3" />

[Rocket Chat](https://rocket.chat/) is a Slack-like chat service from sandstorm.io, backed by MongoDB.

How to Run
==========

1. Deploy the Backbone file:

```
spine deploy
```

**PLEASE NOTE**: This deployment requests a Let's Encrypt certificate, which will make the initial Balancer deploy take longer than usual.

2. Visit ```https://rocket-<your subdomain>.spi.ne```
