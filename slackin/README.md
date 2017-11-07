Slackin
=======

You've got a Slack all set up but you'd like to automate the sending of invitations. Slackin makes this easy and Spine can bring it up in under a minute.

How to Run
==========

1. Follow the guide here to create a Slack OAuth token:

https://github.com/rauchg/slackin

2. Add the new Slack token to the Vault:

```
spine vault add slackin_token your-slack-token
```

3. Change the **SLACK_ORG** environment variable within the **slackin** Cluster to the name of your Slack team (e.g. <name>.slack.com).

4. Deploy the Backbone file:

```
spine deploy
```

5. Visit ```http://slackin-<your subdomain>.spi.ne```
