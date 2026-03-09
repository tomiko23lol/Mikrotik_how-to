# Scripts: 

## Backup and Export scripts
- change variables for FTP 
- run script with scheduler
- tested on OS version 7.21.x


## ipsec test and reset script
- provides check of connection of IPsec tunel.
- in case of tunel down, it restart
- in case no restart is needed, logs message that all is OK.
- script needs to be run with scheduler ( as frequent as needed)

## Spamhouse
- downloads list of known spam and malicious IPs.
- replaces / installs new list
- this list is than used in FW rule where new connections from "blacklist" are immediatelly dropped.
- schedule run of scripts as needed.

## Cloudflare_IPV4
- downloads list of known Cloudflare IPV4 IPs
- replaces those IPs in List
- after that it is used in FW rule as source allow list. For example connection to public IP and forwarding/NAT on port 443 is allowed only from Cloudflare addresses. This way 443 is available only if it originates from Cloudflare Public IPs.
- schedule run of scripts as needed.

