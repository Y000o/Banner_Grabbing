##Banner grabbing

{ echo -e "GET / HTTP/1.0\r\nHost: <host>\r\n\r" >&3; cat <&3 ; } 3<> /dev/tcp - udp/<host>/80

-Ncat:

nc -v <IP> 21
nc -v <IP> 22
nc -v <IP> 80 
HEAD / HTTP/1.0
HEAD / HTTP/1.1

-Telnet

telnet <IP> 22

-Curl

curl -I <IP> | grep -e “Server: ”

-Nmap

nmap -sV --script=banner <IP>

-Echo + ncat

echo "" | nc -v -n -w1 <IP> 80

Curl:

-curl -s -v -D - "https://ejemplo" > /dev/null

Openssl

-openssl s_client -connect "host:puerto"

-echo | openssl s_client -connect host:puerto | openssl x509 -text -noout

Wget

-wget IP -q -S


