# supervisord

[![Docker Automated build](https://img.shields.io/docker/cloud/automated/tinslice/supervisord.svg?style=flat)](https://hub.docker.com/r/tinslice/supervisord/builds)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/tinslice/supervisord.svg?style=flat)](https://hub.docker.com/r/tinslice/supervisord/builds)
[![license](https://img.shields.io/github/license/tinslice/docker-supervisord.svg)](https://github.com/tinslice/docker-supervisord)

Docker image which allows for easy configuration of multiple services using [supervisord](http://supervisord.org/configuration.html).

## Adding services

1. add service configuration to /etc/supervisord.d
2. service configuration file name should have the extension 'conf'

## Configuration example

```conf
[program:my-app]
user=root
command=command-to-run.sh
redirect_stderr=true
stdout_logfile=/var/log/my-app.log
autorestart=true
startretries=3
```
