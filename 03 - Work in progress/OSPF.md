# OSPF
Tags: [[Layer 3]], [[Routing Protocols]], [[link state routing]]
OSPF or Open Shortest Path First is a routing protocol used for networks. It uses link state routing (LSR) algorithm to choose best path. 

[[link-state advertisements]]

**Broadcasting** - Much like Layer 2 networks, OSPF and other routing protocols utilize broadcasting in the IP layer of the OSI model. For instance, hello messages can be sent in a broadcast to identify new ospf neighbors. This however, is not always true (but mostly). 


## OSPF Areas
1. **Backbone**
	The backbone is area 0, or 0.0.0.0. Like the name suggests, the backbone is the foundation area of OSPF. All other OSPF areas must be connected to the backbone, however, that does not mean they need to be directly connected. For instance: 
	![[09 - Misc/Images/Excalidraw/Drawing 2024-09-25 12.54.49.excalidraw]]
	Assuming that Area 2 is being advertised by Area 57 to the backbone, this topology works. 
2. **Regular**
	A regular area is a simple OSPF area that connects into the backbone area.
3. **Stub**
	A stub area is an area that does not receive route advertisements external to the autonomous system and routing within the area is based entirely on a default route. An ABR deletes type 4 and 5 LSAs from internal routers, sends them all a default route of 0.0.0.0 and turns itself into a default gateway. This reduces the link-state database
1. Totally Stubby
2. Not-so-stubby
