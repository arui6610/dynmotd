# dynmotd

### [CHANGELOG](https://github.com/Neutrollized/dynmotd/blob/master/CHANGELOG.md)

Dynamic MOTD for Centos/RHEL (can be adapted for other distros too!)

I got the template for this off someone's repo many years ago, long before I got a GitHub account.  It was initially created for RHEL6, but I've made changes to it for RHEL7 as well as added my own banner on top.  I tried looking for the original so I could do a proper fork and give credit where credit is due, but there are now so many dynmotd repos on GitHub that it's honestly hard to figure out who I got it from.  In any case, you have my thanks and here's a *hat tip* to you, stranger.


## Installation:

```
 1.   vi /etc/ssh/sshd_config  (this is optional; if you have `PrintMotd yes`, then you'll get the static motd as well as the `dynmotd` output)
      PrintMotd no

 2.   vi /etc/pam.d/login  (if applicable)
      # session optional pam_motd.so

 3.   vi /etc/profile.d/dynmotd.sh (mode: 0644)
      /usr/local/bin/dynmotd

 4.   Then of course drop this file in:
      /usr/local/bin/

 5.   Create an optional folder (default: /etc/dynmotd.d) in which you can place custom scripts for checking additional items (file system, services, ports, etc. -- this is optional)
```
