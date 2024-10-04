ISP(Internet Service Provider) mostly operate one's own DNS server and when customer connect to internet, basically use this ISP's DNS server. ISP's DNS server operate within the corresponding ISP network, commonly ISP allocate automatically.
# ISP DNS Server's feature
- **Auto allocation**: When you establish an Internet connection, most ISPs automatically assign their DNS servers in your network settings. Users will use the DNS servers of their ISPs unless they have special settings.
- **Local DNS server**: Because your ISP's DNS servers provide servers close to your location, they provide high-speed DNS lookup speeds by default, especially within your network.
- **Cache**: The DNS server of the ISP also maintains a cache for domain names, reducing lookup time for frequently requested domains.
- **Content Filtering**: Some ISPs may block certain websites or content through DNS servers, depending on the regulations or policies of a particular country. For example, if a particular site is legally blocked, access to that site may be restricted through your ISP's DNS server.
# ISP DNS Server vs Public DNS Server
- The ISP's primary DNS server is located closest to the user's Internet connection, which can be faster in terms of physical distance. It also ensures a certain level of performance thanks to the ISP's network optimization.
- [[Public DNS Server]] are global DNS servers such as Cloudflare (`1.1.1.1`) and Google (`8.8.8.8`) that can provide better performance and security. Users can change to these public DNS servers in their own network settings.

---
Reference link 🙂     
https://www.quora.com/What-are-the-differences-between-an-ISP-and-a-DNS-provider-Which-one-is-more-important-Why