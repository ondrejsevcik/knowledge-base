# Timed `ping` to file

Useful when you want to track stability of your internet connection

```shell
# -i time in seconds
ping -i 5 google.com | xargs -L 1 -I '{}' date '+%+: {}' | tee ~/Desktop/pingLog.txt
```

output
```
Sun Mar 25 15:49:31 CEST 2018: PING google.com (172.217.16.174): 56 data bytes
Sun Mar 25 15:49:31 CEST 2018: 64 bytes from 172.217.16.174: icmp_seq=0 ttl=56 time=19.993 ms
Sun Mar 25 15:49:36 CEST 2018: 64 bytes from 172.217.16.174: icmp_seq=1 ttl=56 time=19.841 ms
Sun Mar 25 15:49:41 CEST 2018: 64 bytes from 172.217.16.174: icmp_seq=2 ttl=56 time=19.061 ms
Sun Mar 25 15:49:46 CEST 2018: 64 bytes from 172.217.16.174: icmp_seq=3 ttl=56 time=20.536 ms
```
