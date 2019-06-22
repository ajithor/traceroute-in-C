# traceroute-in-C
An implementation of the packet tracing tool using C

Principle-
The network layer packet has a field called Time to Live(TTL), which is decremented at every node. Whenever thiis field reaches 0, an ICMP(Internet Control Message Protocal) message is generated and sent to the original sender.
We exploit this nature, by sending out packets with incremental TTLs and recieving ICMP from each intermediate nodes, until we reach the intended reciever.
It is needed to note that those messages have the intermediate node's IP address, which we parse and filter.

To run this, compile both icmp_Listener and pktInjector.c and run icmp_Listener first.
Then run the pktInjector which will ask you to enter the destination ip address.

Should this print only one IP in the output screen, it is your default gateway's IP and that router isnt forwarding the ICMP messages to your computer.
To verify this, keep the icmpListener running and type the tracert command followed by the dest ip on a separate terminal. The listener should pick up all the intermediate IP addresses in the route.

The timing implementation seems to be totally miscalculated; someone who couldn't care less about General relativity is welcome to jump in on that.
Contact me if you want a Packet Parser code.

Feel free to play around and have fun with it.
