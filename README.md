# Ubuntu (cpak)

## Installation

```bash
cpak install github.com/containerpak/ubuntu
```

Create a persistent environment and open Bash:

```bash
cpak environment create --name Ubuntu --origin github.com/containerpak/ubuntu
cpak environment shell --environment Ubuntu --command /bin/bash
```

The environment keeps its root filesystem and private home between sessions. It has network access for `apt`; host files, desktop services and devices are not exposed by default.
