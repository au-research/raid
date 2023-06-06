### Primary AWS region for raid.org

* Status: proposed                                     
* Who:  proposed by STO                               
* When: proposed on 2023-06-06
* Related: none 


# Decision

What region should we use for operating raid.org in AWS?


# Context

## STO opininion

Recommened us-east-2 (Ohio)

* US because all roads lead to Rome
* East coast for lower latency to EU
* us-east-2 to avoid instability, cost and resource contention of us-east-1
  * us-east-1 is the "default" region that most examples point to, it 
    generally sees the first rollout of new stuff (which we don't care about)
  * us-east-1 costs the most and has the most resource contention


# Consequences / Implications

* Operational cost - the busier a region is, the more expensive compute is, 
  espcially spot capacity
* Resource availability - the busier a region is, the more likely a specific 
  class of resource might be unavailable (cost and availability are linked 
  specifically to drive this)
* Stability - us-east-1 sees most things deployed first in this region, 
  us-east-1 tends to have more issues than other regions.  Most demos and 
  sample projects are written for us-east-1 
* Feature availability - because us-east-1 is usually the first to be 
  rolledout, features tend to be available there earlier than other regions
* Latency - wherever we use, some places will be futher away than others


# Links

* https://aws.amazon.com/about-aws/global-infrastructure/
