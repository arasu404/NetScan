# NetScan
Beginner-friendly Python network scanner for local host discovery

# What you need to learn ?
> What is Address Resolution Protocol (ARP)?
> 
>> *The acronym ARP stands for **Address Resolution Protocol** which is one of the most important protocols of the Data link layer in the ![OSA Model](https://www.geeksforgeeks.org/computer-networks/open-systems-interconnection-model-osi/). It is responsible to find the hardware address of a host from a known IP address.There are three basic ARP terms.*

**Note**: ARP finds the hardware address, also known as the Media Access Control (MAC) address, of a host from its known IP address. 

   <img style="float: right;" src="https://media.geeksforgeeks.org/wp-content/uploads/20230418131043/arpp.jpg"> 

 ## How ARP works ?
 
 imagine a device that wants to communicate with others over the internet. What does ARP do? It broadcast a packet to all the devices of the source network. The devices of the network peel the header of the data link layer from the Protocol Data Unit (PDU) called frame and transfer the packet to the network layer (layer 3 of OSI) where the network ID of the packet is validated with the destination IP's network ID of the packet and if it's equal then it responds to the source with the MAC address of the destination, else the packet reaches the gateway of the network and broadcasts packet to the devices it is connected with and validates their network ID. The above process continues till the second last network device in the path reaches the destination where it gets validated and ARP, in turn, responds with the destination MAC address.

 ![arp](https://media.geeksforgeeks.org/wp-content/uploads/20240212121108/How-Address-Resolution-Protocol-ARP-works---gif-opt-(1).gif#centre)
