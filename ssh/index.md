# Tips and Tricks about SSH client

## How to keep SSH connection alive

Example:

```bash
ssh -o ServerAliveInterval=60 username@hostname
```

We also could update the SSH config file to keep alive for all connections.

```ini
# in file:
# - ~/.ssh/config
Host *
    ServerAliveInterval 60
```

We could also configure **~/.bash_profile** for this:

```bash
alias ssh-qa-east="ssh -o ServerAliveInterval=60 <user>@<ip>"
```

References:

* [How to keep ssh session alive](https://stackoverflow.com/questions/25084288/keep-ssh-session-alive)
