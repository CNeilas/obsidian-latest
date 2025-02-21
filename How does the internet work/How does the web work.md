Imagine that the Internet is like a road. On one end there is a client(you), on the other end is a web server where you want to get the data from. To get data back and forth you need:

1. An internet connection.
2. TCP/IP: Transmission Control Protocol and Internet Protocol. They are communication protocols that define how data travels across the Internet.
3. DNS: Domain Name System. It's like an address book for websites. To find the web server's IP address the browser looks at DNS.
4. HTTP: Hypertext Transfer Protocol(HTTP) is an application protocol that defines the language the client and server use to communicate.
5. Files: Websites are made of many files of code, assets.
## How it all happens

1. Browser goes to the DNS and finds the address.
2. Browser sends an HTTP request asking to send a copy of the website to the user. To send data back and forth TCP/IP is used.
3. When server approves the request it sends the client "200 OK" message which means that you can access the data. The data is then sent to you as a series of small packets of data.
4. The browser assembles the data into a web page and displays it to you.

5. ![[How_DNS_works.png]]
