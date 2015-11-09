# Setting up a new umbrella for a client

Clients want to develop locally, but we shouldn't ask them to sync the entire largo-umbrella!

Here's how to create a client-specific umbrella to make their lives easier.

There are two moving parts when setting up a new umbrella.

## 1. Create Child Theme in `largo-umbrella`

1. Login to Bitbucket 
2. Confirm you are permissioned to create new repositories in projectlargo (if you don't see an owner dropdown when you Create a repo in the web interface, ping the INN Nerds)
3. Create a new Git repository for the child theme via web or command line. Our theme repository names are prefixed with "theme-" (ex. theme-cornellsun)
4. Create a new folder for the child theme in the `largo-umbrella` such as `/wp-content/themes/cornellsun` (don't prefix folder name)
4. Open the `.gitmodules` file in the `largo-umbrella`
5. Mimic the submodule setup seen for other themes.
```
[submodule "wp-content/themes/cornellsun"]
	path = wp-content/themes/cornellsun
	url = https://bitbucket.org/projectlargo/theme-cornellsun.git
```

6. Commit these changes to largo-umbrella.

## 2. Create a custom umbrella for the client

1. Login to Bitbucket
2. Create a new Git repository for the new umbrella via web or command line.
3. TO-DO: INSTRUCTIONS FOR FABFILE, VAGRANTFILE, ETC
4. TO-DO: Explain submodules and adding tools, largo and the child theme in `.gitmodules`
5. Run `git submodule init && git submodule update`
6.