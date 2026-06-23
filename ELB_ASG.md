
## Section Overview
This section focuses on high availability and scalability.

## Takeaways 
 - There are two types of scalability: vertical + horizontal scaling. 
 - Vertical scaling refers to sizing resources up/down. (commonly seen with databases/instances)
 - Horizontal scaling refers to distributed systems. (Think of adding additional nodes)
 - High Availability, increases reliability in case of failure.


## Load Balancing
 - A load balancer is a set of servers that distribute traffic to our backend EC2 instances.
 - We can assign a single DNS point to our load balancer. Additionally, we can perform health checks against instances. 

## 4 Kinds of Managed Load Balancers
 - Classic load balancer - older generation. (HTTP/HTTPS/TCP/SSL)
 - Application load balancer - supports HTTP/HTTPS/WebSocket (layer 7)
 - Network load balancer - supports TCP/UDP protocol
 - Gateway load balancer - supports GENEVE protocol (layer 3)

## Application Load Balancer
 - Load balances to multiple applications across machines (target groups)
 - Load balances to multiple applications on the same machine (containers)
 - Supports HTTP/ HTTPS/ Websocket
 - Supports redirects from HTTP to HTTPS.

## Network Load Balancer
 - Forwards TCP & UDP traffic to instances.
 - High performance, handles millions of request per second.
 - Ultra low latency
 - NLB has one static IP per AZ.

## Gateway Load Balancer
 - Load balancer that uses third party virtual appliances to inspect packets prior to routing to ec2 instances.
 - Packets can be sent through a firewall/IDS/IPS
 - Uses GENEVE protocol 6081

## Sticky Sessions
 - Stickiness allows client to be redirected to the same instance behind a load balancer. 
 - An ideal use case would be, when you want to ensure users don't lose their session data. However, it is worth noting this can bring imbalance to your instances. 
 - "Cookies," is what makes stickiness possible; and they can be applied at the load balancer or target level.

