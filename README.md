# WakeMeUp
Wake-On-Lan/MagicPacket android app to recievie wake up request behind NAT (from PHP server proxy)

Idea:
I was looking for a way to access my Windows-based home NAS on the network behind NAT. I have found OpenVPN it very good for accessing my device but it was required for my machinie to work all the time. I had to find better way. So I figured out I can make it sleep and wake it up on demand. I could have bought VPN client device that will do the trick (eg. Mikrotik router), but I have found old smartphone I can repurpose.

First part is script "server.php" I can start from anywhere. I have placed it on my website server. It provides the way to add wake up request. Currently your need to open link with request MAC address and IP address, but also with auth code (security). I was in hurry so I have not build client side request app. I simply put another script which will add my device to requests. Everyone can start it by opening web link.

Second part took me few more hours. It is a smiple android app that will start listener service around every minute. Service will ask server.php for request and if any will send Magic Packet to wake up my NAS. 

It works :) I have published my code so anyone can use it. Some parts are harcoded (like server address). Please change it as you see fit.

Cheers
Piotr Boryszek
