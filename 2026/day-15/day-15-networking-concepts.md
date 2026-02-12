Challenge Tasks

Task 1: DNS – How Names Become IPs

1. Explain in 3–4 lines: what happens when you type google.com in a browser?
-> When we type google.com in a browser basically its an application layer. When we get the webpage that's our presentation layer. Once it starts with its session thats session layer. It transports to TCP thats transport layer then it maps to the IP thats network layer & finally it gets connect to the network.

3. What are these record types? Write one line each:
    * A, AAAA, CNAME, MX, NS
-> A - Maps a domain for IPv4.
  AAAA - Maps domain for IPv6.
  CNAME - Maps a domain name to another domain name.
  MX - Got it from AI tool but didnot get it.
  NS - Got it from AI tool but didnot get it.

4. Run: dig google.com — identify the A record and TTL from the output
<img width="639" height="382" alt="Screenshot 2026-02-12 at 5 49 19 PM" src="https://github.com/user-attachments/assets/8a8f4345-697f-4ad2-81ce-d27467db941c" />
-> A record gives the IPv4 address with TTL(Time To Live) 61 seconds.

Task 2: IP Addressing

1. What is an IPv4 address? How is it structured? (e.g., 192.168.1.10)
->IPv4 is structured from 0.0.0.1 to 255.255.255.254

2. Difference between public and private IPs — give one example of each
->Public IP can be used by anyone & private IP can be used only by its server. Public IPs are kind of risky based on security on other hand, private IPs are secure.
Eg. App frontend IP can be public because we want to have it accessed by everyone. Private IP can be the backend of application which is handling the DB.

3. What are the private IP ranges?
    * 10.x.x.x, 172.16.x.x – 172.31.x.x, 192.168.x.x
  10.0.0.0 : Range - 16,777,216
  172.16.0.1 – 172.31.x.x : Range - 1,048,576
  192.168.x.x : Range - 65,536


4. Run: ip addr show — identify which of your IPs are private
->172.31.21.105
<img width="817" height="211" alt="Screenshot 2026-02-12 at 5 25 09 PM" src="https://github.com/user-attachments/assets/cb37d42e-97ff-4082-95d6-01a3f7f60457" />


Task 3: CIDR & Subnetting

1. What does /24 mean in 192.168.1.0/24?
-> Its a CIDR notation. Where we can have total of 256 IPs.
  
3. How many usable hosts in a /24? A /16? A /28?
-> /24 = 256 hosts
   /16 = 65,536 hosts
   /28 = 16 hosts

5. Explain in your own words: why do we subnet?
-> As IP can be exceed after it crosses its limit so to avoid this risk we can use subnet which is basically same as internet. Where can have same IP used in different subnets because it doesnnot lie under same network.

7. Quick exercise — fill in:
CIDR	Subnet Mask	Total IPs	Usable Hosts
/24	255.255.255.0	256	255.255.255.254 (Last usable host)
/16	255.255.0.0	65,536	255.255.255.254 (Last usable host)
/28	255.255.255.240	16	255.255.255.14 (Last usable host)


Task 4: Ports – The Doors to Services

1. What is a port? Why do we need them?
-> Ports are actually assigned to the application/webserver.

3. Document these common ports:
Port	Service
22	**SSH**
80	**Local webserver**
443 **	HTTPS**
   
	3	Run ss -tulpn — match at least 2 listening ports to their services
<img width="1434" height="243" alt="Screenshot 2026-02-12 at 5 33 17 PM" src="https://github.com/user-attachments/assets/7b0a7678-9a23-40e1-98f1-e755f9ef4011" />
It matches 2 listening ports i.e. 22 for ssh & 80 is of local webserver(nginx).


Task 5: Putting It Together

Answer in 2–3 lines each:
* You run curl http://myapp.com:8080 — what networking concepts from today are involved?
Unable to connect to the URL as it got timed out.
I think, the concepts are involved such as Protocols(HTTP/HTTPS,DNS/IP).  

* Your app can't reach a database at 10.0.1.50:3306 — what would you check first?
-> Whether this port is establishing a connection or not.
  WHether port is in listening state.
  If above both cases work then will check for mysql service.

What you learned :
1. Learned about how internet connectivity works.
2. Learned about OSI & TCP/IP models with having understanding of each layer & how we can apply these layer in real life scenarios.
3. CIDR & IP, ports, subnets - leanred about these concepts. 
