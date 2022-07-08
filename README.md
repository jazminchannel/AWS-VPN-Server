# AWS VPN Server

Competencies
-------

- Cloud Platform : AWS 
- AMI: OpenVPN Access Server - Ubuntu 
- Commands: Bash 

How To Create and Connect to a VPN server on AWS
-----------

1. Launched an OpenVPN Access server . I found this AMI with OpenVPN already installed in AWS Marketplace 
2. Used an existing key pair I already created  
3. SSH'd into my server as root 
```bash
ssh -i "keypair.pem" root@PublicIPv4DNS 
```
4. SSH'd into my server as openvpnas 
```bash
ssh -i "keypair.pem" openvpnas@PublicIPv4DNS
```
5. Changed the password  
```bash
sudo passwd openvpn 
```
6. Accessed admin page in browser 
  - Go to http://IPv4PublicIP:943/admin 

7. Logged in with openvpn username and password 

