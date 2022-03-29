## 100-199 : Information
#### 100 : Continue
- This response indicates that everything so far is OK and the client should continue the request.
#### 101 : Switching Protocol
- This response is sent in response to an Upgrade request header from the client, and indicates the protocol the server is switching to
#### 102 : Processing
- This response indicates that the server has received and is processing the request but no response is available yet.
#### 103 : Early Hints
- This response is primarily intended to be used with the Link HTTP header, letting the user agent start preloading resources while the server prepares a response.
## 200-299 : Successes
#### 200 : OK
- The request has succeeded
#### 201 : Created
- The request has created a new resource
#### 202 : Accepted
- The request has been received but not yet acted upon
#### 203 : Non-Authoritative Information
- This response is sent when the returned information is not the same as is available from the original server.
#### 204 : No Content
- The request succeeded but there is no content to send with it
#### 205 : Reset Content
- Tells the user-agent to reset the document which sent this request
#### 206 : Partial Content
- This response is used when the Range header is sent from the client to request only part of a resource
#### 207 : Multi-Status
- This response is for when multiple status codes are appropriate
#### 208 : Already Reported
- Used inside a \<dav:propstat\> element to avoid repeatedly enumerating the internal members of multiple bindings to the same collection
#### 226 : IM Used
- This response is for when a [[HTTP Request Methods#GET]] request has succeeded and the response has been manipulated
## 300-399 : Redirects
#### 300 : Mutiple Choice
- This response is for when the request has more than one possible response and the user should choose one of them.
#### 301 : Moved Permanently
- This response is for when the URL of the requested resource has been changed permanently. The new URL is given in the response.
#### 302 : Found
- This response is for when the URL of the requested resource has been changed temporarily.
#### 303 : See Other
- This response is for when the client needs to get the requested resource at another URL with a [[HTTP Request Methods#GET]] request
#### 304 : Not Modified
- This response is used for caching purposes. It tells the client that the response has not been modified so the client can continue to use the same cached version of the response.
#### 307 : Temporary Redirect
- This response works the same as [[#302 Found]] but the HTTP request **Must Stay The Same**
#### 308 : Permanent Redirect
- This means that the resource is now permanently located at another URL specified by the Location HTTP Response Header
## 400-499 : Client Errors
#### 400 : Bad Request
- The server could not understand the request
#### 401 : Unauthorized
- This response is given if the client must authenticate themselves before the requested response can be performed
#### 403 : Forbidden
- This response is given if the client does not have access rights to the content. Unlike [[#401 Unauthorized]] the client's identity is known to the server and it does not have access rights.
#### 404 : Not Found
- This response is given when the server can not find the requested resource
#### 405 : Method Not Allowed
- This response is given when the server has disabled the request method included in the requested response.
#### 406 : Not Acceptable
- This response is sent when the web server, after content negotiation, doesn't find any content that conforms to the criteria given by the user.
#### 407 : Proxy Authentication Required
- Similar to [[#401 Unauthorized]] but a proxy must be enabled for authentication.
#### 408 : Request Timeout
- This response means that the server wants to shut down the connection
#### 409 : Conflict
- This response is sent when a request conflicts with the current state of the server
#### 410 : Gone
- This response is sent when the requested content has been deleted from the server.
#### 411 : Length Required
- This response is when the server requires a Content-Length header but it is not defined in the requested response
#### 412 : Precondition Failed
- The client has indicated preconditions in its headers which the server does not meet
#### 413 : Payload Too Large
- This response is given when the request entity is larger than the limits defined by the server
#### 414 : URI Too Long
- The Uniform Resource Identifier for getting the specific resource is too long
#### 415 : Unsupported Media Type
- The media format of the requested data is not supported by the server so the server is rejecting the request
#### 416 : Range Not Satisfiable
- The range specified by the Range header field in the request can't be fulfilled.
#### 417 : Expectation Failed
- This response is when the expectation indicated by the Expect request header field can't be met by the server
#### 418 : I'm A Teapot
- The name of this one is kind of funny but it's actually very important and not used enough. This response is for when you are requesting something from the server that would be totally valid **if it were a different type of server**. It refuses to brew coffee because it is a tea pot.
#### 421 : Misdirected Request
- This response is for when the server honestly thinks you have the wrong guy
#### 426 : Upgrade Required
- This response is for when the server refuses to perform the requested response but might be willing to do so if the client upgrades to a different protocol.
#### 428 : Precondition Required
- This response is for when the origin server requires the request to be conditional. 
#### 429 : Too Many Requests
- The user has sent too many requests in a given amount of time
#### 431 : Request Header Fields Too Large
- The server is unwilling to process the request because its header fields are too large
#### 451 : Unavailable For Legal Reasons
- The requested response can't be legally provided, typically because it isn't allowed in your region.
## 500-599 : Server Errors
#### 500 : Internal Server Error 
- The server has encountered a situation it doesn't know how to handle
#### 501 : Not Implemented
- The request method is not supported by the server
#### 502 : Bad Gateway
- This response means that the server had to act as a gateway to get a request but got an invalid response meaning it can not be relayed.
#### 503 : Service Unavailable
- The server is not ready to handle the request.
#### 504 : Gateway Timeout
- This response is given when the server is acting as a gateway and cannot get a response in time
#### 505 : HTTP Version Not Supported
- The HTTP version used in the requested response is not supported by the server
#### 506 : Variant Also Negotiates
- The server has an internal configuration error where there is no proper end point in the negotiation.
#### 507 : Insufficient Storage
- This response is for when the server does not have the storage for your request
#### 508 : Loop Detected
- The server detected an infinite loop while processing the request
#### 510 : Not Extended
- Further extensions to the request are required for the server to fulfill it
#### 511 : Network Authentication Required
- This response indicates that the client needs to authenticate to gain network access