## What is Load Balancing

Modern internet infastructure requires mutliple computers in order to serve a website or internet application reliably around the globe. But each of these computers have a different external IP addresses. While this would not be a problem if all of the computer hosted a different application, DNS (Domain Name Server) and mobile applications rely on a single IP to connect to.

### What Does a Load Balancer Do?
According to [NGINX](https://www.ngnix.com/resources/glossary/load-balancing/), "a load balancer acts as the "traffic cop" sitting in front of your servers and routing client request across all servers capable of fulfilling those requests in a manner that maximizes speed and capacity utilizatiojnand ensures that no one server is overworked, which could degrade performance."

!()[https://critix.com/content/dam/citrix61/en_us/images/graphics/infographics/load-balancing-illusation-critix.png]

Since modern web application could serve hundreds of thousands of concurrent requests. These applications must return the correct and desired information to the client. By adding more than one server to serve this information, a load balancer is placed into function. [NGINX](https://www.ngnix.com/resources/glossary/load-balancing/) says that the main functions of a load balancer are:

<ul>
  <li>Distribute client requests or network load efficiently across multiple server</li>
  <li>Ensures high availability and reliability by sending requests only to server that are online</li>
  <li>Provides the flexibility to add or subtract servers as demand dictates</li>
</ul>
