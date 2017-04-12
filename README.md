Spine Examples
==============

![teminal animation](tty.gif)

Looking to get started with Spine?

This repo will get you up and running in just a few minutes.

Launching
---------

Each directory contains a **Backbone** file which will spin up a demo application. They can all be launched with a single command:

```bash
cd <service>
spine deploy
```

**PLEASE NOTE**: It can take up to several minutes for DNS to propagate after deploying any new Balancer.

If you don't wish to wait, you can access the **public IP, reported when your Balancer is created**. For example:

```
# cd etherpad
# spine deploy
 - Deploying Cluster: etherpad
 - Deploying Cluster: ep-mariadb
 - Deploying Balancer: etherpad
balancers:
- etherpad:
    datacenter: us-east-1
    name: etherpad
    nerves: 1
    nerve_type: mini
    public_ips:
    - 34.193.135.170
    synapses:
    - port: "80"
      protocol: http
      remote_port: "9001"
      resource: etherpad
      type: cluster
...
```

Digging Deeper
--------------

Once you've launched an application on Spine, you can check the running status of any one of its containers by using the ```spine cluster status``` command:

```
# spine cluster status etherpad
status: RUNNING
nerves:
  0:
    status: RUNNING
    host: drone-f805a661.us-east-1.spine.hosting
    last_event: 1490064265711
    failure_count: 0
```

If you'd like to take a look at the container logs, use the ```spine cluster logs``` command:

```
# spine cluster logs etherpad
0 - 2017-03-21T02:44:27.508Z: Started Etherpad...
0 - 2017-03-21T02:44:27.709Z: [2017-03-21 02:44:27.705] [WARN] console - Declaring the sessionKey in the settings.json is deprecated. This value is auto-generated now. Please remove the setting from the file.
0 - 2017-03-21T02:44:28.945Z: [2017-03-21 02:44:28.937] [INFO] console - Installed plugins:
0 - 2017-03-21T02:44:28.962Z: [2017-03-21 02:44:28.952] [WARN] console - Can't get git version for server header
0 - 2017-03-21T02:44:28.963Z: [2017-03-21 02:44:28.952] [INFO] console - Report bugs at https://github.com/ether/etherpad-lite/issues
```

Finally, if you'd like to hop on a container's root console, use the ```spine cluster ssh``` command:

```
# spine cluster ssh etherpad
             _)
  __|  __ \   |     __ \    _ \
\__ \  |   |  |     |   |   __/
____/  .__/  _| _) _|  _| \___|
      _|
-------------------------------
Cluster: etherpad
Nerve: 0
Owner: philcollins
-------------------------------
root@drone-f805a661:/opt/etherpad-lite#
```

Need help?
----------

If you run into any issues, we're here to ensure that you have a great experience with Spine.

Come join our support Slack and we'd be glad to help you out:

https://support.spi.ne

<p align="center">
  <img src="https://spi.ne/static/logo_small.png" alt="Spine Logo" width="100" height="98">
</p>
