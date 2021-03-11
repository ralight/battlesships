# Battlesships

https://twitter.com/Andrew_Taylor/status/1369621758383448070

SSH to a Linux machine and kill a pid of your choosing.

To use (but don't unless it is a throwaway computer that you are only going to
keep online for a few hours, just to be sure):

* Create a user "shot" and give it a password.
* Make sure `/home/shot` exists and is owned by `shot`.
* Copy battlesships to e.g. /usr/local/bin/ and make sure it is executable.
* Copy `issue` to `/etc/issue` if you want the colourful banner
* Set the shell for `shot` to be `/usr/local/bin/battlesships`
* Install psutil-python3
* Give `shot` passwordless sudo access to run `/usr/bin/kill` only.

You can't kill certain processes even if you try, notably pid 1 (I don't know
if this is true on non-Linux systems), so this is *fairly* safe, but you are
trusting yourself to some hastily written Python code that can kill any user
process.

Logs IP and shot information to `/home/shot/log`.
