## Enable local git config


By default git uses the config stored in `$HOME/.gitconfig`

If you add any project specific configuration manually by running:

git config user.name "FirstName LastName"
git config user.email "email@provider.com"

These are then added to `.git/config` in your project git repo.

If you want to store some additional configurations in your repo which you want to apply to a particular project, it's good pratice to create a local `.gitconfig` in your project directory and store it there.

Once the repo is cloned, you can apply it by running:

```
git config --local include.path ../.gitconfig

```

This gets added to the .git/config as:

```
...
...
...

[user]
	name = FirstName LastName
	email = email@provider.com
[include]
	path = ../.gitconfig
```


For more see: [stack overflow link](https://stackoverflow.com/questions/18329621/how-to-store-a-git-config-as-part-of-the-repository)