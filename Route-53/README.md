# Route 53

- Route 53 is a managed DNS (Domain Name System)
- A DNS is a collection of rules and records that helps clients understand how to reach a server through URLs.

## Diagram for a Record

![](../Images/rec.png)

- Uses Route 53 to be able to use an URL to get the IP address of the application server

## Routing Policies

![](../Images/ro.png)
![](../Images/po.png)

They choose the server based on...
1. nothing
2. health + load (kind of like a load balancer)
3. health + distance
4. health

# Steps

1. Route 53
2. Register Domain (costs money)
3. Wait till it is registered
4. Hosted zones
5. Click on domain name to see records
6. EC2
7. Create instances (without keypair and with HTTP traffic allowed) - in different regions e.g. ireland and oregon
8. Go back to domain
9. Create a record (quick create)
   1. name = www
   2. type = A
   3. value = IP of Ireland instance
   4. Routing policy = Latency
   5. Region = Europe(Ireland)
   6. Record ID = My instance from Ireland
10. Create another record
   1. name = www
   2. type = A
   3. value = IP of Oregon instance
   4. Routing policy = Latency
   5. Region = US West (Oregon)
   6. Record ID = My instance from the US
11. Create records
12. If you now go to www.(domain name) it will take you to the instance that is geographically closest.
13. If you use a vpn to look like you are in the US it ill take you to the Oregon instance.