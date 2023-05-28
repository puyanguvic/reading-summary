
## 2003' Routing Using Potentials: A Dynamic Traffic-Aware Routing Algorithm
We present a routing paradigm called PB-routing that utilizes steepest gradient search methods to route data packets. More specifically, the PB-routing paradigm assigns scalar potentials to network elements and forwards packets in the direction of maximum positive force. We show that the family of PB-routing schemes are loop free and that the standard shortest path routing algorithms are a special case of the PB-routing paradigm. We then show how to design a potential function that accounts for traffic conditions at a node. The resulting routing algorithm routes around congested areas while preserving the key desirable properties of IP routing mechanisms including hop-byhop routing, local route computations and statistical multiplexing. Our simulations using the ns simulator indicate that the traffic aware routing algorithm shows significant improvements in end-to-end delay and jitter when compared to standard shortest path routing algorithms. The simulations also indicate that our algorithm does not incur too much control overheads and is fairly stable even when traffic conditions are
dynamic.
**Main idea:** This traffic-aware routing is based on steepest gradient search methods. In this work, the queue length information is assumed instantaneously available at all nodes when ever a achange occurs.
**Limitations:** 
1. If the network topology is sparsedly connected, this algorithm does not perform any better than OSFF.
2. The queue length of all the node could not be get instantaneously.
3. When congestion happened in the bottleneck link. This algorithm could not do anything.
