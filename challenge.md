Job 1:
Command: printenv | grep PATH
Answer: /usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin:/home/muneezaamber
Command: printenv | grep LANG
Answer: en_US.UTF-8
Command: printenv | grep PWD
Answer: /home/muneezaamber/lab07-env-ssh-firewall

Job 2:
Commands:
export STUDENT_NAME="Muneeza"
export STUDENT_ROLL_NUMBER="FA24B1-SE-010"
export STUDENT_SEMESTER="5"
printenv | grep '^STUDENT_'
Explanation: These variables disappeared after logging out because `export` is only temporary.

Job 3:
Explanation: To make them permanent, we edited `~/.bashrc` using vim, added the export lines at the very end, and ran `source ~/.bashrc` to reload them.

Job 4:
Explanation: To block ping, we backed up `/etc/ufw/before.rules`, replaced ACCEPT with DROP on the echo-request line, and reloaded the firewall using `sudo ufw reload`.
