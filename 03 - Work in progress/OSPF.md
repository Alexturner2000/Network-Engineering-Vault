# OSPF
Tags: [[Layer 3]], [[Routing Protocols]], [[link state]], [[Link-state Database]], [[link-state advertisements]], [[SPF algorithm]]

OSPF or Open Shortest Path First is a routing protocol used for networks. It uses link state routing (LSR) algorithm to choose best path. 

Open Shortest Path first uses Dijkstra's algorithm

OSPFv1 (1989) - Old and not used
OSPFv2 (1998) - IPv4
OSPFv3 (2008) - IPv6

**Broadcast** - Much like Layer 2 networks, OSPF utilizes broadcasting in the IP layer of the OSI model. For instance, hello messages can be sent in a broadcast to identify new OSPF neighbors. This however, is not always true (but mostly). 

**Non-Broadcast** - Because its not always guaranteed that OSPF will be able to use multicast packets, it may run in a non-broadcasting mode. There are two non-broadcasting modes. NBMA non-broadcast multi-access or Point to Multipoint.

There is a difference between **Adjacency and Neighboring** routers. An adjacency is when a relationship is formed between the selected neighboring routers for the purpose of exchanging routing information. Not all neighboring routers will share routing information.


There are three main steps to becoming an adjacent router
1. Become neighbors
2. Exchange LSAs
3. Calculate best route SPF

## OSPF Areas
1. **Backbone**
	The backbone is area 0, or 0.0.0.0. Like the name suggests, the backbone is the foundation area of OSPF. All other OSPF areas must be connected to the backbone. Its also worth noting that the ABR is also considered a backbone router. 
	![[Connected Backbone and Regular Areas]]
	Assuming that Area 2 is being advertised by Area 57 to the backbone, this topology works. 
2. **Regular**
	A regular area is a simple OSPF area that connects into the backbone area.
3. **Stub**
	A stub area is an area that does not receive route advertisements external to the autonomous system and routing within the area is based entirely on a default route. An ABR deletes type 4 and 5 LSAs from internal routers, sends them all a default route of 0.0.0.0 and turns itself into a default gateway. This reduces the link-state database
1. Totally Stubby
2. Not-so-stubby


## Contiguous
It is a rule of thumb to have a contiguous OSPF area topology, but what does that mean? It means to not have duplicate areas outside of the backbone area. For example:
