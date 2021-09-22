# How to summarize the information in a .pcap/.pcapng file?
```capinfos <file.pcap>```

# How to split a .pcap/.pcapng file?
```tcpdump -r <old_file.pcap> -w <new_files> -C 10``` : splits on every ~10 MB

```editcap -c 1000 input.pcap output.pcap``` : splits on 1000 packets

**Honourable mentions:**
- PcapSplitter: part of https://github.com/seladb/PcapPlusPlus
- SplitCap: https://www.netresec.com/index.ashx?page=SplitCap

# How to convert from pcapng to pcap?
```editcap -F libpcap <old_file.pcapng> <new_file.pcap>```

# How to merge .nfdump(S) into a single .csv?
```nfdump -R <directory_with_nfcapds> > merged_nfcapd.csv```
