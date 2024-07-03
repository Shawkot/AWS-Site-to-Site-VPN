# AWS-site-to-site-VPN
This repo consists all the configuration steps and files related to site-to-site VPN with AWS.
In this project, I connected a private network with a VPC on AWS via VPN. For this, I configure a 
site-to-site VPN which connect two private networks and they can communicate directly via vpn tunnel.
For this connection to work, I used the following components in AWS:

1. VPC (virtual private cloud), subnet, internet gateway, routing table
2. Customer gateway, virtual private gateway and site-to-site vpn connections
3. endpoint to connect to a instance using private IP.
4. EC2 instance with specific security group.

For on-premise network, I used Vyos software based router and configure
site-site-site VPN on that router. This router sat behind a NAT device. I also needed a 
public IP for the configuration.

Finally, to test the connectivity of the vpn, I configure the following on AWS and on-prem:
- a mysql server on AWS
- an apache webserver with PHP in the private network.
- I created a simple todo app using php, put some data on mysql and the php
can pull those data from mysql server using the vpn connection.
