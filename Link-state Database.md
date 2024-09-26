# Link-State Database (LSDB)
Tags: [[link-state advertisements]], [[OSPF]], 

A link-state database (LSDB) stores all the relevant routing information for OSPF to function. Each router in the same autonomous system has an LSDB, and every router in the **same area** will have the **same LSDB**.

With the LSDB, each router uses the SPF algorithm (Dijkstra) to calculate the best route. 