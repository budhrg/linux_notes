#### Network related commands

1. To check the hostname of local machine: <br>
`$ hostname`

2. To list all hosts inside local machine <br>
`$ cat /etc/hosts`

3. To see DNS resolver: <br>
`$ cat /etc/resolve.conf`

4. To check IP addresses about any host or website: <br>
`$ host <website name>`

5. To querying Domain Name System<br>
`$ dig <website name>`
<br>*`dig` (domain information groper) is a network administration command-line tool for querying Domain Name System (DNS) name servers.*

6. To query domain name only <br>
`$ nslookup <website name>`
<br>*`nslookup` is a network administration command-line tool for querying the Domain Name System (DNS) to obtain domain name or IP address mapping or for any other specific DNS record.*

7. To see network interfaces(Connection channel between device and network) <br>
`$ ifconfig` or `/sbin/ifconfig`

8. Network configuration file in Debian family: <br>
`$ /etc/network/interfaces`

9. Network configuration commands: <br>
  - To view the IP address: <br>
    $ `/sbin/ip addr show`

  - To view the routing information: <br>
    `$ /sbin/ip route show`
<br>*`ip` :- show / manipulate routing, devices, policy routing and tunnels*

10. To check the status of the remote host: <br>
`$ ping <host name>`
<br>*`ping` is frequently used for network testing and management; however, its usage can increase network load unacceptably.*

11. `route`: <br>
*A network requires the connection of many nodes. Data moves from source to destination by passing through a series of routers and potentially across multiple networks. Servers maintain routing tables containing the addresses of each node in the network. The IP Routing protocols enable routers to build up a forwarding table that correlates final destinations with the next hop addresses.*
<br>To view or change the IP routing table: <br>
`$ route`
  - Show current routing table : `$ route –n`
  - Add static route           : `$ route add -net address`
  - Delete static route        : `$ route del -net address`

12. To see the routes which the data packet takes to reach the destination: <br>
`$ traceroute <domain>`
<br> *`traceroute` is used to inspect the route which the data packet takes to reach the destination host which makes it quite useful for troubleshooting network delays and errors. By using `traceroute` you can isolate connectivity issues between hops, which helps resolve them faster.*

13. To displays all active connections and routing tables:<br>
`$ netstat -r`
<br>*Useful for monitoring performance and troubleshooting.*

14. To queries network interfaces: <br>
`$ ethtool <interface name>`
<br>*It can also set various parameters such as the speed.*

15. **FTP**: To connect to remote ftp server <br>
`$ ftp -p <server name>`
