# General

[Cloud Customer Care Services](https://cloud.google.com/support)

Cloud Customer Care offers the following support services:

-   Basic Support
-   Standard Support
-   Enhanced Support
-   Premium Support

**standard** = **4hr**

**enhanced** = **1hr**

**premium** = **15min+TAM(Technical Account Manager)**

(Enhanced Support offers P1 - 1 hour Initial response time while Standard offers P2 - 4hr & Premium offers P1 - 15mins Initial Response time)

---

[NETWORK SERVICE TIERS](https://cloud.google.com/network-tiers?hl=en)

\***\*Premium\*\***

> Give users exceptional **high performing network** experience by using Google’s global network.

\***\*Standard\*\***

> Get **control over network costs**, while still delivering performance comparable with other cloud providers.

| Category             | Premium                                                                                                | Standard                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| **Network**          | High performance routing                                                                               | Lower performance network                                                                     |
| **Network Services** | Network services such as Cloud Load Balancing are global (single VIP for backends in multiple regions) | Network services such as Cloud Load Balancing are regional (one VIP per region)               |
| **Service Level**    | High performance and reliability                                                                       | Performance and availability comparable to other public cloud providers (lower than premium)  |
| **Use Case**         | Performance, reliability, global footprint and user experience are your main considerations            | **Cost is your main consideration**, and you’re willing to trade-off some network performance |

---

[Resource hierarchy](https://cloud.google.com/resource-manager/docs/cloud-platform-resource-hierarchy)

-   Create a **folder per department**, and create a **project per environment** in each folder.
-   no concept of creating project for each region
-   billing accounts can only be set at the Organization level or the Project level, not the folder level. [Reference](https://stackoverflow.com/questions/69421432/gcp-can-billing-be-configured-at-the-folder-level) [Reference](https://cloud.google.com/billing/docs/concepts)

> environments: development, testing, and production

![](https://cloud.google.com/resource-manager/img/cloud-hierarchy.svg)

---

[Dataset Access Controls](https://cloud.google.com/bigquery/docs/dataset-access-controls#granting_access_to_a_dataset)

The Compute Engine **service account** should be included in the **IAM Policy** on the **BigQuery dataset** to allow a production job **running on a Compute Engine instance** that is part of an instance group to have **access to a BigQuery dataset**.

-   When an identity calls a Google Cloud API, BigQuery requires that the identity has the appropriate permissions to use the resource. You can grant permissions by granting roles to a user, a group, or a **service account**.
-   MIGs(Manages Instance Groups) uses the **Compute Engine default service account** for its own operation

---

[VPC Network Peering](https://cloud.google.com/vpc/docs/vpc-peering)

VPC Network Peering gives you several advantages over using external IP addresses or VPNs to connect networks, including:

-   Network Latency: Connectivity that uses only internal addresses **provides lower latency** than connectivity that uses external addresses.
-   Network **Security**: Service owners do not need to have their services exposed to the public Internet and deal with its associated risks.
-   Network Cost: Google Cloud charges [egress bandwidth pricing](https://cloud.google.com/vpc/network-pricing#internet_egress) for networks using external IPs to communicate even if the traffic is within the same zone. If however, the networks are peered they can use internal IPs to communicate and save on those egress costs. [Regular network pricing](https://cloud.google.com/vpc/network-pricing) still applies to all traffic.
