# Prophaze_Solution

Approach to achieve the optimum solution:

After understanding the problem statement with utmost clearity, my approach towards the solution of the problem can be understood by following steps:
1. The first and foremost task was to build the logical structure or a blueprint of the solution. I needed a serevr, a client and a live connection between    them. Along with this, the server needs to have same decoding capabilities and revert back the response.
2. There was a need of a live connection between a server and a client. Hence, my first actual step was to implement the server code and the client and        establish a live connection between them. 
3. After this the post request connection was established by using the do_POST() function on the server side and the post() function from the request          library on the client side.
4. Once the post request was being recieved along with the encrypted payload, I started implementing the logic to decode the payload sent by the client on    the server side. 
5. Steps in the decoding logic:
      a. The payload was coming in bytes, hence I first encoded it in string and I got a string of the encrypted payload.
      b. Then the extra spaces and '0x' were removed from the string. 
      c. Now the string was decoded from hex to ASCII using the fromhex().decode() from the bytearray. This results in a string having space separated              ASCII values. 
      d. Now the ASCII values are separated and stores in a list and converted in character and joined in a string. 
      e. This string is still encdoded in base64 and hence the string is decoded using the b64decode() function from base64 library. 
6. The resultant decode string is produced by the server to the client via a valid response. 
