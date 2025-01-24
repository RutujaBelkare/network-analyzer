Here’s how you can develop a simple packet sniffer tool in Python. This program will capture and analyze network packets, displaying details like source and destination IP addresses, protocols, and payload data.
We’ll use the socket library and optionally the struct module for decoding packet headers. 
This is intended strictly for educational purposes and should only be used in environments where you have permission to monitor network traffic.
scapy provides a high-level interface for packet sniffing and analysis. The sniff function listens for packets, and you can define a custom packet_handler function to process each packet.
pkt.haslayer() is used to check if the packet contains a specific layer (Ethernet, IP, TCP, UDP, ICMP, etc.).
pkt[Ether].src and pkt[Ether].dst retrieve the source and destination MAC addresses.
pkt[IP].src and pkt[IP].dst retrieve the source and destination IP addresses.
You can extract the payload of TCP, UDP, or ICMP packets using pkt[TCP].payload, pkt[UDP].payload, or pkt[ICMP].payload.
