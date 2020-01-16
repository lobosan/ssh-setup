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


## Validate connection with github from local machine

```shell
ssh -T git@github.com
```

Type yes to accept the connection


## Setup git username and email

```shell
git config --global user.name "Santiago Galindo"
git config --global user.email "sp.galindoh@gmail.com"
```


## Verify git user name and email

```shell
git config --list
```
