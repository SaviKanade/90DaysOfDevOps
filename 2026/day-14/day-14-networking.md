* OSI layers (L1–L7) vs TCP/IP stack (Link, Internet, Transport, Application)
![A955ACEC-3B20-44E0-A0CC-42D5834C4F11_4_5005_c](https://github.com/user-attachments/assets/29574db6-bde8-4f8c-a0ea-333ad373cdc1)


* Where IP, TCP/UDP, HTTP/HTTPS, DNS sit in the stack
     Application  ----> HTTP/HTTPS
     Transport  -----? TCP/UDP
     Internet  ---> IP address/Route
     Network Access  -----> MAC 

     

* One real example: “curl https://example.com = App layer over TCP over IP” layer :
<img width="1095" height="666" alt="Screenshot 2026-02-12 at 3 50 29 PM" src="https://github.com/user-attachments/assets/ae3520e4-968f-46b4-831e-175a327075fb" />
Application : https, webpage (presentation layer) 
Transport : TCP
Internet : IP


Hands-on Checklist 

* Identity: hostname -I (or ip addr show) — note your IP.
-> It gives your system's IP.


* Reachability: ping <target> — mention latency and packet loss.
<img width="959" height="241" alt="Screenshot 2026-02-12 at 3 40 32 PM" src="https://github.com/user-attachments/assets/faafa005-bfec-4d0d-a4be-ccfe7ec6ed3e" />
-> Ping checks the connectivity between your server & destination. Latency is nothing but the time difference which is showed in ping command.

Latency : 30.5ms
Packet loss : 0

* Path: traceroute <target> (or tracepath) — note any long hops/timeouts.
-> Yes, there were some long hops but no timeout.
<img width="1470" height="557" alt="Screenshot 2026-02-12 at 3 43 09 PM" src="https://github.com/user-attachments/assets/7e1c5854-3b14-4cf5-aeea-46f0e55f2384" />
Traceroute gives the routes of www.myntra.com traces. Basically, when we searched it & how it gives us its webpage. 


* Ports: ss -tulpn (or netstat -tulpn) — list one listening service and its port.
<img width="847" height="268" alt="Screenshot 2026-02-12 at 3 45 56 PM" src="https://github.com/user-attachments/assets/8f2276f2-4ebf-44ab-b967-6aad25230289" />
-> This command shows active connections list. LISTEN means the connection is open & the server is listening to that connection's port. 
Port - 22
Service - ssh.service

Port - 80
Service - nginx.service

* Name resolution: dig <domain> or nslookup <domain> — record the resolved IP.
<img width="454" height="164" alt="Screenshot 2026-02-12 at 3 48 05 PM" src="https://github.com/user-attachments/assets/91e15ef1-31de-42e1-80f1-1ef02646cb51" />
-> nslookup gives the DNS's IP 


* HTTP check: curl -I <http/https-url> — note the HTTP status code.
-> HTTP
  Note : didnot get it. like why we are checking http status code.

* Connections snapshot: netstat -an | head — count ESTABLISHED vs LISTEN (rough).
<img width="738" height="171" alt="Screenshot 2026-02-12 at 4 02 29 PM" src="https://github.com/user-attachments/assets/75ece8f9-9723-402a-a788-3d903734baaa" />
-> netstat command shows the active connections list. This command basically giving the connections list output along with head command which gives starting lines with word count for those connections which have ESTABLISHED & LISTENING. 


Mini Task: Port Probe & Interpret

1. Identify one listening port from ss -tulpn (e.g., SSH on 22 or a local web app).
-> 80 on NGINX

  
3. From the same machine, test it: nc -zv localhost <port> (or curl -I http://localhost:<port>).
    nc -zv tests the connectivity of port from our localhost.
  <img width="552" height="56" alt="Screenshot 2026-02-12 at 4 13 47 PM" src="https://github.com/user-attachments/assets/4206f496-e065-4803-b5db-47c16fee5425" />


5. Write one line: is it reachable? If not, what’s the next check? (e.g., service status, firewall).
-> Yes, its reachable.
   If its not reachable then firstly verify if that connection is connected to server or not. If yes, then check for that port if its listening. If yes, then verify the service status.



* Which command gives you the fastest signal when something is broken?
->It depends on the aspects i.e. APP, connectivity, port, service.
  curl will give the fastest signal if APP breaks.
  PING for reachability.
  netstat -tulpn for port listening.
  systemctl for services.

* What layer (OSI/TCP-IP) would you inspect next if DNS fails? If HTTP 500 shows up?
-> If DNS fails or if http 500 error shows up will inspect Application layer.
  
* Two follow-up checks you’d run in a real incident.
-> ping/if needed traceroute/curl with verbose mode(curl -vvv url)/netstat -tulpn or netstat -an
