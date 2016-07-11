Node-Replicate
===

This repository contains the files for the docker image [hanzel/node-replicate](https://hub.docker.com/r/hanzel/node-replicate/). This calls the [replicator](https://github.com/botleg/replicator) image with the current `container-id` to replicate itself. The application has the following route:

* `/`: Renders the html page with button that call `/run` route.
* `/run`: Calls the [replicator](https://hub.docker.com/r/hanzel/replicator/) image with the current `container-id` to replicate itself.

Usage
---
To provide the authentication for https, the following files are needed in `/ssl` folder:

* `cert.pem`: Client certificate file
* `key.pem`: Certificate key files