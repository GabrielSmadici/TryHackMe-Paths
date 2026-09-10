This is a cheatsheet for TCPDump commands and my understanding of them.

tcpdump -i -> tells tcpdump to start listening on a certain interface, eg. tcpdump -i eth0
-i any -> if you don't knwo on which interface to listen to you can use 'any' to listen on all of them
ip a s -> linux comand that lists available interfaces

-w -> save to file, format: -w [file-name]

-r -> read from file, format: -r [file-name]

-c -> specify the numper of packets to capture, format: -c [number]

-n -> don't use domain names instead of ips

-nn -> stops port numbers from being resolved and doesn't use domain names for ips

-v (-vv -vvv) -> more verbouse output

src -> filters by source (packets received), format: src [condition] [value]
dst -> filters by destination (packets sent), format: dst host [condition] [value]

host -> listen to specific target, formats: host [ip], host [host-name]

port -> filters by port number, format: src/dst port [number]

protocol (you don't type protocol you just type the specific one) -> filters by protocol, format: [protocol (eg. tcp, upd, icmp tec.)]

logical gates can be used when filtering -> eg. src host 10.10.10.1 and port 6666 and not tcp

greater/less -> filter by size (in bytes), format: greater/less [length]




