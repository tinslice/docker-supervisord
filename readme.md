# supervisord

Docker image (<https://cloud.docker.com/u/tinslice/repository/docker/tinslice/supervisord>) based on `alpine` which allows for easy configuration of multiple services using [supervisord](http://supervisord.org/configuration.html).

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
