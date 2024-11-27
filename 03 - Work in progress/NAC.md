# NAC

Tags: [[802.1x]], 

There are two different types Network Access Control (NAC). MAC auth and Cert Auth.


1. Layer 1 connectivity is formed between the device and the switch via electrical or optical
2. Layer 2, the laptop sends out frames of its MAC address, which is received by the switch
3. Layer 2, the switch triggers MAC authentication upon receiving a new mac address. The switch captures the device MAC address and sends a RADIUS request to ClearPass containing the MAC address as the username and sometimes also as the password
4. The ClearPass server receives the RADIUS request and checks the MAC address against its configured policies or database
    1. If permitted, ClearPass sends a RADIUS Access-Accept message back to the switch, possibly sending attributes like VLAN assignment
    2. If denied, ClearPass sends a RADIUS Access-Reject message
5. The switch receives the the RADIUS access status
    1. If permitted, the switch opens the port for the laptop to communicate on the network and possibly adding on addition attributes to the port
    2. If denied, the switch may disable the port, or place it in a restricted VLAN, or however its configured
6. Once Authenticated, the device will create a DHCP request

![[Drawing 2024-08-30 14.28.05.excalidraw]]