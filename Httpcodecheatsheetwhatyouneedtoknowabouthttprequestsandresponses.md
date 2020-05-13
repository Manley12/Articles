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
    <td>The requester has asked to switch protocols and the server has agreed.</td>
  </tr>
</table>

<h4> 2xx: Success </h4>
<table>
  <tr>
    <td>200 OK</td>
    <td>This is the standard response for successful HTTP requests. Code 200 means everything is okay.</td>
  </tr>
  <tr>
    <td>201 Created</td>
    <td>The fulfilled request resulted in the creation of a new resource.</td>
  </tr>
  <tr>
    <td>202 Accepted</td>
    <td>The request has been accepted for processing, but has not completed processing</td>
  </tr>
  <tr>
    <td>203 Non-Authoritative Information</td>
    <td>The information contained in the entity header is from a local or third-party copy, not from the original.</td>
  </tr>
  <tr>
    <td>204 No Content</td>
    <td>The server sucessfully processed the request, but is not returning any content</td>
  </tr>
  <tr>
    <td>205 Reset Content</td>
    <td>The requester should clear the form used for the transaction</td>
  </tr>
  <tr>
    <td>206 Partial Content</td>
    <td>The server is only delivering part of the resource due to a range header that was sent by the client. This range header is used by HTTP clients to enable resuming interrupted downloads or split downloads in multiple simultaneous streams.</td>
  </tr>
</table>
  
<h4>3xx Redirection</h4>
<table>
  <tr>
    <td>300 Multiple Choices</td>
    <td>A list of links, from which the requester can select one and go to it. For example, this code could be used to present multiple video formats.</td>
  </tr>
  <tr>
    <td>301 Moved Permanently</td>
    <td>The requested page has moved to a new URL</td>
  </tr>
</table>  
  
### Unknown Yet

HTTP codes are important to understand, especially if you are developing a web application and are trying to debug based upon the console responses.
