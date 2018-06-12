Switch to the projects directory you created previously:

`cd ~/projects`{{execute}}

Create a folder for your first project stack:

`mkdir first-project`{{execute}}

Switch to that folder:

`cd first-project`{{execute}}

Create a directory called `.docksal`:

`mkdir .docksal`{{execute}}

Docksal bundles a default basic LAMP stack.
Creating the `.docksal` directory is all that is necessary to tell Docksal that you want to use a folder as a project root.

You are now ready to start your first project stack:

`fin project start`{{execute}}

It will take some time for Docker to pull the LAMP stack images (Apache, MySQL and PHP), but this happens only once.

When the process is done, check the "Web server" tab again.
