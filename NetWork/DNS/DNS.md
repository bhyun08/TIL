DNS is an abbreviation of **Domain Name System**. DNS is system that convert [[Domain Name]] into IP address. DNS plays a very important role because the Internet communicates through IP addresses by default. If there is no DNS, we must enter IP addresses in numbers, not domain names, when accessing the website.

For example, when we connect `localhost`, we can refer to oneself network. But when we connect `127.0.0.1`, we can also refer to oneself network. It means `localhost` and `127.0.0.1` have same IP address. Because DNS change `localhost` to `127.0.0.1`, we can connect `localhost` to `127.0.0.1`. This can be found in the host configuration file of the OS.
# DNS Components
![](https://velog.velcdn.com/images/zinukk/post/ae04e921-f5f7-43a3-9f07-28b3a9719719/image.png)
- **DNS Resolver**: When a user enters a domain name, the server is responsible for processing this request and finding the IP address.
- **DNS Root Server**: The top layer of the domain name system, which connects requests to appropriate top-level domain (TLD) servers.
- **TLD Server**: A server that manages information for top-level domains, such as `.com`, `.org`, and `.net`.
- **Authoritative DNS Server**: Server that provides the final IP address for a particular domain.
# DNS workflow
https://www.youtube.com/watch?v=27r4Bzuj5NQ
1. The user enters a domain name in a web browser.
2. DNS Resolver queries the Root server, TLD server, and Authoritative DNS server in order to find the IP address of the domain.
3. Finally, the Authentic DNS server checks the IP address of the domain and returns it to user.
4. The browser will use this IP address to connect to the server and access the user's desired web page.

---
Reference link 🙂     
https://aws.amazon.com/ko/route53/what-is-dns/
https://velog.io/@zinukk/9kpyzbdt