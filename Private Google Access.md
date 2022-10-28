[Private Google Access](https://cloud.google.com/vpc/docs/configure-private-google-access)

# Main Points

(**Cloud NAT** helps Compute Engine VM which lacks an external IP address to have connection to **internet** whereas **Private Google Access** **doesn't** go through public **internet**)

-   allow Compute Engine VM which lacks an external IP address to connect to the set of external IP addresses used by [Google APIs and services](https://developers.google.com/apis-explorer/) by enabling Private Google Access on the subnet used by the VM's network interface.
-   Private Google Access for on-premises hosts provides a way for **on-premises** systems to **connect** to [Google APIs and services](https://developers.google.com/apis-explorer/) by routing traffic through a [**Cloud VPN**](https://cloud.google.com/network-connectivity/docs/vpn) tunnel or a [**Cloud Interconnect**](https://cloud.google.com/network-connectivity/docs/interconnect) attachment (VLAN). Private Google Access for on-premises hosts is an alternative to connecting to Google APIs and services over the internet.

---
