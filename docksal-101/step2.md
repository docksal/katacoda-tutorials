Create a folder for your first project stack:

```
cd ~/projects
mkdir first-project
cd first-project
```{{execute}}

Create a directory called `.docksal`:

`mkdir .docksal`{{execute}}

Docksal bundles a default basic LAMP stack.
Creating the `.docksal` directory is all that is necessary to tell Docksal that you want to use a folder as a project root.

You are now ready to start your first project stack:

`fin project start`{{execute}}

It will take some time for Docker to pull the LAMP stack images (Apache, MySQL and PHP), but this happens only once.

When the process is done, open the "vhost-proxy" tab again and prepend `first-project.` to the URL, e.g.:

```
http://first-project.2886795277-80-frugo01.environments.katacoda.com
```

Note: please use the HTTP protocol in the URL (`http://`), otherwise you'll get a browser warning about invalid certificate. 

You will see an "Forbidden" error. This is normal.

![forbidden-error](https://i.imgur.com/OO28nr9.png)

There is no document root in the project directory. Let's create one and add a simple `index.php` file:

```
mkdir docroot
echo '<?php phpinfo(); ?>' > docroot/index.php
```{{execute}}

Reload the "vhost-proxy" tab. You should now see a PHP info page.
