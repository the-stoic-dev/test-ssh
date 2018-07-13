I am attempting to use various ssh keys, following guidance on
https://nerderati.com/2011/03/17/simplify-your-life-with-an-ssh-config-file/.

This works just the way I want.  The only catch is you have to change the Git
remote.


**git remote -v**

```
origin	git@github-stoic:the-stoic-dev/test-ssh.git (fetch)
origin	git@github-stoic:the-stoic-dev/test-ssh.git (push)
```


**~/.ssh/config**

```
Host github-stoic
  User git
  HostName github.com
  IdentityFile ~/.ssh/id_rsa_the_stoic_dev

Host github.com
  User git
  HostName github.com
  IdentityFile ~/.ssh/id_rsa
```
