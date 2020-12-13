# JWT_Authorization

Web based authorization standard , Not for Authentication 
Microservice  
Security 


- Normal mechanism where user request , Session ID generated at Server side and Server send back Session ID as Cookie and subsequent call pass the cookie (Browser will do that ) and server identify user 
- Sticky session pattern where load balancer remember the server where the user session is there
-  JWT – Signed the request and send the same token in sub sequent call 


![](/screenshots/GetImage.png)
- Middle portion Payload is Base 64 encoded 
- Header tells how it is signed ( basically algorithm ) --> Header is in base 64 we can see ( just for convenance 
- Signature – You can see SHA256 which is same in header.. Also you can see secrete key which is just server has. Basically, it will take base64Encode(header)+.+base64Encode(payload) and signed it using SHA256 algorithm and secret key and this is third value.. End user change anything and server can't decrypt it then request will fail 

 

