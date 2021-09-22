# On how to split a .pcap/.pcapng file

```tcpdump -r <old_file> -w <new_files> -C 10``` : splits on every 10 MB
```editcap -c 1000 input.pcap output.pcap``` : splits on 1000 packets. The output will be multiple capture files formatted like output_{index}_{timestamp}.pcap 

### honourable mentions:
- https://github.com/seladb/PcapPlusPlus
- https://www.netresec.com/index.ashx?page=SplitCap
