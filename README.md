# fetchphotoinsta
Fetch Photo from Instagram both hashtags and usernames

Depending on your connection speed, you can fetch 1-2k photos in 15 seconds!

!Only works on Windows platforms!

First you need to start server in your localhost on port 80 (can be editable by code), move "/test" directory into localhost main directory. Then open "keyword" and "username" files individually and edit instagram account login information according to yours -do not panic, this is not sending your data to anywhere secretly- (is really not? :)).

This will throw "cURL error 60: SSL certificate: unable to get local issuer certificate" if you do not follow these steps below:
(assuming wamp or xampp server environment)
- Download cacert.pem here;   https://curl.haxx.se/docs/caextract.html
- Put it here in the following directory (wherever your php installed on);   C:\wamp64\bin\php\php7.3.12(edit your version)\extras\ssl
- Finally, edit your php.ini file as adding this line in it;   curl.cainfo = "C:\wamp64\bin\php\php7.3.12(edit your version)\extras\ssl\cacert.pem" (Please consider your environment's path)
- Restart xampp/wamp server
(Special thanks to reference: https://stackoverflow.com/a/34883260/13236398)

Congrats! You are ready to run the program!

P.S: There is a timeout which 120 seconds for requesting via API. So after 120 secs, program might show an error then exit. 

P.S: After a lot of often requests, obviously Instagram will block your Server IP address for a while. So before it unblocked, you can change IP address or transfer files to another server. First step of block is most probably 3 days as tested.
