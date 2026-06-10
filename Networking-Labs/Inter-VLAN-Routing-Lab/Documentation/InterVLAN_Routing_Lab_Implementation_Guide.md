\# Inter-VLAN Routing Lab Implementation Guide



\## My Thoughts and Research



As I worked through this lab, I wanted to understand more than just the commands required to make the network function. I wanted to understand why the network behaved the way it did before and after routing was introduced.



One of the first things that became clear was the purpose of VLANs. VLANs allow organizations to logically divide a single physical network into multiple isolated segments. Instead of placing every device into one large broadcast domain, network administrators can separate users, departments, or resources into their own logical networks. This improves security, reduces unnecessary broadcast traffic, and makes the network easier to manage as it grows.



The next concept I wanted to understand was why devices in different VLANs could not communicate with one another. Before configuring Router-on-a-Stick, I intentionally tested communication between VLAN 20 and VLAN 30. The failed pings were not evidence that something was broken. In fact, they demonstrated that the segmentation was working correctly. The VLANs had effectively created separate silos within the same physical network.



This led me to the role of the router. A switch operates primarily at Layer 2 and uses MAC addresses to move traffic within a local network. A router operates at Layer 3 and uses IP addresses to move traffic between networks. Because VLAN 20 and VLAN 30 existed as separate logical networks, a Layer 3 device was required to move traffic between them. In this lab, the router became the bridge that allowed communication between those isolated segments.



One of the more interesting concepts I encountered was Router-on-a-Stick (ROAS). Rather than dedicating a physical router interface to each VLAN, a single interface was divided into multiple logical subinterfaces. Each subinterface represented a different VLAN and served as the default gateway for that network. This approach is efficient because multiple VLANs can share a single physical connection to the router.



Understanding trunking and 802.1Q tagging was equally important. Before this lab, I understood that a trunk allowed multiple VLANs to cross a single link, but I did not fully appreciate how that happened. The trunk uses 802.1Q tagging to add VLAN information to Ethernet frames. This tagging allows the switch and router to identify which VLAN traffic belongs to as it travels across the shared connection.



I also spent time thinking about IP addressing and gateway assignments. Each VLAN requires its own subnet because VLANs represent separate broadcast domains. Assigning different subnets allows the router to make routing decisions between those networks. Each VLAN therefore requires its own default gateway so devices know where to send traffic that is destined for another network.



The traffic flow itself became easier to visualize after completing the lab. Traffic begins at a workstation and is forwarded by the switch. If the destination exists within the same VLAN, the switch can deliver the traffic directly using Layer 2 switching. If the destination resides in another VLAN, the traffic must be sent to the default gateway. The router then evaluates the destination network and forwards the packet to the appropriate VLAN before sending it back through the switch.



From a troubleshooting perspective, this lab reinforced how many different points of failure can exist within a network. A missing trunk configuration, an incorrect VLAN assignment, an incorrect gateway, missing encapsulation, or a disabled router interface can all prevent communication. Working through these possibilities helped me better understand how network engineers isolate and resolve connectivity problems.



I also spent time considering the security implications of Inter-VLAN Routing. Segmentation is one of the most effective ways to limit unnecessary communication and reduce the potential impact of a compromise. However, once routing is introduced, communication pathways are created between those isolated segments. This is why organizations often implement access control lists (ACLs), firewalls, and segmentation policies to control exactly which systems are allowed to communicate.



One of the biggest lessons from this lab was understanding the balance between connectivity and security. Businesses need departments and systems to communicate, but they also need boundaries to protect sensitive resources. Inter-VLAN Routing provides that balance when it is properly designed and secured.



Overall, this lab helped me connect several networking concepts that are often studied separately. VLANs, trunking, routing, gateways, IP addressing, segmentation, and security all came together in a single environment. Rather than simply learning how to configure Router-on-a-Stick, I gained a better understanding of why organizations use it and how it fits into real-world network design.



