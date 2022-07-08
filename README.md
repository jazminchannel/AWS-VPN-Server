# AWS VPN Server
![](https://openvpn.net/wp-content/uploads/clientUI-login.png)
Competencies
-------

- Cloud Platform : AWS 
- AMI: OpenVPN Access Server - Ubuntu 
- Commands: Bash 

How To Create and Connect to a VPN server on AWS
-----------

1. Launched an OpenVPN Access server . I found this AMI with OpenVPN already installed in AWS Marketplace ![](https://openvpn.net/wp-content/uploads/vpn_server_resources/byol-ami.png)
2. Used an existing key pair I already created  
3. SSH'd into my server as root 
```bash
ssh -i "keypair.pem" root@PublicIPv4DNS 
```
4. SSH'd into my server as openvpn 
```bash
ssh -i "keypair.pem" openvpnas@PublicIPv4DNS
```
5. Changed the openvpn password 
```bash
sudo passwd openvpn 
```
6. Accessed admin page in browser 
  - Go to http://IPv4PublicIP:943/admin 
7. Logged in with openvpn username and password 
8. Went to Configuration > VPN settings. Scrolled down to routing and allowed clients to access network services on the VPN gateway IP address. 
9. Clicked save settings and update running server 
10. Went to user portal  

  - http://IPv4PublicIP:943/ 

  - Signed in using openvpn username and password 

  - Downloaded the client for my desktop 
11. Opened OpenVPN on my desktop  
12. Entered my IPv4PublicIP and connected using my openvpn credentials 
13. Connected! (Googled " What is my IP " to confirm )

