# traceroute-in-C
An implementation of the packet tracing tool using C

To run this, compile both icmp_Listener and pktInjector.c and run icmp_Listener first.
Then run the pktInjector which will ask you to enter the destination ip address.

Should this print only one IP in the output screen, it is your default gateway's IP and that router isnt forwarding the ICMP messages to your computer.
To verify this, keep the icmpListener running and type the tracert command followed by the dest ip on a separate terminal. The listener should pick up all the intermediate IP addresses in the route.

The timing implementation seems to be totally miscalculated; someone who couldn't care less about General relativity is welcome to jump in on that.
Contact me if you want a Packet Parser code.

Feel free to play around and have fun with it.
