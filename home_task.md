(a) For a quick test: I would use the `export` command in the terminal. It is temporary and completely disappears as soon as I log out, leaving no mess behind.
(b) For a setting only for me: I would use the `~/.bashrc` file. This is my personal hidden configuration file, and bash reads it every time I log in, so the settings stay permanently but only affect my user account.
(c) For a setting for all users: I would use the `/etc/environment` file. This is the system-wide configuration file, so any variable written here applies permanently to every single user who logs into the server.
Why an SSH key is safer than a password:
An SSH key is much safer because a password can be easily guessed (brute-forced) or stolen via phishing, whereas an SSH key uses complex cryptography that is virtually impossible to guess. 
If someone steals my private key, they can log into any server that has my public key. If this happens, I must immediately log into those servers using another method (like the VM console) and delete my compromised public key from the `~/.ssh/authorized_keys` file, then generate a completely new key pair.
