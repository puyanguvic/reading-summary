## 2022' Stateful Multi-Pipelined Programmable Switches
Given the clock rate of a single packet processing pipeline has saturated due to slowdown in transistor scaling, today’s programmable switches employ multiple parallel pipelines to meet high packet processing rates. However, parallel processing poses a challenge for stateful packet processing, where it becomes hard to guarantee functional correctness while maintaining line rate processing. This paper presents the design and implementation of MP5, which is a new switch architecture, compiler, and runtime for multi-pipelined programmable switches that is functionally equivalent to a logical single pipelined switch while also processing packets close to the ideal processing rate, for all packet processing programs.

**Main idea** multi-pipelined programmable switch processing pipeline that achieves the following two goals.
• Correctness. The multi-pipelined switch is functionally equivalent to the single pipelined switch.
• Performance. The multi-pipelined switch processes packets as close to line rate (i.e., 𝑁∗𝐵) as theoretically possible for a given packet processing program and stream of input packets, without compromising on correctness.

It is a P4 and Domino following work in SDN control plane, to improve the packet processing rate.


## 2021' Programmable Packet Scheduling with a Single Queue
Programmable packet scheduling enables scheduling algorithms to be programmed into the data plane without changing the hardware. Existing proposals either have no hardware implementations for switch ASICs or require multiple strict-priority queues. We present Admission-In First-Out (AIFO) queues, a new solution for programmable packet scheduling that uses only a single first-in first-out queue. AIFO is motivated by the confluence of two recent trends: shallow buffers in switches and fast-converging congestion control in end hosts, that together leads to a simple
observation: the decisive factor in a flow’s completion time (FCT) in modern datacenter networks is often which packets are enqueued or dropped, not the ordering they leave the switch. The core idea of AIFO is to maintain a sliding window to track the ranks of recent packets and compute the relative rank of an arriving packet in the window for admission control. Theoretically, we prove that AIFO provides bounded performance to Push-In First-Out (PIFO). Empirically, we fully implement AIFO and evaluate AIFO with a range of real workloads, demonstrating AIFO closely approximates PIFO. Importantly, unlike PIFO, AIFO can run at line rate on existing hardware and use minimal switch resources—as few as a single queue.

**Main idea** AIFO is a new approach to programmable packet scheduling that uses only a single queue. AIFO computes a rank quantile for a coming packet and decides whether to admit the packet into the queue based on the rank qunatile and the queue length. It based on slicing window to adjust the packet order and give the first prioiry to the high rank packets.


## 2017' NFVnice: Dynamic backpressure and scheduling for NFV service chains
Managing Network Function (NF) service chains requires careful system resource management. We propose NFVnice, a user space NF scheduling and service chain management framework to provide fair, efficient and dynamic resource scheduling capabilities on Network Function Virtualization (NFV) platforms. The NFVnice framework monitors load on a service chain at high frequency (1000Hz) and employs backpressure to shed load early in the service chain, thereby preventing wasted work. Borrowing concepts such as rate proportional scheduling from hardware packet schedulers, CPU shares are computed by accounting for heterogeneous packet processing costs of NFs, I/O, and traffic arrival characteristics. By leveraging cgroups, a user space process scheduling abstraction exposed by the operating system, NFVnice is capable of controlling when network functions should be scheduled. NFVnice improves NF performance by complementing the capabilities of the OS scheduler but without requiring changes to the OS’s scheduling mechanisms. Our controlled experiments show that NFVnice provides the appropriate rate-cost proportional fair share of CPU to NFs and significantly improves NF performance (throughput and loss) by reducing wasted work across an NF chain, compared to using the default OS scheduler. NFVnice achieves this even for heterogeneous NFs with vastly different computational costs and for heterogeneous workloads.

## 2016' Packet Transactions: High-Level Programming for Line-Rate Switches




## 2003' Routing Using Potentials: A Dynamic Traffic-Aware Routing Algorithm
We present a routing paradigm called PB-routing that utilizes steepest gradient search methods to route data packets. More specifically, the PB-routing paradigm assigns scalar potentials to network elements and forwards packets in the direction of maximum positive force. We show that the family of PB-routing schemes are loop free and that the standard shortest path routing algorithms are a special case of the PB-routing paradigm. We then show how to design a potential function that accounts for traffic conditions at a node. The resulting routing algorithm routes around congested areas while preserving the key desirable properties of IP routing mechanisms including hop-byhop routing, local route computations and statistical multiplexing. Our simulations using the ns simulator indicate that the traffic aware routing algorithm shows significant improvements in end-to-end delay and jitter when compared to standard shortest path routing algorithms. The simulations also indicate that our algorithm does not incur too much control overheads and is fairly stable even when traffic conditions are
dynamic.

**Main idea:** This traffic-aware routing is based on steepest gradient search methods. In this work, the queue length information is assumed instantaneously available at all nodes when ever a achange occurs.

**Limitations:** 
1. If the network topology is sparsedly connected, this algorithm does not perform any better than OSFF.
2. The queue length of all the node could not be get instantaneously.
3. When congestion happened in the bottleneck link. This algorithm could not do anything.
