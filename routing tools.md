# Routing tools

## Quagga Routing Suite
https://www.nongnu.org/quagga/
Quagga is a routing software suite, providing implementations of OSPFv2, OSPFv3, RIP v1 and v2, RIPng and BGP-4 for Unix platforms, particularly FreeBSD, Linux, Solaris and NetBSD. Quagga is a fork of GNU Zebra which was developed by Kunihiro Ishiguro.

The Quagga architecture consists of a core daemon, zebra, which acts as an abstraction layer to the underlying Unix kernel and presents the Zserv API over a Unix or TCP stream to Quagga clients. It is these Zserv clients which typically implement a routing protocol and communicate routing updates to the zebra daemon. Existing Zserv implementations are:

- kernel interface, static routes, zserv server
- RIPv1/RIPv2 for IPv4 and RIPng for IPv6
- OSPFv2 and OSPFv3
- BGPv4+ (including address family support for multicast and IPv6)
- IS-IS with support for IPv4 and IPv6

Quagga daemons are each configurable via a network accessible CLI (called a 'vty'). The CLI follows a style similar to that of other routing software. There is an additional tool included with Quagga called 'vtysh', which acts as a single cohesive front-end to all the daemons, allowing one to administer nearly all aspects of the various Quagga daemons in one place.

Please see the Documentation for further detailed information. Community support is also available via the mailling lists.
