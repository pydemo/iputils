# iputils

source: https://github.com/iputils/iputils

## get rid of 'Operation not permitted'
```
./ping/ping oracle.com
./ping/ping: socket: Operation not permitted
```
```
sudo setcap 'cap_net_admin,cap_net_raw+ep' ./ping/ping
```

./ping/ping  google.com
```
PING google.com (172.217.6.14) 56(84) bytes of data.
64 bytes from ord38s01-in-f14.1e100.net (172.217.6.14): icmp_seq=1 ttl=101 time=17.4 ms
64 bytes from ord38s01-in-f14.1e100.net (172.217.6.14): icmp_seq=2 ttl=101 time=17.6 ms
64 bytes from ord38s01-in-f14.1e100.net (172.217.6.14): icmp_seq=3 ttl=101 time=17.5 ms
64 bytes from ord38s01-in-f14.1e100.net (172.217.6.14): icmp_seq=4 ttl=101 time=17.4 ms
```
