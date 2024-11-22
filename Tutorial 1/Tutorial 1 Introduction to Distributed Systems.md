# Tutorial 1: Introduction to Distributed Systems

Answer: Le Liu

**1. Describe the key features of a Distributed System?**

Transparent, open, scalable

**2. What is the difference between the following terms: host, site, server, client? **

Host: A host is a specific machine that is connected into the DS

Site: A site is a geographical location that contains one or more hosts in the DS

Server: A host makes resources available to the DS

Client: A host accesses the servers and utilizes any available resources

**3. What  is  the  difference  between  a  loosely-coupled  and  a  tightly  coupled  Distributed 
System? Give a real-world example of each**

loosely-coupled: Computers are connected over a network. Such as Internet.

tightly-coupled: Multiple processors within a single computer sharing memory and resources. Such as multi-processor systems.

**4. The  lecture  notes  state  “a  Distributed  System  has,  by  default,  no  global  clock”. 
Explain why this is the case.**

Distributed systems have no common clock. In each computer, it maintains an internal clock, known as a Real Time Clock. It is impossible to guarantee that the real-time clocks of two computers will run at the same speed.

**5. In what way are the concepts of redundancy and reliability related?**

By increasing the number of copies or key components, the system can continue to operate when a part fails, thereby improving reliability.

**6. When would the  use  of concurrency for a processing task might be a disadvantage? **

Task management, network communication. They may be have costs. Increased Complexity.

**7. Why is middleware important? List the main benefits of using middleware. **

It delivers an abstract layer of support that acts as a building block for the 
construction of the target application(s).

- Remote Method Invocation
- Support for communication between groups of processes
- Event Notification
- Support for partitioning, placement, and retrieval of shared data objects 
  amongst cooperating computers
- Support for the replication of shared data objects
- Real-time Multimedia Transmission

**8. Using Lamport’s concept of a “happens before” relation, identify all the events that**

**a) happen before p3.**

$p_1$ , $p_2$, $q_1$, $r_1$, $r_2$, $r_3$

**b) p3 happens before**

No

**c) are concurrent with p3. **

$q_2$, $q_3$, $r_4$

**9. What is the difference between a “logical clock“ and a real-time clock**

The RTC is maintained internally by the computer. This clock is powered by a separate battery so that it continues to
function even when the computer is turned off. But, it is impossible to guarantee that the real-time clocks of two computers will run at the same speed.

The logical clock be used to capture Temporal Ordering or Causal Ordering between events. 



**10. In the system shown in Figure 1, a snapshot was taken that has recorded the following events: {p1, p2, q1, q2, r1, r2, r3}. Is this a “consistent snapshot”? Explain your answer.**

![image-20240928212624296](C:/Users/Mrle/AppData/Roaming/Typora/typora-user-images/image-20240928212624296.png)

This is a **consistent snapshot**. For any pair of given events. Such that event e is in the cut C, and f -> e, then f is also in the cut C.

**Q11![无标题的笔记本 (2)-1](https://mrle-1316607909.cos.ap-hongkong.myqcloud.com/%E6%97%A0%E6%A0%87%E9%A2%98%E7%9A%84%E7%AC%94%E8%AE%B0%E6%9C%AC%20(2)-1.jpg)**

![无标题的笔记本 (2)-2](https://mrle-1316607909.cos.ap-hongkong.myqcloud.com/%E6%97%A0%E6%A0%87%E9%A2%98%E7%9A%84%E7%AC%94%E8%AE%B0%E6%9C%AC%20(2)-2.jpg)
