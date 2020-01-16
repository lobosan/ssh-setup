## Check if we have ssh keys

```shell
ls -al ~/.ssh
```

## Generate SSH keys

```shell
ssh-keygen -t rsa -b 4096 -C "sp.galindoh@gmail.com"
```

Leave default values so no passphrase


## Evaluate if SSH Agent is running

```shell
eval "$(ssh-agent -s)"
```


## Add our new SSH Key to the agent

```shell
ssh-add ~/.ssh/id_rsa
```


## Copy the content of the public key

```shell
less ~/.ssh/id_rsa.pub
```

Press q to quit


## Go to GitHub Settings and add the public key

https://github.com/settings/keys
