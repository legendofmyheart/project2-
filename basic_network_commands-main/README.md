# basic_network_commands

1 - IPCONFIG

-- IPCONFIG command is used to display the IPv4, IPv6, subnet mask, default Gateway of all the network adapters in the system.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/d30fead8-85bc-4be7-941a-4b2cf59e4f94)

IPCONFIG Command be used with the following Parameters:-

 I - IPCONFIG /all -- This command also works similar like IPCONFIG, Additioanlly it provide extra details like DNS Server Address, DHCP Server Address, IP's Lease Period.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/63baab82-90c2-4aa8-ab45-b5a027a5261c)

II - IPCONFIG /release -- This command is used to release the current IP Information for a specified network Adapter. This command is used before renewing IP Address from DHCP Server
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/489f8496-874e-4119-a0c2-603772db1cf1)
 
III - IPCONFIG /renew -- This command is used to renew the IP Information that is released using the above II command.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/91d210a7-a52a-460b-92bd-d71fcf05110c)

IV - IPCONFIG /displaydns -- This command is used to display the DNS Information of the wessite that is stored in the DNS Resolver Cache.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/8452998a-938d-4805-b750-0653432a8ab5)

V - IPCONFIG /flushdns -- This command is used to clear or fulsh the DNS Information of the Website that is Stored in the DNS Resolver Cache.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/07a0e72a-e57c-40d4-a6da-86d4f4b38a8a)

VI - IPCONFIG /registerdns -- This command manually registers DNS Record for the specific Network Adapter.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/86c98d50-64fe-4d44-9ac3-06c427667ce7)


2 - PING 
-- PING Command is used to test the reachability of the Host in the IP Network by sending the ICMP Packets.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/294134ac-6357-452f-8c70-9c86f9d444f2)

PING Command can be used with the following parameters:-
I - ping -n 5 www.twitter.com  This command is used to test the reachability of the twitter website and adding a flag of -n 5 specifies the count of ICMP Packet need to be sent.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/c0ce54a3-12d8-48f7-bd21-d1de65dfafae)

II - ping -w 3000 www.twitter.com This command also serves the same purpose of PING I Command, additionally we are adding a flag -w 3000 which specifies the timeout of the packet to drop if it does'nt received reply from the host after the specified time. The Default Value is 1000 millisecond (ie) 1 second
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/42af5f22-854b-4965-97ff-3ffdb2b664ed)
 
III - ping -l 64 www.twitter.com This command also serves same purpose as PING I Command, additionally we are adding a flag -l 64 which specifies the size of the ICMP Packets in Bytes. The Default Packet size is 32 Bytes.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/8f9d61bf-9d06-4fea-88ec-c162f6b4fd80)

IV - ping -f www.twitter.com This Command also serves the same purpose as PING I Command, additionally we are adding a flag -f which means DO NOT FRAGMENT, Usually in ping command fragmentation is enabled which means breaking the packets into smaller fragments to prevent data loss in transmit. The Purpose of providing DO NOT FRAGMENT is to check the Maximum Packet size required for transmission.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/19f6e034-ea85-40d9-a68f-97cc2d5596b6)


3 - TRACERT 
-- Tracert Command is used to display the routing path that the packet transmitted from source to destination, How much devices it traversed during transmission, Number of Hops it has taken all the details can be shown.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/cbc5a833-5a1d-44b9-aa91-0e698c7d3427)

4 - NSLOOKUP
-- NSLOOKUP Simply means retriving Domain name information regarding the specified dns address from the DNS Server. We can also perform reverse dns search by inputting the IP address of the domain and display the details about its Domain Name.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/b96f39f4-098d-41be-b8dc-e9c64108c712)

NSLOOKUP Command can be used with the Following Arguments:- 

I - nslookup -type=soa www.twitter.com This Command retrieve information regarding the Specified Domain Name, Additionally we are providing the flag -type=soa which provides authoritative response like displaying primary server name and other details of the specified domain.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/e766a9c1-9967-4cd9-a9c9-078f10f1b1e7)


5 - NETSTAT 
-- NETSTAT Command abbrevation is Network Statistics, that is used to display all active TCP Connection, Ports on which computer is listening, Ethernet Statistics, IPv4 Statistics, IPv6 Statistics. Without providing any flags netstat command will print all the TCP Connection.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/f7e417f4-2bcf-4464-a148-fc18b097b6cb)

NETSTAT Command can be used with the following Arguments:-
I - netstat -a This command will print all the TCP Connections, all the ports in TCP, UDP is listening.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/631ada4a-5f48-4d8d-9b42-5c44479c7175)

II - netstat -e This command will print the network statistics details that includes number of bytes and packets sent and received.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/7259717d-da65-40fe-a4de-c9e36032c6a3)

III - netstat -o This Command will print TCP Connection with the Process ID(PID).In Task Manager->Processes we can find the Application based on the PID.
![image](https://github.com/giridharan-6701/basic_network_commands/assets/94190302/60ffcfc8-dea4-428a-8da5-044272145f38)

IV - netstat - r This command will print the routing table 



6 - ARP 
--ARP Stands for Address Resolution Protocol, That is used to map the IP Address with its respective MAC Address.







