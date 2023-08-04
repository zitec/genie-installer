# Genie

Wizard for helping you setup [Genie](https://gitlab.zitec.com/research/genie) on your system.

## Install

```
bash <(curl -sL https://zit.ec/genie)
```

## Requirements

- Node.js (>= v18)

## FAQ

**Q**: Why don't you use `curl -sL https://zit.ec/genie | bash` instead of `bash <(curl -sL https://zit.ec/genie)`?  
  
**A**: The shell script uses the `read` command for reading user input. By piping the script, we close the stdin and therefore it cannot be reopened. A workaround is to spawn a new process which will substitute the initial one. You can read more about it [here](https://askubuntu.com/questions/1463637/bash-builtin-read-after-a-pipe-doesnt-wait-for-user-input).