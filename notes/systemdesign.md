# Systems design

* Scaling
  * horizontal and vertical
* load balancing - distribute load
  - service discovery
  - health check
  - lb based on one algorithm
    * least connection
    * round robin
    * least response time
    * ip hash
* cdn
  - offload traffic to edge servers
  - as cache
* microservices (more info on separate note)
* sharding
  - split data based on some attribute
* availability
  - serial components -> multiply availability of all components (decreases)
  - parallel -> availability increases with increase in components


HA principles
* eliminate SPOF - single point of failure
* reliable crossover point
* deletection of failures

SPOF
* identify spof
* try active/active configurations
* have multiple lbs and failover if one of them goes down
* monitor spofs carefully
* route based on geography
* spread servers/lbs etc across regions/racks/servers

Fault tolerance metrics
* MTTR - mean time to recover
* MTBF - between failures
* MTTF - time to failure
* MTTD - time to detect
* failure rate

swimlane - for fault tolerance

Backpresure
* happens when different systems process at different speeds
* strategies
  - control producer
  - buffer
  - drop
