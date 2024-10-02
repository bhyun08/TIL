Web Browser is a software application that navigates and displays web pages or web applications on a computer or mobile device connected to the Internet. When user input Address of a particular website(URL) or search term, web browser show that get the appropriate web page and show it on the screen.

![](https://i.namu.wiki/i/uLQ5Be6XnAkVybdgVOwJOUMk5puRpn17MLJCO_Cu4-l-NdPJdglc2wc-eJs5LKK3LPR9Y-aoptxuCVH_yBW3XD0xi48qcbWM3xrwagjVZI404YAUyfzmduFgBBZCatLdGu5oVtpicox_oFrDFryNBw.webp)     
This is picture that draw simply web browser's role. 

# What does a web browser do?
Actually, web browser support many features to browse web.
- Web technology interpretation: Web browser can interpret web technology like **HTML, CSS, JavaScript,** etc.
- Network communication: Web browsers communicate with web servers using **HTTP** or **HTTPS** protocols.
- Request and Response: Aforementioned features all are work **Request and Response**.
# Web browser's kind
There are so many different kinds of web browsers. Each browser has its pros and cons, and the uses used are slightly different. Representative web browsers include safari, chrome, firefox, opera, and edge.
# Web browser's workflow
https://www.youtube.com/watch?v=FQHNg9gCWpg
![](https://www.engineersgarage.com/wp-content/uploads/2019/07/Simple-Block-Diagram-Showing-Working-of-Web-Browser.gif)
1. **User input**: When a user enters a website address(URL) or a search term in the search box, the browser prepares to process this request.
2. **DNS inquiry**: To convert the domain name entered in the URL(ex: www.curry.com) to an IP address, the browser first requests the DNS server to inquiry. The DNS server returns the appropriate IP address for that domain.
3. **Connect Server**: The browser that receives the IP address establishes a connection with the web server. If you use the TCP/IP protocol in this process and the website supports HTTPS, SSL/TLS encryption applies. In this step, **3-way-handshake** work.
4. **HTTP Request**: Browser send http(s) request to server 
5. **HTTP Response**: Server send http(s) response to browser. Send files such as HTML, CSS, JavaScript, and images to your browser in response to your request.
6. **Rendering**: Browser interprets HTML, CSS, and JavaScript files received from the server and draws web pages onto the screen. HTML is the structure of web pages, CSS is the style, and JavaScript is the dynamic feature.
	1. **Create Document Object Model(DOM)**: Create a DOM tree by parsing HTML documents. The DOM represents the structure and content of a web page, which allows JavaScript to access the tree and make dynamic changes to the page.
	2. **Create a CSSOM(CSS Object Model)**: Create a CSSOM tree by parsing the CSS file, which defines the style of a web page.
	3. **Create a AST(Abstract Syntax Tree)**: During the browser's rendering process, AST (Abstract Syntax Tree) is mainly generated when parsing JavaScript code.
	4. **Create a render tree**: Combine DOM and CSSOM to create a render tree. This render tree contains what the browser needs to draw on the screen and the style.
7. **User interaction**: Users can interact (click, type, etc.) even after the page is rendered, and JavaScript processes this behavior to dynamically update the web page.

---
Reference link 🙂     
https://namu.wiki/w/%EC%9B%B9%20%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80       
https://www.mozilla.org/en-US/firefox/browsers/what-is-a-browser/       
https://www.engineersgarage.com/web-browsers-what-is-web-browser/