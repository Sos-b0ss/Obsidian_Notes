Sources:
https://www.lifewire.com/virtual-local-area-network-817357
https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/deploy/configure-virtual-local-areal-networks-for-hyper-v
\
A virtual local area network is a logical subnetwork that groups a collection of devices from different physical LANs. Large business computer networks often set up VLANs to re-partition a network for improved traffic management. Several kinds of physical networks support virtual [[LAN]]s, including Ethernet and [[Wi-Fi]].
\
[[VLAN]]s offer one way to isolate network traffic. [[VLAN]]s are configured in switches and routers that support 802.1q. If you configure multiple [[VLAN]]s and want communication to occur between them, you'll need to configure the network devices to allow that. You will need the following to configure VLANs:
-   A physical network adapter and driver that supports 802.1q VLAN tagging.
-   A physical network switch that supports 802.1q VLAN tagging.

---

#### To allow a virtual switch to use a VLAN

1.  Open Hyper-V Manager.
    
2.  From the Actions menu, click **Virtual Switch Manager**.
    
3.  Under **Virtual Switches**, select a virtual switch connected to a physical network adapter that supports VLANs.
    
4.  In the right pane, under VLAN ID, select **Enable virtual LAN identification** and then type a number for the VLAN ID.
    
    All traffic that goes through the physical network adapter connected to the virtual switch will be tagged with the VLAN ID you set.
    

#### [](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/deploy/configure-virtual-local-areal-networks-for-hyper-v#to-allow-a-virtual-machine-to-use-a-vlan)To allow a virtual machine to use a VLAN

1.  Open Hyper-V Manager.
    
2.  In the results pane, under **Virtual Machines**, select the appropriate virtual machine and then right-click **Settings**.
    
3.  Under **Hardware**, select an virtual switch that's set up with a VLAN.
    
4.  In the right pane, select **Enable virtual LAN identification**, and then type the same VLAN ID as the one you specified for the virtual switch.
    

If the virtual machine needs to use more VLANs, do one of the following:

-   Connect more virtual network adapters to appropriate virtual switches and assign the VLAN IDs. Make sure to configure the IP addresses correctly and that the traffic you want to route through the VLAN also uses the correct IP address.
    
-   Configure the virtual network adapter in trunk mode using the [Set-VMNetworkAdapterVlan](https://docs.microsoft.com/en-us/powershell/module/hyper-v/set-vmnetworkadaptervlan) cmdlet.
