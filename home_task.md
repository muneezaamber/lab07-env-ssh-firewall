(a) For a quick test: I would use the `export` command in the terminal. It is temporary and completely disappears as soon as I log out, leaving no mess behind.
(b) For a setting only for me: I would use the `~/.bashrc` file. This is my personal hidden configuration file, and bash reads it every time I log in, so the settings stay permanently but only affect my user account.
(c) For a setting for all users: I would use the `/etc/environment` file. This is the system-wide configuration file, so any variable written here applies permanently to every single user who logs into the server.
