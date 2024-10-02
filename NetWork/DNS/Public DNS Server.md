Public DNS server is a publicly available DNS server for multiple users and is one of the most frequently used services on the Internet. Public DNS server is an alternative DNS server that can be used in place of the primary DNS server provided by Internet Service Providers (ISPs). This server translates domain names to IP addresses and is primarily used to speed up, enhance security, or avoid filtering specific content.
# Why DNS server has IP address?
DNS servers are responsible for translating domain names into IP addresses, but since this DNS server itself is a server, it has a unique IP address like any other server. For example, just as the DNS server IP address of Cloudflare is `1.1.1.1`, DNS servers need IP addresses to communicate over the Internet. Users can use the DNS server by entering the public DNS server IP address directly in their network settings.
# Role of Public DNS Server IP Addresses
- **Fast inquiry speed**: Public DNS servers enable faster lookup of IP addresses for specific domains. In particular, public DNS servers such as Cloudflare and Google can provide faster and more efficient service delivery through distributed data centers around the world.
- **Stronger Security**: Some public DNS servers provide security features that block phishing or malicious sites by default. For example, OpenDNS can block security threats based on filtering policies that you set.
- **Accessibility and privacy protection**: Some public DNS servers can be used in place of DNS servers provided by ISPs, and privacy can be enhanced through log storage policies, etc. Cloudflare's 1.1.1.1 is famous for its log-free policy.
# Public DNS server workflow
1. A user enters a domain name in a web browser: for example, www.example.com .  
2. Request to a Public DNS server: If you have enabled a Public DNS server in your network settings (for example,`1.1.1.1` in Cloudflare or `8.8.8.8` in Google), the browser requests the IP address of the domain name from that Public DNS server. This Public DNS server will act as a Recursive DNS server.  
3. Public DNS Server checks the cache: The public DNS server first checks that the information it has cached has the domain's IP address. Because many users access from around the world, public DNS servers store frequently requested domain information in their cache. If there is cached information, it can return the IP address immediately and respond quickly without going through a Root or TLD server.  
4. If there is no information in the cache: If a domain request is received that is not in the cache, the Public DNS server still passes through the Root server, the TLD server, and the Authoritative DNS server to find the IP address, which is the same as the basic DNS lookup process.  
	- Root server: Returns information about the top-level domain (for example, .com) of the domain name.  
	- TLD Server: Forwarding requests to servers with DNS information for a particular top-level domain (e.g., `.com`).  
	- Authentic DNS server: The server that holds the final IP address of the domain name, and finally returns the IP address.  
5. IP address return and caching: The Public DNS server returns the IP address it obtained to the user and stores the information in the cache for a certain period of time. The next time there is a request for the same domain, the cache will be able to respond directly without going through the Root or TLD servers.

---
Reference link 🙂     
https://www.webhostface.com/kb/knowledgebase/public-dns/