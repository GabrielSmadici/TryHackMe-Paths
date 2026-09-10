This is a cheatsheet of Nmap commands and my understanding of them.

nmap -sn -> scans wherether the host is alive, format: namp -sn [ip/range of ips]
-sn works by sending ICMP/ARP/TCP probes to see ift he host if alive

nmap -sL -> lists target hosts on a network and resolvves them to their doman names (through DNS queries)
-sL is silent since it doesn't send packets to the hosts

nmap -sT -> connect scan, this tries to establish 3-way handshakes with TCP ports
-sT will tear down the established connections if they succeed

nmap -sS -> SYN or stealth scan, only sends a TCP SYN packet, no connection established, so more stealthy

nmap -sU -> UDP port scan (only sends packets since there is no need to establish a connection for UDP)

-sV -> detects the software and version on ports

-O -> detects the operating system running on the host (requirements: 1 open and 1 closed ports)

-A -> agressive scan, -sV + -O + --tracerounte (traces hops)

-Pn -> forces nmap to skip -sn to see if the target is alive, and scans the ports anyway, useful if the target blocks ping requests

-F -> scans most popular 100 ports instead of the default 1000

-p -> specify what ports to scan, eg. -p10-1024 scans ports 10->1024 or p- scans all the ports 1->65535

--min/max-prarallelism -> how many probes to send, format: nmap -sT --min-parallelism [number]

--min/max-rate -> how many packes per second, format: nmap -sT --min-rate [number]

--host-timeout -> wait time before moving on

-v -> verbouse (4 levels -v -vv -vvv -v4)

-d -> debugging (9 levels -d -dd ... -d9)

-oN -> save output into a file (normal type - .nmap)
-oX -> save output into XML file (.xml)
-oG -> save output into greppable file (.gnmap)
-oA -> save output in all formats