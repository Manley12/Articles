## HTTP Code Cheat Sheet - What You Need to Know About HTTP Requests and Responses
If you have ever copied a link from your browser and noticed that http:// or https:// had been added before the domain, you are looking at the protocol used which defines how messages are formatted and transmitted. It also defines how web servers and browsers should respond to various commands. HTTP stands for HyperText Transfer Protocol and is used, or at least the variant HyperText Transfer Protocol Secure (HTTPS), for nearly every single website on the internet.

### HTTP Codes
All HTTP response codes can be separated into five categories. Theese are the categories:
<ul>
  <li><i>1xx informational response</i> - the request has been received and continuing process</li>
  <li><i>2xx successful</i> - the request has been received, understood, and accepted</li>
  <li><i>3xx redirection<i> - further action is needed in order to complete the request</li>
  <li><i>4xx client error<i> - the request contains bad syntax or cannot be fulfilled</li>
  <li><i>5xx server error<i> - the server failed to fulfil the apparently valid request</li>
</ul>  
    
<h4> 1xx: Information</h4>
<table>
   <tr>
     <td><b>Message</b></td>
     <td><b>Description</b></td>  
  </tr>
  <tr>
    <td>100 Continue</td>
    <td>The server has received the request headers and the client should proceed to send the request body providing that the request has been accepted.</td>
  </tr>
  <tr>
    <td>101 Switching Protocols</td>
  </tr>
</table>
  
### Unknown Yet

HTTP codes are important to understand, especially if you are developing a web application and are trying to debug based upon the console responses.
