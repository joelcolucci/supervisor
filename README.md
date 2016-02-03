# Supervisord
This repository contains notes on working with [supervisor](http://supervisord.org/index.html).

## Installation
Ubuntu
```
sudo apt-get install supervisor
```
Mac OS X
```
sudo pip install supervisor
```

## Getting started
### Creating a new configuration file (Ubuntu)
[See official docs](http://supervisord.org/configuration.html)
Create a new file within the `/etc/supervisor/conf.d/` directory named for
your app. Example: myapp.conf.

### Filling out the configuration file
Example:
```
[program:myapp]
command=/home/myusername/code/myproject/venv/bin/gunicorn myapp:app

directory=/home/myusername/code/myapp

user=myusername

autostart=true

autorestart=true

redirect_stderr=True
```

## Learn more
[Running Supervisor on a Mac](https://nicksergeant.com/running-supervisor-on-os-x/)
