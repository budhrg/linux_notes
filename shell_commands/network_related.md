#### Network related commands

1. To check the hostname of local machine:
`$ hostname`

2. To list all hosts inside local machine
`$ cat /etc/hosts`

3. To see DNS resolver:
`$ cat /etc/resolve.conf`

4. To check IP addresses about any host or website:
`$ host <website name>`

5.To querying Domain Name System
`$ dig <website name>`

*`dig` (domain information groper) is a network administration command-line tool for querying Domain Name System (DNS) name servers.*

6. To query domain name only
`$ nslookup <website name>`

*`nslookup` is a network administration command-line tool for querying the Domain Name System (DNS) to obtain domain name or IP address mapping or for any other specific DNS record.*

7. To see network interfaces(Connection channel between device and network)
`$ ifconfig` or `/sbin/ifconfig`

8. Network configuration file in Debian family:
`$ /etc/network/interfaces`

9. Network configuration commands:
  - To view the IP address:
    $ `/sbin/ip addr show`

  - To view the routing information:
    `$ /sbin/ip route show`

*`ip` :- show / manipulate routing, devices, policy routing and tunnels*

10. To check the status of the remote host:
`$ ping <host name>`

*`ping` is frequently used for network testing and management; however, its usage can increase network load unacceptably.*

11. `route`:
*A network requires the connection of many nodes. Data moves from source to destination by passing through a series of routers and potentially across multiple networks. Servers maintain routing tables containing the addresses of each node in the network. The IP Routing protocols enable routers to build up a forwarding table that correlates final destinations with the next hop addresses.*

To view or change the IP routing table:
`$ route`

  - Show current routing table : `$ route –n`
  - Add static route           : `$ route add -net address`
  - Delete static route        : `$ route del -net address`

12. To see the routes which the data packet takes to reach the destination:
`$ traceroute <domain>

*`traceroute` is used to inspect the route which the data packet takes to reach the destination host which makes it quite useful for troubleshooting network delays and errors. By using `traceroute` you can isolate connectivity issues between hops, which helps resolve them faster.*

13. To displays all active connections and routing tables:
`$ netstat -r`

*Useful for monitoring performance and troubleshooting.*

14. To queries network interfaces:
`$ ethtool <interface name>

*It can also set various parameters such as the speed.*

15. **FTP**: To connect to remote ftp server
`$ ftp -p <server name>`

16.

