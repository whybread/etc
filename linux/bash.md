# Bash

## Useful Commands


### Ubuntu general

- GUI/CLI mode
```
$ sudo systemctl isolate graphical.target
$ sudo systemctl isolate multi-user.target
```
or
```
$ sudo init 5
$ sudo init 3
```

- GUI/CLI mode default
```
$ sudo systemctl set-default grapical.target
$ sudo systemctl set-default multi-user.target
```

### Ubuntu services

- List services which start with booting
```
$ sudo systemctl list-unit-files --type=service
```

- Enable/Disable service with booting
```
$ sudo systemctl disable docker.service
$ sudo systemctl enable docker.service
```

- Current service status
```
$ sudo service --status-all
$ sudo systemctl status docker.service
```

- Current service management
```
$ sudo service docker status
$ sudo service docker start
$ sudo service docker stop
```
