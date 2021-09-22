# .pcap and .nfdump swiss knife
The goal of this repo is to summarize a list of commands usefull to deal with pcap, pcapng and nfdump/netflow type of files

## How to summarize the information in a .pcap/.pcapng file?
```capinfos <file.pcap>```

## How to split a .pcap/.pcapng file?
```tcpdump -r <old_file.pcap> -w <new_files> -C 10``` : splits on every ~10 MB

```editcap -c 1000 input.pcap output.pcap``` : splits on 1000 packets

**Honourable mentions:**
- PcapSplitter: part of https://github.com/seladb/PcapPlusPlus
- SplitCap: https://www.netresec.com/index.ashx?page=SplitCap

## How to convert from pcapng to pcap?
```editcap -F libpcap <old_file.pcapng> <new_file.pcap>```

## How to merge .nfdump(S) into a single .csv?
```nfdump -R <directory_with_nfcapds> > <output_file.csv>```
```nfdump -r <nflow_file> -o extended -o csv > <output_file.csv>``` export netflow to csv

## How to convert a packet-based to a flow-based file?
**Read:** https://gist.github.com/jjsantanna/f2ee2f1fe23208299f4a2ca392f8b23f

```nfpcapd -r <path_to_pcap_file.pcap> -l <output_directory.netflow>``` 

