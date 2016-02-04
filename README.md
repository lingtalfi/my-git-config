My git config
==================
2016-02-04


a copy of my .gitconfig file.



There are two files (in the resources dir):

- .gitconfig, which contains all my aliases, and more. This file should be in your user home directory
- my_git_passwords.txt, which is referenced by the .gitconfig, and stores my git passwords (to avoid typing the password everytime I push to the github.com repository). This file should be where you define it in the .gitconfig  (zouzou's home directory in this example).


The my_git_passwords.txt actually stores two imaginary repositories: zouzou and zouzouSister.



Basically, with this config, I spend most of my time using the following commands:

git snap initial commit (add all files to the commit and commit with the message: initial commit)
git dd (list the commits)
git ddd (list the commits with timestamps)
git ss (see the current status)
git pp      (push to github.com, include pushing tags if any)