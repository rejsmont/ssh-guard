ssh-guard
=========

Firewall host after a number of unsuccessful logins

Required packages:
shorewall
shorewall6
libberkeleydb-perl
libdatetime-perl
libsocket-getaddrinfo-perl

=Install (ubuntu)

sudo apt-get install libberkeleydb-perl libdatetime-perl libsocket-getaddrinfo-perl shorewall shorewall6

sudo mkdir -p /etc/ssh-guard
sudo mkdir -p /var/lib/ssh-guard
sudo mkdir -p /usr/local/sbin

sudo cp ssh-guard /usr/local/sbin
sudo cp whitelist /etc/ssh-guard
sudo cp ssh-guard-pam-config /usr/share/pam-configs/ssh-guard

sudo pam-auth-update
