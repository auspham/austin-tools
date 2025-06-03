# fzssh

Quick SSH-Manager using fzf

# Requirement

- Linux OS / WSL
- fzf installed
- Pre-definition jump box in `~/.ssh/config`

# Setup

Create a `$HOME/.serverlist.csv` file using the format


```
# Format: servername      IP
server-name-1                                     1.2.3.4
server-name-2                                     10.20.30.40
server-name-3                                     100.20.30.40
server-name-4                                     10.200.30.40
...
```

# Usage

`fzssh`

- Interactive select the host or name 


`fzssh abitrary_ip`
-  Auto select jump box based on the first prefix of ip. Jumpbox is based on
`~/.ssh/config`

- For example, if your jumpbox has `1.2.3.4` in `~/.ssh/config` and you do `fzssh 1.2.3.5`, it will choose `1.2.3.4` as jumpbox

# Optional parameter

`fzssh ...  -L port:ip:port`
- Port forwarding for selected host


# Bonus

- `update_ssh_hostname`: to autofill `~/.serverlist.csv`, works well for SONIC_MGMT https://github.com/sonic-net/sonic-mgmt/. Note: this will overwrite your `~/.serverlist.csv`