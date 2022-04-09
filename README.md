# pi-hole-error
pi hole error

This process collects information from your Pi-hole, and optionally uploads it to a unique and random directory on tricorder.pi-hole.net.

The intent of this script is to allow users to self-diagnose their installations.  This is accomplished by running tests against our software and providing the user with links to FAQ articles when a problem is detected.  Since we are a small team and Pi-hole has been growing steadily, it is our hope that this will help us spend more time on development.

NOTE: All log files auto-delete after 48 hours and ONLY the Pi-hole developers can access your data via the given token. We have taken these extra steps to secure your data and will work to further reduce any personal information gathered.

*** [ INITIALIZING ]
[i] 2022-04-09:07:57:49 debug log has been initialized.
[i] System has been running for 5 days, 18 hours, 56 minutes

*** [ INITIALIZING ] Sourcing setup variables
[i] Sourcing /etc/pihole/setupVars.conf...

*** [ DIAGNOSING ]: Core version
[i] Core: v5.9 (https://discourse.pi-hole.net/t/how-do-i-update-pi-hole/249)
[i] Remotes: origin	https://github.com/pi-hole/pi-hole.git (fetch)
             origin	https://github.com/pi-hole/pi-hole.git (push)
[i] Branch: master
[i] Commit: v5.9-0-g6ffa2ba

*** [ DIAGNOSING ]: Web version
[i] Web: v5.11 (https://discourse.pi-hole.net/t/how-do-i-update-pi-hole/249)
[i] Remotes: origin	https://github.com/pi-hole/AdminLTE.git (fetch)
             origin	https://github.com/pi-hole/AdminLTE.git (push)
[i] Branch: master
[i] Commit: v5.11-0-g64bbce9

*** [ DIAGNOSING ]: FTL version
[✓] FTL: v5.14

*** [ DIAGNOSING ]: lighttpd version
[i] 1.4.53

*** [ DIAGNOSING ]: php version
[i] 7.3.29

*** [ DIAGNOSING ]: Operating system
[i] dig return code:  0
[i] dig response:  "Raspbian=9,10,11 Ubuntu=16,18,20,21 Debian=9,10,11 Fedora=33,34 CentOS=7,8"
[✓] Distro:  Raspbian
[✓] Version: 10

*** [ DIAGNOSING ]: SELinux
[i] SELinux not detected

*** [ DIAGNOSING ]: FirewallD
[i] Firewalld service inactive

*** [ DIAGNOSING ]: Processor
[✓] armv7l

*** [ DIAGNOSING ]: Disk usage
   Filesystem      Size  Used Avail Use% Mounted on
   /dev/root        59G  7.1G   49G  13% /
   devtmpfs        430M     0  430M   0% /dev
   tmpfs           463M   18M  446M   4% /dev/shm
   tmpfs           463M   36M  427M   8% /run
   tmpfs           5.0M  4.0K  5.0M   1% /run/lock
   tmpfs           463M     0  463M   0% /sys/fs/cgroup
   /dev/mmcblk0p1  253M   49M  204M  20% /boot
   tmpfs            93M     0   93M   0% /run/user/999
   tmpfs            93M  4.0K   93M   1% /run/user/1000

*** [ DIAGNOSING ]: Network interfaces and addresses
   1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
       link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
       inet 127.0.0.1/8 scope host lo
          valid_lft forever preferred_lft forever
       inet6 ::1/128 scope host 
          valid_lft forever preferred_lft forever
   2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
       link/ether b8:27:eb:6b:da:6e brd ff:ff:ff:ff:ff:ff
       inet 192.168.5.77/22 brd 192.168.7.255 scope global noprefixroute eth0
          valid_lft forever preferred_lft forever
       inet6 fdae:fb05:73a5:1:d4f6:cc79:f2fc:c8cc/64 scope global dynamic mngtmpaddr noprefixroute 
          valid_lft 2591989sec preferred_lft 604789sec
       inet6 fe80::7459:2947:e84f:cfab/64 scope link 
          valid_lft forever preferred_lft forever
   3: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
       link/ether b8:27:eb:3e:8f:3b brd ff:ff:ff:ff:ff:ff
       inet 192.168.5.75/22 brd 192.168.7.255 scope global dynamic noprefixroute wlan0
          valid_lft 11057sec preferred_lft 9257sec
       inet6 fdae:fb05:73a5:1:e48f:7fd9:6042:6350/64 scope global dynamic mngtmpaddr noprefixroute 
          valid_lft 2591990sec preferred_lft 604790sec
       inet6 fe80::185c:4f3a:eb26:f035/64 scope link 
          valid_lft forever preferred_lft forever

*** [ DIAGNOSING ]: Network routing table
   default via 192.168.4.1 dev eth0 src 192.168.5.77 metric 202 
   default via 192.168.4.1 dev wlan0 proto dhcp src 192.168.5.75 metric 303 
   192.168.4.0/22 dev eth0 proto dhcp scope link src 192.168.5.77 metric 202 
   192.168.4.0/22 dev wlan0 proto dhcp scope link src 192.168.5.75 metric 303 

*** [ DIAGNOSING ]: Networking
[✓] IPv4 address(es) bound to the eth0 interface:
    192.168.5.77/22

[✓] IPv6 address(es) bound to the eth0 interface:
    fdae:fb05:73a5:1:d4f6:cc79:f2fc:c8cc/64
    fe80::7459:2947:e84f:cfab/64

[i] Default IPv4 gateway: 192.168.4.1
   * Pinging 192.168.4.1...
[✓] Gateway responded.
[i] Default IPv6 gateway: fe80::e4e6:4ce:a119:2111
   * Pinging fe80::e4e6:4ce:a119:2111...
[✓] Gateway responded.

*** [ DIAGNOSING ]: Ports in use
[✓] udp:0.0.0.0:53 is in use by pihole-FTL
    udp:0.0.0.0:68 is in use by dhcpcd
    udp:0.0.0.0:631 is in use by cups-browsed
    udp:0.0.0.0:45286 is in use by avahi-daemon
    udp:0.0.0.0:5353 is in use by avahi-daemon
[✓] udp:*:53 is in use by pihole-FTL
    udp:*:41045 is in use by avahi-daemon
    udp:*:5353 is in use by avahi-daemon
[✓] tcp:127.0.0.1:4711 is in use by pihole-FTL
    tcp:0.0.0.0:5900 is in use by vncserver-x11-c
[✓] tcp:0.0.0.0:80 is in use by lighttpd
[✓] tcp:0.0.0.0:53 is in use by pihole-FTL
    tcp:0.0.0.0:22 is in use by sshd
    tcp:127.0.0.1:631 is in use by cupsd
[✓] tcp:[::1]:4711 is in use by pihole-FTL
    tcp:[::]:5900 is in use by vncserver-x11-c
[✓] tcp:[::]:80 is in use by lighttpd
[✓] tcp:[::]:53 is in use by pihole-FTL
    tcp:[::]:22 is in use by sshd
    tcp:[::1]:631 is in use by cupsd

*** [ DIAGNOSING ]: Name resolution (IPv4) using a random blocked domain and a known ad-serving domain
[✓] 3piles.com is 0.0.0.0 on lo (127.0.0.1)
[✓] 3piles.com is 0.0.0.0 on eth0 (192.168.5.77)
[✓] 3piles.com is 0.0.0.0 on wlan0 (192.168.5.75)
[✓] doubleclick.com is 172.217.169.46 via a remote, public DNS server (8.8.8.8)

*** [ DIAGNOSING ]: Name resolution (IPv6) using a random blocked domain and a known ad-serving domain
[✓] net.69679.9578.302br.net is :: on lo (::1)
[✓] net.69679.9578.302br.net is :: on eth0 (fdae:fb05:73a5:1:d4f6:cc79:f2fc:c8cc)
[✓] net.69679.9578.302br.net is :: on eth0 (fe80::7459:2947:e84f:cfab)
[✓] net.69679.9578.302br.net is :: on wlan0 (fdae:fb05:73a5:1:e48f:7fd9:6042:6350)
[✓] net.69679.9578.302br.net is :: on wlan0 (fe80::185c:4f3a:eb26:f035)
[✗] Failed to resolve doubleclick.com via a remote, public DNS server (2001:4860:4860::8888)

*** [ DIAGNOSING ]: Discovering active DHCP servers (takes 10 seconds)
   Scanning all your interfaces for DHCP servers
   Timeout: 10 seconds
   
   * Received 300 bytes from eth0:192.168.4.1
     Offered IP address: 192.168.5.77
     Server IP address: N/A
     Relay-agent IP address: N/A
     BOOTP server: (empty)
     BOOTP file: (empty)
     DHCP options:
      Message type: DHCPOFFER (2)
      server-identifier: 192.168.4.1
      lease-time: 14400 ( 4h )
      netmask: 255.255.252.0
      router: 192.168.4.1
      dns-server: 192.168.4.1
      broadcast: 192.168.7.255
      ntp-server: 192.168.4.1
         --- end of options ---
    
   * Received 300 bytes from eth0:192.168.4.1
     DHCPOFFER hardware address did not match our own - ignoring packet (not for us)
     DHCPREQUEST chaddr: b8:27:eb:6b:da:6e (our MAC address)
     DHCPOFFER   chaddr: b8:27:eb:3e:8f:3b (response MAC address)
   * Received 300 bytes from wlan0:192.168.4.1
     DHCPOFFER hardware address did not match our own - ignoring packet (not for us)
     DHCPREQUEST chaddr: b8:27:eb:3e:8f:3b (our MAC address)
     DHCPOFFER   chaddr: b8:27:eb:6b:da:6e (response MAC address)
   * Received 300 bytes from wlan0:192.168.4.1
     Offered IP address: 192.168.5.75
     Server IP address: N/A
     Relay-agent IP address: N/A
     BOOTP server: (empty)
     BOOTP file: (empty)
     DHCP options:
      Message type: DHCPOFFER (2)
      server-identifier: 192.168.4.1
      lease-time: 14400 ( 4h )
      netmask: 255.255.252.0
      router: 192.168.4.1
      dns-server: 192.168.4.1
      broadcast: 192.168.7.255
      ntp-server: 192.168.4.1
         --- end of options ---
    
   DHCP packets received on interface wlan0: 1
   DHCP packets received on interface lo: 0
   DHCP packets received on interface eth0: 1

*** [ DIAGNOSING ]: Pi-hole processes
[✓] lighttpd daemon is active
[✓] pihole-FTL daemon is active

*** [ DIAGNOSING ]: Pi-hole-FTL full status
   ● pihole-FTL.service - LSB: pihole-FTL daemon
   Loaded: loaded (/etc/init.d/pihole-FTL; generated)
   Active: active (exited) since Thu 2022-04-07 10:07:44 BST; 1 day 21h ago
     Docs: man:systemd-sysv-generator(8)
  Process: 28752 ExecStart=/etc/init.d/pihole-FTL start (code=exited, status=0/SUCCESS)

Apr 07 10:07:32 raspberrypi systemd[1]: Starting LSB: pihole-FTL daemon...
Apr 07 10:07:32 raspberrypi pihole-FTL[28752]: Not running
Apr 07 10:07:32 raspberrypi su[28764]: (to pihole) root on none
Apr 07 10:07:32 raspberrypi su[28764]: pam_unix(su:session): session opened for user pihole by (uid=0)
Apr 07 10:07:44 raspberrypi pihole-FTL[28752]: FTL started!
Apr 07 10:07:44 raspberrypi systemd[1]: Started LSB: pihole-FTL daemon.

*** [ DIAGNOSING ]: Setup variables
    BLOCKING_ENABLED=true
    PIHOLE_INTERFACE=eth0
    IPV4_ADDRESS=192.168.5.77/22
    IPV6_ADDRESS=fdae:fb05:73a5:1:e48f:7fd9:6042:6350
    QUERY_LOGGING=true
    INSTALL_WEB_SERVER=true
    INSTALL_WEB_INTERFACE=true
    LIGHTTPD_ENABLED=true
    CACHE_SIZE=10000
    DNSMASQ_LISTENING=local
    PIHOLE_DNS_1=208.67.222.222
    PIHOLE_DNS_2=208.67.220.220
    PIHOLE_DNS_3=2620:119:35::35
    PIHOLE_DNS_4=2620:119:53::53
    PIHOLE_DNS_5=4.2.2.1
    PIHOLE_DNS_6=4.2.2.2
    PIHOLE_DNS_7=8.26.56.26
    PIHOLE_DNS_8=8.20.247.20
    PIHOLE_DNS_9=84.200.69.80
    PIHOLE_DNS_10=84.200.70.40
    PIHOLE_DNS_11=2001:1608:10:25:0:0:1c04:b12f
    PIHOLE_DNS_12=2001:1608:10:25:0:0:9249:d69b
    PIHOLE_DNS_13=9.9.9.9
    PIHOLE_DNS_14=149.112.112.112
    PIHOLE_DNS_15=2620:fe::fe
    PIHOLE_DNS_16=2620:fe::9
    PIHOLE_DNS_17=9.9.9.10
    PIHOLE_DNS_18=149.112.112.10
    PIHOLE_DNS_19=2620:fe::10
    PIHOLE_DNS_20=2620:fe::fe:10
    PIHOLE_DNS_21=9.9.9.11
    PIHOLE_DNS_22=149.112.112.11
    PIHOLE_DNS_23=2620:fe::11
    PIHOLE_DNS_24=2620:fe::fe:11
    PIHOLE_DNS_25=1.1.1.1
    PIHOLE_DNS_26=1.0.0.1
    PIHOLE_DNS_27=2606:4700:4700::1111
    PIHOLE_DNS_28=2606:4700:4700::1001
    DNS_FQDN_REQUIRED=true
    DNS_BOGUS_PRIV=true
    DNSSEC=false
    REV_SERVER=false

*** [ DIAGNOSING ]: Dashboard and block page
[✗] Block page X-Header: X-Header does not match or could not be retrieved.
HTTP/1.1 200 OK
Content-type: text/html; charset=UTF-8
Expires: Sat, 09 Apr 2022 06:58:16 GMT
Cache-Control: max-age=0
Date: Sat, 09 Apr 2022 06:58:16 GMT
Server: lighttpd/1.4.53

[✓] Web interface X-Header: X-Pi-hole: The Pi-hole Web interface is working!

*** [ DIAGNOSING ]: Gravity Database
-rw-rw-r-- 1 pihole pihole 100M Apr  3 03:02 /etc/pihole/gravity.db

*** [ DIAGNOSING ]: Info table
   property              value                                   
   --------------------  ----------------------------------------
   version               15                                      
   updated               1648951330                              
   gravity_count         1345044                                 
   Last gravity run finished at: Sun Apr  3 03:02:10 BST 2022

   ----- First 10 Gravity Domains -----
   localhost.localdomain
   wizhumpgyros.com
   coccyxwickimp.com
   webmail-who-int.000webhostapp.com
   010sec.com
   01mspmd5yalky8.com
   0byv9mgbn0.com
   ns6.0pendns.org
   dns.0pengl.com
   12724.xyz


*** [ DIAGNOSING ]: Groups
   id    enabled  name                                                date_added           date_modified        description                                       
   ----  -------  --------------------------------------------------  -------------------  -------------------  --------------------------------------------------
   0           1  Default                                             2021-09-18 18:01:30  2021-09-18 18:01:30  The default group                                 

*** [ DIAGNOSING ]: Domainlist (0/1 = exact white-/blacklist, 2/3 = regex white-/blacklist)
   id     type  enabled  group_ids     domain                                                                                                date_added           date_modified        comment                                           
   -----  ----  -------  ------------  ----------------------------------------------------------------------------------------------------  -------------------  -------------------  --------------------------------------------------
   1      0           1  0             (\.|^)secure\.pes\.itv\.com$                                                                          2021-09-19 09:04:07  2021-09-19 09:04:14  ITV                                               
   2      0           1  0             tom.itv.com                                                                                           2021-09-19 09:04:34  2021-09-19 09:04:34  ITV                                               
   3      0           1  0             arc.msn.com                                                                                           2021-09-22 15:59:42  2021-11-23 13:37:46  Xbox store                                        
   4      0           1  0             activity.windows.com                                                                                  2021-09-22 15:59:55  2021-09-22 15:59:55  EA Play on Xbox                                   
   7      0           1  0             xbox.ipv6.microsoft.com                                                                               2021-09-22 18:03:10  2022-02-03 22:16:52                                                    
   8      0           1  0             device.auth.xboxlive.com                                                                              2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   9      0           1  0             www.msftncsi.com                                                                                      2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   10     0           1  0             title.mgt.xboxlive.com                                                                                2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   11     0           1  0             xsts.auth.xboxlive.com                                                                                2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   12     0           1  0             title.auth.xboxlive.com                                                                               2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   13     0           1  0             ctldl.windowsupdate.com                                                                               2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   14     0           1  0             attestation.xboxlive.com                                                                              2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   15     0           1  0             xboxexperiencesprod.experimentation.xboxlive.com                                                      2021-09-22 18:03:11  2022-02-03 22:16:52                                                    
   16     0           1  0             xflight.xboxlive.com                                                                                  2021-09-22 18:03:12  2022-02-03 22:16:52                                                    
   17     0           1  0             cert.mgt.xboxlive.com                                                                                 2021-09-22 18:03:12  2022-02-03 22:16:52                                                    
   18     0           1  0             xkms.xboxlive.com                                                                                     2021-09-22 18:03:12  2021-11-23 13:36:57  Xbox things                                       
   19     0           1  0             def-vef.xboxlive.com                                                                                  2021-09-22 18:03:12  2022-02-03 22:16:52                                                    
   20     0           1  0             notify.xboxlive.com                                                                                   2021-09-22 18:03:13  2022-02-03 22:16:52                                                    
   21     0           1  0             help.ui.xboxlive.com                                                                                  2021-09-22 18:03:13  2022-02-03 22:16:52                                                    
   22     0           1  0             licensing.xboxlive.com                                                                                2021-09-22 18:03:13  2022-02-03 22:16:52                                                    
   23     0           1  0             eds.xboxlive.com                                                                                      2021-09-22 18:03:13  2022-02-03 22:16:52                                                    
   24     0           1  0             www.xboxlive.com                                                                                      2021-09-22 18:03:13  2022-02-03 22:16:52                                                    
   25     0           1  0             v10.vortex-win.data.microsoft.com                                                                     2021-09-22 18:03:13  2021-11-23 13:36:57  Xbox things                                       
   26     0           1  0             settings-win.data.microsoft.com                                                                       2021-09-22 18:03:13  2021-11-23 13:36:57  Xbox things                                       
   38     0           1  0             xkms.xbolive.com                                                                                      2022-02-03 22:16:52  2022-02-03 22:16:52                                                    
   45     0           1  0             displaycatalog.mp.microsoft.com                                                                       2022-02-03 22:22:39  2022-02-03 22:22:39                                                    
   46     0           1  0             umwatson.events.data.microsoft.com                                                                    2022-02-05 08:45:46  2022-02-05 08:45:46                                                    
   47       2         1  0             (\.|^)https://rocketreach\.co$                                                                        2022-03-17 15:15:10  2022-03-17 15:17:34  RocketReach                                       

*** [ DIAGNOSING ]: Clients

*** [ DIAGNOSING ]: Adlists
   id     enabled  group_ids     address                                                                                               date_added           date_modified        comment                                           
   -----  -------  ------------  ----------------------------------------------------------------------------------------------------  -------------------  -------------------  --------------------------------------------------
   1            1  0             https://raw.githubusercontent.com/StevenBlack/hosts/master/hosts                                      2021-09-18 18:01:30  2021-09-18 18:01:30  Migrated from /etc/pihole/adlists.list            
   2            1  0             https://dbl.oisd.nl/                                                                                  2021-09-18 18:51:00  2021-09-18 18:51:00  Apple News and More                               
   4            1  0             https://adaway.org/hosts.txt                                                                          2021-09-19 00:59:04  2021-09-19 00:59:04                                                    
   5            1  0             https://v.firebog.net/hosts/AdguardDNS.txt                                                            2021-09-19 00:59:14  2021-09-19 00:59:14                                                    
   6            1  0             https://v.firebog.net/hosts/Admiral.txt                                                               2021-09-19 00:59:27  2021-09-19 00:59:27                                                    
   7            1  0             https://raw.githubusercontent.com/anudeepND/blacklist/master/adservers.txt                            2021-09-19 00:59:37  2021-09-19 00:59:37                                                    
   8            1  0             https://s3.amazonaws.com/lists.disconnect.me/simple_ad.txt                                            2021-09-19 00:59:47  2021-09-19 00:59:47                                                    
   9            1  0             https://v.firebog.net/hosts/Easylist.txt                                                              2021-09-19 00:59:59  2021-09-19 00:59:59                                                    
   10           1  0             https://pgl.yoyo.org/adservers/serverlist.php?hostformat=hosts&showintro=0&mimetype=plaintext         2021-09-19 01:00:08  2021-09-19 01:00:08                                                    
   11           1  0             https://raw.githubusercontent.com/FadeMind/hosts.extras/master/UncheckyAds/hosts                      2021-09-19 01:00:17  2021-09-19 01:00:17                                                    
   12           1  0             https://raw.githubusercontent.com/bigdargon/hostsVN/master/hosts                                      2021-09-19 01:00:25  2021-09-19 01:00:25                                                    
   13           1  0             https://raw.githubusercontent.com/PolishFiltersTeam/KADhosts/master/KADhosts.txt                      2021-09-19 01:00:43  2021-09-19 01:00:43                                                    
   14           1  0             https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.Spam/hosts                         2021-09-19 01:00:51  2021-09-19 01:00:51                                                    
   15           1  0             https://v.firebog.net/hosts/static/w3kbl.txt                                                          2021-09-19 01:00:59  2021-09-19 01:00:59                                                    
   16           1  0             https://v.firebog.net/hosts/Easyprivacy.txt                                                           2021-09-19 01:01:30  2021-09-19 01:01:30                                                    
   17           1  0             https://v.firebog.net/hosts/Prigent-Ads.txt                                                           2021-09-19 01:01:39  2021-09-19 01:01:39                                                    
   18           1  0             https://raw.githubusercontent.com/FadeMind/hosts.extras/master/add.2o7Net/hosts                       2021-09-19 01:01:47  2021-09-19 01:01:47                                                    
   19           1  0             https://raw.githubusercontent.com/crazy-max/WindowsSpyBlocker/master/data/hosts/spy.txt               2021-09-19 01:02:01  2021-09-19 01:02:01                                                    
   20           1  0             https://hostfiles.frogeye.fr/firstparty-trackers-hosts.txt                                            2021-09-19 01:02:11  2021-09-19 01:02:11                                                    

*** [ DIAGNOSING ]: contents of /etc/pihole

-rw-r--r-- 1 root root 0 Sep 18  2021 /etc/pihole/custom.list

-rw-r--r-- 1 root root 65 Apr  3 03:01 /etc/pihole/local.list

-rw-r--r-- 1 root root 234 Sep 18  2021 /etc/pihole/logrotate
   /var/log/pihole.log {
   	su root root
   	daily
   	copytruncate
   	rotate 5
   	compress
   	delaycompress
   	notifempty
   	nomail
   }
   /var/log/pihole-FTL.log {
   	su root root
   	weekly
   	copytruncate
   	rotate 3
   	compress
   	delaycompress
   	notifempty
   	nomail
   }

-rw-rw-r-- 1 pihole root 15 Feb 19 21:26 /etc/pihole/pihole-FTL.conf
   PRIVACYLEVEL=0

*** [ DIAGNOSING ]: contents of /etc/dnsmasq.d

-rw-r--r-- 1 root root 1.9K Mar 13 20:27 /etc/dnsmasq.d/01-pihole.conf
   addn-hosts=/etc/pihole/local.list
   addn-hosts=/etc/pihole/custom.list
   localise-queries
   no-resolv
   cache-size=10000
   log-queries
   log-facility=/var/log/pihole.log
   log-async
   server=208.67.222.222
   server=208.67.220.220
   server=2620:119:35::35
   server=2620:119:53::53
   server=4.2.2.1
   server=4.2.2.2
   server=8.26.56.26
   server=8.20.247.20
   server=84.200.69.80
   server=84.200.70.40
   server=2001:1608:10:25:0:0:1c04:b12f
   server=2001:1608:10:25:0:0:9249:d69b
   server=9.9.9.9
   server=149.112.112.112
   server=2620:fe::fe
   server=2620:fe::9
   server=9.9.9.10
   server=149.112.112.10
   server=2620:fe::10
   server=2620:fe::fe:10
   server=9.9.9.11
   server=149.112.112.11
   server=2620:fe::11
   server=2620:fe::fe:11
   server=1.1.1.1
   server=1.0.0.1
   server=2606:4700:4700::1111
   server=2606:4700:4700::1001
   domain-needed
   expand-hosts
   bogus-priv
   local-service

-rw-r--r-- 1 root root 2.2K Feb 19 21:26 /etc/dnsmasq.d/06-rfc6761.conf
   server=/test/
   server=/localhost/
   server=/invalid/
   server=/bind/
   server=/onion/

*** [ DIAGNOSING ]: contents of /etc/lighttpd

-rw-r--r-- 1 root root 0 Feb 19 21:26 /etc/lighttpd/external.conf

-rw-r--r-- 1 root root 3.7K Feb 19 21:26 /etc/lighttpd/lighttpd.conf
   server.modules = (
       "mod_access",
       "mod_accesslog",
       "mod_auth",
       "mod_expire",
       "mod_redirect",
       "mod_setenv",
       "mod_rewrite"
   )
   server.document-root        = "/var/www/html"
   server.error-handler-404    = "/pihole/index.php"
   server.upload-dirs          = ( "/var/cache/lighttpd/uploads" )
   server.errorlog             = "/var/log/lighttpd/error.log"
   server.pid-file             = "/run/lighttpd.pid"
   server.username             = "www-data"
   server.groupname            = "www-data"
   server.port                 = 80
   accesslog.filename          = "/var/log/lighttpd/access.log"
   accesslog.format            = "%{%s}t|%V|%r|%s|%b"
   index-file.names            = ( "index.php", "index.html", "index.lighttpd.html" )
   url.access-deny             = ( "~", ".inc", ".md", ".yml", ".ini" )
   static-file.exclude-extensions = ( ".php", ".pl", ".fcgi" )
   mimetype.assign = (
       ".ico"   => "image/x-icon",
       ".jpeg"  => "image/jpeg",
       ".jpg"   => "image/jpeg",
       ".png"   => "image/png",
       ".svg"   => "image/svg+xml",
       ".css"   => "text/css; charset=utf-8",
       ".html"  => "text/html; charset=utf-8",
       ".js"    => "text/javascript; charset=utf-8",
       ".json"  => "application/json; charset=utf-8",
       ".map"   => "application/json; charset=utf-8",
       ".txt"   => "text/plain; charset=utf-8",
       ".eot"   => "application/vnd.ms-fontobject",
       ".otf"   => "font/otf",
       ".ttc"   => "font/collection",
       ".ttf"   => "font/ttf",
       ".woff"  => "font/woff",
       ".woff2" => "font/woff2"
   )
   include_shell "cat external.conf 2>/dev/null"
   include_shell "/usr/share/lighttpd/use-ipv6.pl " + server.port
   include_shell "find /etc/lighttpd/conf-enabled -name '*.conf' -a ! -name 'letsencrypt.conf' -printf 'include \"%p\"
' 2>/dev/null"
   $HTTP["url"] =~ "^/admin/" {
       setenv.add-response-header = (
           "X-Pi-hole" => "The Pi-hole Web interface is working!",
           "X-Frame-Options" => "DENY"
       )
   }
   $HTTP["url"] =~ "^/admin/\.(.*)" {
       url.access-deny = ("")
   }
   $HTTP["url"] =~ "/(teleporter|api_token)\.php$" {
       $HTTP["referer"] =~ "/admin/settings\.php" {
           setenv.add-response-header = ( "X-Frame-Options" => "SAMEORIGIN" )
       }
   }
   expire.url = ( "" => "access plus 0 seconds" )

*** [ DIAGNOSING ]: contents of /etc/cron.d

-rw-r--r-- 1 root root 1.8K Feb 19 21:26 /etc/cron.d/pihole
   1 3   * * 7   root    PATH="$PATH:/usr/sbin:/usr/local/bin/" pihole updateGravity >/var/log/pihole_updateGravity.log || cat /var/log/pihole_updateGravity.log
   00 00   * * *   root    PATH="$PATH:/usr/sbin:/usr/local/bin/" pihole flush once quiet
   @reboot root /usr/sbin/logrotate --state /var/lib/logrotate/pihole /etc/pihole/logrotate
   */10 *  * * *   root    PATH="$PATH:/usr/sbin:/usr/local/bin/" pihole updatechecker local
   32 15  * * *   root    PATH="$PATH:/usr/sbin:/usr/local/bin/" pihole updatechecker remote
   @reboot root    PATH="$PATH:/usr/sbin:/usr/local/bin/" pihole updatechecker remote reboot

*** [ DIAGNOSING ]: contents of /var/log/lighttpd

-rw-r--r-- 1 www-data www-data 303 Apr  3 13:01 /var/log/lighttpd/error.log
   -----head of error.log------
   2022-04-03 00:00:44: (server.c.1759) logfiles cycled UID = 0 PID = 9156 
   2022-04-03 13:01:30: (server.c.2059) server stopped by UID = 0 PID = 1 
   2022-04-03 13:01:40: (server.c.1464) server started (lighttpd/1.4.53) 
   2022-04-03 13:01:40: (server.c.1493) WARNING: unknown config-key: alias.url (ignored) 

   -----tail of error.log------
   2022-04-03 00:00:44: (server.c.1759) logfiles cycled UID = 0 PID = 9156 
   2022-04-03 13:01:30: (server.c.2059) server stopped by UID = 0 PID = 1 
   2022-04-03 13:01:40: (server.c.1464) server started (lighttpd/1.4.53) 
   2022-04-03 13:01:40: (server.c.1493) WARNING: unknown config-key: alias.url (ignored) 

*** [ DIAGNOSING ]: contents of /var/log

-rw-r--r-- 1 pihole pihole 554 Apr  9 07:58 /var/log/pihole-FTL.log
   -----head of pihole-FTL.log------
   [2022-04-09 05:06:43.912 28769M] Rate-limiting 192.168.4.1 for at least 3 seconds
   [2022-04-09 05:06:46.149 28769/T28774] Ending rate-limitation of 192.168.4.1
   [2022-04-09 07:28:48.403 28769M] Resizing "FTL-dns-cache" from 196608 to (12544 * 16) == 200704 (/dev/shm: 17.9MB used, 484.6MB total, FTL uses 17.8MB)
   [2022-04-09 07:57:25.019 28769M] Rate-limiting 192.168.4.1 for at least 21 seconds
   [2022-04-09 07:57:46.042 28769/T28774] Ending rate-limitation of 192.168.4.1
   [2022-04-09 07:58:19.865 28769M] Rate-limiting 192.168.4.1 for at least 27 seconds

   -----tail of pihole-FTL.log------
   [2022-04-09 05:06:43.912 28769M] Rate-limiting 192.168.4.1 for at least 3 seconds
   [2022-04-09 05:06:46.149 28769/T28774] Ending rate-limitation of 192.168.4.1
   [2022-04-09 07:28:48.403 28769M] Resizing "FTL-dns-cache" from 196608 to (12544 * 16) == 200704 (/dev/shm: 17.9MB used, 484.6MB total, FTL uses 17.8MB)
   [2022-04-09 07:57:25.019 28769M] Rate-limiting 192.168.4.1 for at least 21 seconds
   [2022-04-09 07:57:46.042 28769/T28774] Ending rate-limitation of 192.168.4.1
   [2022-04-09 07:58:19.865 28769M] Rate-limiting 192.168.4.1 for at least 27 seconds

*** [ DIAGNOSING ]: contents of /dev/shm
-rw------- 1 pihole pihole 668K Apr  9 07:36 /dev/shm/FTL-clients
-rw------- 1 pihole pihole 240 Apr  7 10:07 /dev/shm/FTL-counters
-rw------- 1 pihole pihole 196K Apr  7 10:07 /dev/shm/FTL-dns-cache
-rw------- 1 pihole pihole 140K Apr  8 15:22 /dev/shm/FTL-domains
-rw------- 1 pihole pihole 56 Apr  7 10:07 /dev/shm/FTL-lock
-rw------- 1 pihole pihole 12K Apr  7 10:07 /dev/shm/FTL-overTime
-rw------- 1 pihole pihole 4.0K Apr  7 10:07 /dev/shm/FTL-per-client-regex
-rw------- 1 pihole pihole 16M Apr  7 10:59 /dev/shm/FTL-queries
-rw------- 1 pihole pihole 12 Apr  7 10:07 /dev/shm/FTL-settings
-rw------- 1 pihole pihole 240K Apr  8 23:00 /dev/shm/FTL-strings
-rw------- 1 pihole pihole 156K Apr  7 10:07 /dev/shm/FTL-upstreams

*** [ DIAGNOSING ]: contents of /etc

-rw-r--r-- 1 root root 24 Feb 19 21:26 /etc/dnsmasq.conf
   conf-dir=/etc/dnsmasq.d

-rw-r--r-- 1 root root 87 Apr  3 13:01 /etc/resolv.conf
   nameserver 1.1.1.1
   nameserver 1.0.0.1
   nameserver 192.168.4.1

*** [ DIAGNOSING ]: Pi-hole diagnosis messages
   id    timestamp            type                  message                                                       blob1                 blob2                 blob3                 blob4                 blob5               
   ----  -------------------  --------------------  ------------------------------------------------------------  --------------------  --------------------  --------------------  --------------------  --------------------
   523   2022-04-09 07:58:19  RATE_LIMIT            192.168.4.1                                                   1000                  60                                                                                    

*** [ DIAGNOSING ]: Locale
    LANG=

*** [ DIAGNOSING ]: Pi-hole log
-rw-r--r-- 1 pihole pihole 49M Apr  9 07:58 /var/log/pihole.log
   -----head of pihole.log------
   Apr  9 00:00:24 dnsmasq[28769]: query[A] api.ring.com from 192.168.4.1
   Apr  9 00:00:24 dnsmasq[28769]: forwarded api.ring.com to 4.2.2.1
   Apr  9 00:00:24 dnsmasq[28769]: reply api.ring.com is <CNAME>
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 100.26.103.157
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 52.45.53.55
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 54.197.47.195
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 18.214.155.45
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 52.1.7.58
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 18.211.139.8
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 52.200.138.148
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 35.174.54.35
   Apr  9 00:00:24 dnsmasq[28769]: query[AAAA] api.ring.com from 192.168.4.1
   Apr  9 00:00:24 dnsmasq[28769]: forwarded api.ring.com to 4.2.2.1
   Apr  9 00:00:24 dnsmasq[28769]: query[A] clientsapigw.us-east-1.gws.ring.com from 192.168.4.1
   Apr  9 00:00:24 dnsmasq[28769]: forwarded clientsapigw.us-east-1.gws.ring.com to 4.2.2.1
   Apr  9 00:00:24 dnsmasq[28769]: reply api.ring.com is <CNAME>
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is NODATA-IPv6
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 54.211.48.25
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 52.22.96.159
   Apr  9 00:00:24 dnsmasq[28769]: reply clientsapigw.us-east-1.gws.ring.com is 35.153.250.191

   -----tail of pihole.log------
   Apr  9 07:58:20 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:20 dnsmasq[28769]: Rate-limiting tvpnlogopeu.samsungcloud.tv is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: query[A] api.ring.com from 192.168.4.1
   Apr  9 07:58:21 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: Rate-limiting api.ring.com is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: query[AAAA] api.ring.com from 192.168.4.1
   Apr  9 07:58:21 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: Rate-limiting api.ring.com is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: query[AAAA] app-measurement.com from 192.168.4.1
   Apr  9 07:58:21 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: Rate-limiting app-measurement.com is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: query[A] app-measurement.com from 192.168.4.1
   Apr  9 07:58:21 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:21 dnsmasq[28769]: Rate-limiting app-measurement.com is REFUSED (EDE: blocked)
   Apr  9 07:58:22 dnsmasq[28769]: query[A] tvpnlogopeu.samsungcloud.tv from 192.168.4.1
   Apr  9 07:58:22 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:22 dnsmasq[28769]: Rate-limiting tvpnlogopeu.samsungcloud.tv is REFUSED (EDE: blocked)
   Apr  9 07:58:22 dnsmasq[28769]: query[AAAA] tvpnlogopeu.samsungcloud.tv from 192.168.4.1
   Apr  9 07:58:22 dnsmasq[28769]: config error is REFUSED (EDE: blocked)
   Apr  9 07:58:22 dnsmasq[28769]: Rate-limiting tvpnlogopeu.samsungcloud.tv is REFUSED (EDE: blocked)


********************************************
********************************************
[✓] ** FINISHED DEBUGGING! **
