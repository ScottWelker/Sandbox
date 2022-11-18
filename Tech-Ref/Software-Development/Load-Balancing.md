[Home](/Slalom-LLC/Slalom-Consulting) | [Glossary](/Glossary) | [Tech Ref](/Tech-Ref) | [Software Development](/Tech-Ref/Software-Development)
**Disambiguation:** [Content Delivery Network (CDN)](/Tech-Ref/Software-Development/CDN-\(Content-Delivery-Network\)), [Network Load Balancing (NLB)](/Tech-Ref/Networking/NLB-\(Network-Load-Balancing\)).

[[_TOC_]]

---
# Introduction
"_In computing ***Load Balancing*** refers to the process of distributing a set of tasks over a set of resources (computing units), with the aim of making their overall processing more efficient. Load balancing can optimize the response time and avoid unevenly overloading some compute nodes while other compute nodes are left idle._"

"_Load balancing is the subject of research in the field of parallel computers. Two main approaches exist: **static algorithms**, which do not take into account the state of the different machines, and **dynamic algorithms**, which are usually more general and more efficient, but require exchanges of information between the different computing units, at the risk of a loss of efficiency._"

## Reference
1. [Wikipedia: Load Balancing](https://en.wikipedia.org/wiki/Load_balancing_(computing))
1. [Logz.io: What Is Load Balancing and How Does It Work?](https://logz.io/blog/best-open-source-load-balancers/)
1. [AVINetworks: What Is Load Balancing?](https://avinetworks.com/what-is-load-balancing/)
1. [a10networks: How do Layer 4 Load Balancing and Layer 7 Load Balancing Differ?](https://www.a10networks.com/blog/how-do-layer-4-and-layer-7-load-balancing-differ/)
1. [Medium.com: Difference Between Layer 4 vs. Layer 7 Load Balancing](https://medium.com/@harishramkumar/difference-between-layer-4-vs-layer-7-load-balancing-57464e29ed9f)

---
# Topics
1. [BIG-IP (F5)](/Tech-Ref/F5-Inc/BIG%2DIP-\(F5\)).
1. [Content Delivery Network (CDN)](/Tech-Ref/Software-Development/CDN-\(Content-Delivery-Network\)).
1. [Development and IT Operations (DevOps)](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)).
1. [Quality of Service (QoS)](/Tech-Ref/Software-Development/DevOps-\(Development-and-IT-Operations\)/QoS-\(Quality-of-Service\)).
1. [Software Development](/Tech-Ref/Software-Development).
1. [Web Application](/Tech-Ref/WWW-\(World-Wide-Web\)/Web-Application).

---

# Load Balancers (Scaling Out)
Load balancer types vary according to the [OSI model](/Tech-Ref/OSI-Model) layer at which the load balancer “_operates_.” 

## Layer 4 Load Balancing (Classic & NLB)
"_Classic load balancers, also known as “plain old load balancers” (POLB) operate at layer 4 of the [OSI](/Tech-Ref/OSI-Model). They take client requests, which are composed of TCP or UDP packets, and make decisions that route the requests based on common algorithms._

"_[Network Load Balancers (NLB)](/Tech-Ref/Networking/NLB-\(Network-Load-Balancing\)) also operate at [layer 4](/Tech-Ref/OSI-Model), but they can scale to handle large amounts of requests and can route traffic using hashing algorithms based on information like port and IP address._"

## Layer 7 Load Balancing (Application)
Application Load Balancers operate at [layer 7 of the OSI](/Tech-Ref/OSI-Model), making routing decisions based on the actual content of the application traffic, like [HTTP](/Tech-Ref/WWW-\(World-Wide-Web\)/HTTP-\(Hypertext-Transfer-Protocol\)) headers, queries, and [URLs](/Tech-Ref/WWW-\(World-Wide-Web\)/URI-\(Uniform-Resource-Identifier\)/URL-\(Uniform-Resource-Locator\)). Choosing what type of load balancer to implement depends heavily on your use case.

### Application Delivery Controler (ADC)
- [Application Delivery Controller (ADC)](/Tech-Ref/Software-Development/Load-Balancing/ADC-\(Application-Delivery-Controller\)).

---
# Load Balancing Methods
These common algorithms form the backbone of most load balancers. Although, Application Load Balancers can make more sophisticated decisions based on the application traffic.

## Round Robin
The load balancer distributes connection requests to a pool of servers in a repeating loop, regardless of relative load or capacity. Server A, server B, server C, server A, server B, etc. 

## Weighted Round Robin
This is like the standard round robin, except for the fact that certain back end servers can be assigned to a higher priority, receiving disproportionally more traffic/requests. Server A, server A, server B, server C, server A, server A, server B, server C, etc. 

## Least Connections
This algorithm is fairly self-explanatory; the load balancer sends a new request to the back end server with the least number of active connections. 

## Weighted Least Connections
This algorithm is like least connections, but certain back end servers can be assigned a higher priority, receiving disproportionally more traffic/requests. In a scenario where some back end servers have a larger or more performant resource configuration, you would use WLC to route them a greater share of the traffic.

## Random
Requests are sent to back end servers in a completely random fashion. No considerations are made for load levels, connection count, etc. 
