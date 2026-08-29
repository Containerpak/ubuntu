# Use Ubuntu as a persistent environment

Install the package once:

```bash
cpak install github.com/containerpak/ubuntu
```

Create an environment and open Bash:

```bash
cpak environment create --name Ubuntu --origin github.com/containerpak/ubuntu
cpak environment shell --environment Ubuntu --command /bin/bash
```

The shell runs as root inside the environment, so Ubuntu packages can be installed normally:

```bash
apt update
apt install git build-essential
```

## Persistent storage

Installed packages, system configuration and the private home directory remain available after the shell closes or the environment stops. Host files, desktop services and devices stay unavailable unless you grant them through the environment settings.

## Manage the environment

```bash
cpak environment list
cpak environment inspect --environment Ubuntu
cpak environment processes --environment Ubuntu
cpak environment stop --environment Ubuntu
```

Deleting the environment also deletes its installed packages, system changes and private home:

```bash
cpak environment delete --environment Ubuntu
```
