# COMPUTER NETWORKS
Department Network

# DEVICES USED:
•	60 Generic Computers
•	12 Switches (2960)
•	4 Routers (2911)
•	2 Generic Servers

# STRUCTURE:
The network topology consists of three departments (cyber security, artificial intelligence, and computer science). Each department consists of a Lab, Faculty Office, and Classrooms. The Labs actually have more than 20 computers but as this project is a model of the actual network so I have used only six computers per lab, similarly faculty offices consist of eight computers and each department has six classrooms. Labs have two switches, the Faculty office has one, and the six classes are connected with a single switch. 

![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/be82c0ca-e1cb-4b1a-b91f-4a3183d04606)

# PROCEDURE:
First, add PCs to the topology and connect them with their respective switches. After performing this function, connect the switches with their respective routers. Now enter the CLI of the router and write the following set of commands to turn the DHCP in the PCs connected with the routers. Add the Respective IP range, subnet mask, default gateways, and respective DNS server IP. Now after writing the commands in the CLI of the routers, enter PC now go to Desktop > IP configuration and from here turn the DHP on. After this, you will observe that the IP is assigned to the computer from the given range, and the subnets and other blanks are assigned their values.

![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/6fb6bde7-8771-44f1-b5cb-e284d756d037)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/ba37bb50-9840-4621-9f33-473ef60d2e9c)

Now set the servers. Firstly, assign the IPs, subnet masks, default gateways, and DNS server IP in the server configuration menu.

# DNS SERVER:
To configure the DNS server perform the following steps.
After assigning the IP address etc. go into the Services > DNS and turn the DNS option on. Now add the name of the server in the Name tab and IP in the IP Address tab. In addition, press the Add below. You can add the IPs of the computers in this tab if you want to. Now to access the server open PC > Desktop > Web Browser and enter the IP or the name of the server after this a message WEB ACCESSED SUCCESSFULLY will be displayed. You can ping the server from the PC > CMD by using the server’s name or IP address.

![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/c384d1d0-1950-4d48-a2ce-7cf871749441)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/e907ea51-333f-46a4-9616-6f7736502b40)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/161800d4-7746-4a42-8f38-d795da6b2fe5)

# EMAIL SERVER:
After assigning the IP address etc. go into the Services > EMAIL and turn the SMTP & POP options on. Now add a domain in the Domain section e.g. mail.com or Gmail.com. Now add user names and passwords in the username and password sections and press the + button below. Now add the domain name to your DNS server section and then go to the CMD of a PC and type the domain name or the IP of the server to ping the server.

![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/3544d1d0-9831-4440-9fee-15935504c004)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/8b9ad1f4-c2d0-4801-9275-072bbc91c286)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/bf8921ed-35ee-451c-8bf6-30912c800b7b)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/a6c1244b-15f2-4113-8608-a3427443cda5)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/880cff96-3c04-4c23-b2cf-7fa8f061379c)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/c25a6c80-05db-454b-a14e-8c01a6846d7c)


# ROUTING:
Firstly, add serial ports from the Physical section in the routers. Now use the Serial DCE Wire to connect the routers with each other as shown in the figure below. Now assign the IPs to the serial ports and click on the checkbox at the top right corner of the menu. Similarly, repeat the same process for the rest of the ports in each router now go to the RIP section and add the addresses for the networks in the departments and the IPs of the routes as shown in the figure below.

![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/5e26d97a-5b44-4c50-ae20-ea82ec71de39)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/849b18c0-68ce-432c-8cde-ba5d296638aa)
![image](https://github.com/iabdullah215/Computer-Networks/assets/121729444/00f8e001-c10d-48d0-a4b9-1ebdb886ddad)

# SUBNETTING:
The given IP addresses, 193.168.1.0, 193.168.2.0, 193.168.3.0, and 193.168.4.0 can be divided into four subnets, each accommodating up to 64 IP addresses using a subnet mask of 255.255.255.192 or /26 in CIDR notation. The /26 mask provides 2^6 or 64 possible host addresses per subnet, leaving 2 addresses reserved for the network address and broadcast address. The subnet ranges and their assignable IP addresses are as follows: the first subnet is 193.168.1.0 to 193.168.1.63, with assignable IP addresses ranging from 193.168.1.1 to 193.168.1.62. The second subnet range is 193.168.1.64 to 193.168.1.128, with assignable IP addresses ranging from 193.168.1.65 to 193.168.1.126. Similarly, the third and fourth subnet ranges are 193.168.1.128 to 193.168.1.191 and 193.168.1.192 to 193.168.1.255, respectively. By dividing these IP addresses into subnets, network administrators can manage and allocate IP addresses more efficiently, allowing for better utilization of available IP address space.

# CALCULATIONS:
IPs used: 193.168.1.0, 193.168.2.0, 193.168.3.0 and 193.168.4.0<br>2^2 = 4 (Number of networks)<br>2^6 = 26 (Number of hosts)<br>64-2 = 64 (IP that can be assigned)<br>Subnet mask = 255.255.255.192 /26<br>Binary = 11111111.11111111.11111111.11000000

# TABLE:

| Range                        | Assignable IPs               |
|------------------------------|------------------------------|
| (1,2,3,4).0 – (1,2,3,4).63   | (1,2,3,4).1 –(1,2,3,4).62    |
| (1,2,3,4).64 –(1,2,3,4).127  | (1,2,3,4).65 –(1,2,3,4).126  |
| (1,2,3,4).128 –(1,2,3,4).191 | (1,2,3,4).129 –(1,2,3,4).190 |
| (1,2,3,4).192 –(1,2,3,4).255 | (1,2,3,4).193 –(1,2,3,4).254 |


