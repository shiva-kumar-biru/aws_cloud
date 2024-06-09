# Security Group

## Introduction

- They control how traffic is allowed into or out of the EC2 instance.
- Security groups only contains allow rules
- Security groups rules can reference by IP or by security group
- Security groups are acting as a "Firewall" on EC2 instance

They regulate

- Access to ports

- Authorized IP ranges
  
- Control In and Outbound


## Classic Ports to know

# Common Classic Ports

| Port Number | Protocol | Description                             |
|-------------|----------|-----------------------------------------|
| 20          | TCP      | FTP Data Transfer                       |
| 21          | TCP      | FTP Command Control                     |
| 22          | TCP/UDP  | SSH Remote Login Protocol               |
| 23          | TCP      | Telnet Protocol                         |
| 25          | TCP      | SMTP (Simple Mail Transfer Protocol)    |
| 53          | TCP/UDP  | DNS (Domain Name System)                |
| 80          | TCP      | HTTP (Hypertext Transfer Protocol)      |
| 110         | TCP      | POP3 (Post Office Protocol)             |
| 123         | UDP      | NTP (Network Time Protocol)             |
| 143         | TCP      | IMAP (Internet Message Access Protocol) |
| 443         | TCP      | HTTPS (HTTP Secure)                     |
| 993         | TCP      | IMAPS (IMAP Secure)                     |
| 995         | TCP      | POP3S (POP3 Secure)                     |
| 3389        | TCP      | RDP (Remote Desktop Protocol)           |
| 5432        | TCP      | PostgreSQL Database                     |
| 5900        | TCP      | VNC (Virtual Network Computing)         |
| 6379        | TCP      | Redis Database                          |
| 8080        | TCP      | HTTP Alternate                          |
| 3306        | TCP      | MySQL Database                          |
| 1521        | TCP      | Oracle Database                         |
| 27017       | TCP      | MongoDB                                 |


## steps to create a Security Group and attaching to EC2 instance.

[Create a Security Group](https://github.com/shiva-kumar-biru/aws_cloud/blob/main/projects/ec2-instance-management/create_security_group.md)
