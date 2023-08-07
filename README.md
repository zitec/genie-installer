# Genie

Wizard for helping you setup [Genie](https://gitlab.zitec.com/research/genie) on your system.

## Install

```
bash <(curl -fsSL https://zit.ec/genie)
```

## Requirements

- Node.js (>= v18)

## FAQ

**Q**: Why don't you use `curl -fsSL https://zit.ec/genie | bash` instead of `bash <(curl -fsSL https://zit.ec/genie)`?  
  
**A**: The shell script uses the `read` command for reading user input. By piping the script, we will close the stdin and therefore we cannot read user input anymore. A workaround is to spawn a new bash process which will substitute the initial one. You can read more about it [here](https://askubuntu.com/questions/1463637/bash-builtin-read-after-a-pipe-doesnt-wait-for-user-input).