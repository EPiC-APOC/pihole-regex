## Regex Filters for Pi-hole
This is a custom `regex.list` file for use with Pi-hole v4+ (FTLDNS).

All commands will need to be entered via Terminal (PuTTY or your SSH client of choice) after logging in.

### Why use the installer?
The installer will determine whether you are using the Pi-hole database or the older style regex.list, then evaluate your current regular expressions and act accordingly. It has been created to make life easier.

### Can I use these regexps without using the installer?
Yes, you can. You can enter them one by one in the Pi-hole web interface.

### [OPTIONAL] Back up your existing regex list

If you are using the new **Pi-hole DB**
```
sudo cp /etc/pihole/gravity.db /etc/pihole/gravity.db.bak
```

If you are using the older style **regex.list**:
```
sudo cp /etc/pihole/regex.list /etc/pihole/regex.list.bak
```

### Installation Instructions
```
MMOTTI:
curl -sSl https://raw.githubusercontent.com/mmotti/pihole-regex/master/install.sh | bash 

EPiC (fork):
curl -sSl https://raw.githubusercontent.com/EPiC-APOC/pihole-regex/master/install.sh | bash 
```

### Removal Instructions
```
MMOTTI:
curl -sSl https://raw.githubusercontent.com/mmotti/pihole-regex/master/uninstall.sh | bash

EPiC (fork):
curl -sSl https://raw.githubusercontent.com/EPiC-APOC/pihole-regex/master/uninstall.sh | bash
```

### Testing the regex filter
See if you can access https://ad.pi-hole.net/

Then check the query log in the Pi-hole admin console for your blocked domain. It should show as **Pi-holed (wildcard)**.

![alt test](https://image.ibb.co/j5kWTz/Blocked.png)
