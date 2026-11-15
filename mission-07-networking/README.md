# Mission 07 — How Computers Communicate

## 1. Task / Objective

The objective of this mission is to understand basic network types and concepts, observe network lookup and connectivity information, and describe what happens when a website opens.

In this mission, I explored different network concepts, performed connectivity tests and DNS lookups using macOS Terminal, and understood how computers communicate when accessing a website.

## 2. Work Completed

### Task 7.1 — Explain Network Concepts

A computer network connects devices so they can exchange data and share resources.

**Network Concepts**

| Concept | Explanation | Example |
|---|---|---|
| LAN (Local Area Network) | A network covering a small geographical area, such as a home, laboratory or office. | Home Wi-Fi network |
| MAN (Metropolitan Area Network) | A network covering a city or a large campus area. | City-wide university network |
| WAN (Wide Area Network) | A network covering large geographical areas and connecting multiple smaller networks. | The Internet |
| DNS (Domain Name System) | Translates a domain name into an IP address. | Resolving example.com |
| Router | Connects different networks and forwards data between them. | Home Wi-Fi router |
| Protocol | A set of rules that devices follow to communicate with each other. | HTTP, HTTPS and TCP |
| Packet Switching | Divides data into smaller packets that travel across a network and are reassembled at the destination. | Sending data over the Internet |
| Client-Server | A communication model in which a client requests a service and a server provides it. | A browser requesting a webpage |

### Task 7.2 — Observe Network Information

I used Terminal on macOS to check network connectivity and perform a DNS lookup.

**1. Connectivity Test Using Ping**

**Command Used**

```bash
ping -c 4 example.com
```

**Purpose**

The ping command checks whether my computer can communicate with another server over a network. It also measures response time and packet loss.

**My Observations**

| Information | Result |
|---|---|
| Website tested | example.com |
| Packets transmitted | 4 |
| Packets received | 4 |
| Packet loss | 0% |
| Minimum response time | 50.851 ms |
| Average response time | 106.933 ms |
| Maximum response time | 156.824 ms |

**What I Observed**

The computer successfully communicated with example.com. All four packets were received, resulting in 0% packet loss. The response times varied, showing how long the server took to respond to each request.

**2. DNS Lookup**

**Command Used**

```bash
nslookup example.com
```

**Purpose**

The nslookup command is used to find the IP address associated with a domain name.

**My Observations**

| Information | Result |
|---|---|
| Domain name | example.com |
| DNS lookup | Successful |
| First resolved IP address | 104.20.23.154 |
| Second resolved IP address | 172.66.147.243 |

The DNS resolver details have been excluded to protect network privacy.

**What I Observed**

The DNS lookup successfully translated the domain name example.com into IP addresses. It also displayed information about the DNS server that handled the request.

**3. Answers to the Questions**

**Q1. What does a connectivity test help you check?**

A connectivity test checks whether my computer can communicate with another device or server over a network. It also provides information about response time and packet loss.

**Q2. What information does a DNS lookup display?**

A DNS lookup displays the IP addresses associated with a domain name and information about the DNS server that provided the response.

**Q3. Describe the role of DNS when you enter a website name in a browser.**

DNS translates a human-readable domain name into an IP address, allowing the browser to locate and communicate with the correct web server.

### Task 7.3 — What Happens When You Open a Website?

The following steps explain how a website loads when a user enters its address in a browser.

1. **Entering the URL:** The user enters a website address into the browser, which acts as the client.

2. **DNS Lookup:** The browser uses DNS to find the IP address associated with the domain name.

3. **Network Communication:** The request travels through the network, including the router, towards the website's server.

4. **Connection Establishment:** The client establishes a connection with the server using network protocols such as TCP and TLS for HTTPS.

5. **Sending the Request:** The browser sends an HTTP or HTTPS request to the server asking for the webpage.

6. **Server Response:** The server processes the request and sends back the webpage data, including HTML, CSS and JavaScript files.

7. **Displaying the Website:** The browser processes the received data and displays the webpage to the user.

## 3. Commands / Tools Used

| Command / Tool | Purpose |
|---|---|
| `ping -c 4 example.com` | Tests network connectivity and measures response time. |
| `nslookup example.com` | Performs a DNS lookup to find domain IP addresses. |
| macOS Terminal (Zsh) | Used to execute network commands and observe their output. |

## 4. My Understanding

Through this mission, I understood how computers communicate over networks and how different networking components work together.

I learned the following concepts:

1. **LAN, MAN and WAN:** Different network types are classified according to the geographical area they cover.
2. **DNS:** DNS translates human-readable domain names into IP addresses.
3. **Router:** A router connects different networks and forwards data between them.
4. **Protocols:** Protocols provide rules that allow devices to communicate.
5. **Packet Switching:** Data is divided into smaller packets that travel across a network.
6. **Client-Server Model:** A client requests a service, and a server responds to that request.

I also understood how the `ping` command checks network connectivity and how `nslookup` finds IP addresses associated with domain names.

Finally, I learned the sequence of events involved in opening a website, from entering its URL to receiving the server response and displaying the webpage.

## 5. Difficulties Faced

Initially, I needed to understand the difference between a connectivity test and a DNS lookup.

I also needed to understand how the different networking components, such as DNS, routers, clients and servers, work together when a website is opened.

## 6. How I Resolved Them

I resolved my confusion by practising the `ping` and `nslookup` commands in Terminal and observing their outputs.

By comparing the results, I understood that `ping` checks connectivity and response time, whereas `nslookup` retrieves IP address information associated with a domain name.

I also studied the role of each networking component and arranged the website-loading process into seven steps to understand it more clearly.

## 7. Evidence / Files

The following work and outputs are associated with this mission:

- `mission-07-networking/README.md` — Documentation of network concepts, observations and website communication.
- Ping command output — Connectivity test results for example.com.
- DNS lookup output — IP addresses obtained using nslookup.
- Network concepts table — Explanation of LAN, MAN, WAN, DNS, router, protocols, packet switching and client-server communication.
- Website communication steps — Seven-step explanation of how a website opens in a browser.

No personal IP address, Wi-Fi name or private network information is included.

## 8. Commit Details

**Suggested Commit Message:**

```bash
Explain networking concepts and website communication
```

The mission documentation should be staged, committed and pushed to GitHub separately.

## 9. Conclusion

Mission 7 helped me understand how computers communicate over networks and how websites are accessed through DNS, routers, servers and communication protocols.

By performing practical network commands and studying the website communication process, I gained a better understanding of how the Internet works.