# Scalling

- [Scalling](#scalling)
  - [1. Vertical Scaling](#1-vertical-scaling)
  - [2. Horizontal Scaling](#2-horizontal-scaling)
    - [Drawbacks](#drawbacks)
  - [Comparison](#comparison)
- [Load balancers](#load-balancers)

Given architecture is an example of a client-server based system. In this, there is a client who sends requests to the server and then the client receives a response from the server accordingly but when the number of users/clients increases, the load on the server increases enormously which makes it difficult for the server to perform efficiently and hence becomes slow. Therefore, it is important to make the server scalable in a way such that the server capacity increases according to the increasing traffic without any sort of failure.
**Scaling** is the process of expanding resources and performance with increasing load and traffic on an existing system without increasing complexity. Horizontal and vertical scaling are two types of scaling methods.
![scaling](52.jpg)

![Scaling](saclling.png)

Option for scaling your database can be grouped into two major categories… 
* Vertical Scaling
* Horizontal Scaling
  
![sacling concepts](Scaling-Concept.png)

## 1. Vertical Scaling
In simple terms upgrading the capacity of a single machine or moving to a new machine with more power is called vertical scaling. You can add more powers to your machine by adding better processors, increasing RAM, or other power increasing adjustments. Vertical scaling can be easily achieved by switching from small to bigger machines but remember that this involves downtime. You can enhance the capability of your server without manipulating your code. 

* This approach is also referred to as the ‘scale-up‘ approach.
* It doesn’t require any partitioning of data and all the traffic resides on a single node with more capacity.
* Easy implementation.
* Less administrative efforts as you need to manage just one system.
* Application compatibility is maintained.
* Mostly used in small and mid-sized companies.
* MySQL and Amazon RDS is a good example of vertical scaling.
  
## 2. Horizontal Scaling
This approach is the best solution for projects which have requirements for high availability or failover. In horizontal scaling, we enhance the performance of the server by adding more machines to the network, sharing the processing and memory workload across multiple devices. We simply add more instances of the server to the existing pool of servers and distribute the load among these servers. In this approach, there is no need to change the capacity of the server or replace the server. Also, like vertical scaling, there is no downtime while adding more servers to the network. Most organizations choose this approach because it includes increasing I/O concurrency, reducing the load on existing nodes, and increasing disk capacity. 

* This approach is also referred to as the ‘scale-out’ approach.
* Horizontal scalability can be achieved with the help of a distributed file system, clustering, and load–balancing.
* Traffic can be managed effectively.
* Easier to run fault-tolerance.
* Easy to upgrade
* Instant and continuous availability.
* Easy to size and resize properly to your needs.
* Implementation cost is less expensive compared to scaling-up
* Google with its Gmail and YouTube, Yahoo, Facebook, eBay, Amazon, etc. are heavily utilizing horizontal scaling.
* Cassandra and MongoDB is a good example of horizontal scaling.
### Drawbacks
* Complicated architectural design
* High licensing fees
* High utility costs such (cooling and electricity)
* The requirement of extra networking equipment such as routers and switches.

## Comparison
	
| Horizontal Scaling      | Vertical Scaling  |
| ----------- | ----------- |
| Load balancing required      | Load balancing not required       |
| Resilient to system failure  | Single point of failure        |
|Utilizes Network Calls|Interprocess communication|
|Data inconsistency|Data consistent|
|Scales well|Hardware limit|

# Load balancers
A load balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. Load balancers are used to increase capacity (concurrent users) and reliability of applications. They improve the overall performance of applications by decreasing the burden on servers associated with managing and maintaining application and network sessions, as well as by performing application-specific tasks.

![laod balancer](what%20is%20load%20balancing.png)



# Refferences
* https://www.f5.com/services/resources/glossary/load-balancer#:~:text=A%20load%20balancer%20is%20a,users%20and%20reliability%20of%20applications.
*  https://www.geeksforgeeks.org/system-design-horizontal-and-vertical-scaling/
*  https://github.com/mgp/book-notes/blob/master/high-scalability-notes.markdown
*  https://gist.github.com/vasanthk/485d1c25737e8e72759f
