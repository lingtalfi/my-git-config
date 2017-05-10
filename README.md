My git config
==================
2016-02-04


a copy of my .gitconfig file.




My config files
-------------------

There are two files (in the resources dir):

- [.gitconfig](https://github.com/lingtalfi/my-git-config/blob/master/resources/.gitconfig), which contains all my aliases, and more. This file should be in your user home directory
- [my_git_passwords.txt](https://github.com/lingtalfi/my-git-config/blob/master/resources/my_git_passwords.txt), which is referenced by the .gitconfig, and stores my git passwords (to avoid typing the password everytime I push to the github.com repository). This file should be where you define it in the .gitconfig  (zouzou's home directory in this example).


The my_git_passwords.txt actually stores two imaginary repositories: zouzou and zouzouSister.


My workflow with git
-------------------------

Basically, with this config, I spend most of my time using the following commands:

git snap initial commit (add all files to the commit and commit with the message: initial commit)
git dd (list the commits)
git ddd (list the commits with timestamps)
git ss (see the current status)
git pp      (push to github.com, include pushing tags if any)



Multiple accounts trick
-----------------------------

I have two git accounts, with two separated emails.
Usually I commit with account A, but I have one repository RR which needs to be committed using account B.

I like to just hop into the local project dir and do my commands:

```bash
git snap my update
git pp
```

However, if I do so in the RR repository, I get a permission denied error,
because git uses the wrong account (account A instead of account B).

To fix this, I open the **.git/config** file of the RR projects, and add the following at the end of the file:

```bash
[user]
	name = karayabin
	name = karayabin@gmail.com
[credential]
	username = karayabin		
```

Now, it works: I can hop into RR and push/commit.
Hope this helps.


