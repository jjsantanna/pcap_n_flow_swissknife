# On how to split a .pcap/.pcapng file

```tcpdump -r <old_file> -w <new_files> -C 10```
```tcpdump -r old_file -w new_files -C 1000``` splits on every 955MB of recorded traffic

