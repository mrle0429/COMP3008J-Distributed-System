# Distributed System

## Introduction

### 1. 分布式系统的定义

 A collection of independent computers that appear to the users of the system as a single computer.  Any system that consists of hardware or software components located at networked computers that communicate and coordinate their actions via message passing

多个独立计算机组成的系统，这一系统可以被用户视作单个计算机。核心特征是独立的计算机通过信息传递使用网络通信和协作运行。

### 2. 分布式系统特点

- Transparent: Hiding the actual structure of the system form user.
- 用户不必知道实际的系统结构
- Open: Supporting the addition/removal of resources at run-time
- 使用开放标准
- Scalable: The system can expand to meet increased demand.
- 分布式系统可以增加新的计算资源。

### 3. 术语

- Site. 包含一个或多个主机的地理位置
- Host. 连接到分布式系统上具体的设备
- Resource. A resource is a program or data that resides on a host.
- Task. a specific set of instructions that a user asks the distributed system to execute

### 4. 优势

**Resource Sharing**

Each node can access and utilize the available resources of the other nodes in the system.

每个节点可以访问和利用其他节点的资源

**Concurrency** 

Multiple machines allows multiple users to work in parallel.

多机器和用户可以同时执行任务

**Global Time**

Some tasks carried out by a distributed system require a shared concept of  time.

某些任务需要一个统一的时间概念。

**Reliability**

Reliability refers to the ability of the system to continue functioning after the  failure of a component.

即使某些组件出现故障，分布式系统仍能继续工作

**Scalability**

Scalability is concerned with how well can a system handle increasing numbers of users and resources.

系统可以随着用户和资源数量的增加而扩展。

### 5. 挑战

**Heterogeneity**

异构性

The heterogeneity of a Distributed System refers to its ability to work  with different: • Networks, Computer Hardware, Operating Systems, Programming  Languages, Implementations by Different Developers

分布式系统需要支持不同类型的硬件、网络和操作系统。

 **Openness**

Openness refers to the degree to which a system is extensible

系统可扩展的程度。

### 6. System Models

**Architectural Models**

Defines the set of components that make up a system and the interplay between those components.

组件分类：

服务器，客户端，对等进程

**Software Architecture Models**

This layered model presents an abstraction of an individual computer that acts as a node within some Distributed System

层次：

- 平台层
- 中间件层
- 应用层

**Middleware**

中间件是运行在分布式系统中一组计算机上的进程或对象，这些对象之间协同工作，为分布式系统提供通信和资源共享的支持。
中间件提供了一个抽象层，用来充当构建目标应用程序的构件。