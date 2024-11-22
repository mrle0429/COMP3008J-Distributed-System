---
title: COMP3008J Distributed System Tutorial #3
author: Le Liu
---



# Distributed System Tutorial #3

1. **What is routing?  What criteria are considered during a 'routing decision'?**

routing是在网络中用于决定数据包从源地址到目标地址路径的过程。

routing decision需要考虑：

**Scalability：**节点增加仍能保证高效的路由路径决策

**Load Balancing**：分散节点的负载，避免某些节点负载过重

**Network Dynamics**：考虑节点增加，删除，故障情况。路由决策适应这种变化

**Fault Tolerance：**备用线路的考虑。

**Target Identification**

**Security and Anonymity**



2. **What is an overlay? Briefly describe what a routing overlay is.**

**Overlay** is used to clarify that it is an application layer routing mechanism (it is not a network layer mechanism like IP routing).

Routing overlay是实现路由功能的逻辑结构。它根据特定的算法，在节点之间转发消息，确保快速通信。It directs the request to a node on which a replica (or the original) of   the resource resides. 它还负责增加，删除资源节点，并为他们创建GUID.

3. **Pastry Node Routing Decision**

![屏幕截图 2024-11-22 144558](E:/BDIC/Stage3_1/DistributedSystems/Tutorial%203/%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%202024-11-22%20144558.png)

4.  **Reliable Multicast**

5. **Briefly explain the gossip architecture. Give an example of when it may be necessary to sacrifice consistency for high availability.**

The Gossip architecture is a  framework  for implementing highly  available  services.

A node receives or generates new information. It randomly selects one or more nodes to share the information. The receiving nodes continue propagating the information to their peers. The process repeats until the information has been shared with all nodes.



 Offline Payment Authorization

- In scenarios where network connectivity is limited, payment systems like credit cards or mobile wallets allow offline authorization of transactions.

- Reason for Sacrificing Consistency:
  - Enforcing consistency would require real-time verification, causing delays or failures in areas with poor connectivity.
- Outcome:
  - Transactions might be temporarily processed offline, with conflicts (e.g., insufficient funds) resolved during later reconciliation.