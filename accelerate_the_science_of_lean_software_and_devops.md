Accelerate: The Science of Lean Software and DevOps: Building and Scaling High Performing Technology Organizations
---

> Nicole Forsgren, Jez Humble, Gene Kim

# TOC
<!-- TOC depthFrom:2 -->

- [Continuous Delivery](#continuous-delivery)
    - [Measurement](#measurement)
- [Architecture](#architecture)
    - [Measurement](#measurement-1)
- [Security](#security)
- [Lean Management](#lean-management)
- [Lean Product Development](#lean-product-development)
- [Deployment Pain](#deployment-pain)
- [Leadership](#leadership)

<!-- /TOC -->
---

## Continuous Delivery

In order to implement continuous delivery, you need the following foundations:

* *Comprehensive configuration management* - configuring environments, building, testing and deploying software fully automated. All changed applied using automation.
* *Continuous integration* - short lived feature branches. Changes integrated into trunk/master frequently. High preforming organizations have the shortest integration times and branch lifetimes, lasting typically 1 hour to 1 day max.
* *Continuous testing* - unit and integration testing on every commit. All automated tests should run on workstations.

### Measurement

The best things to continuously measure:

* *Lead time* - time it takes from commit to production.
* *Deployment frequency* - how often are we deploying changes to production (this change may include multiple commits).
* *Mean time to restore* - how quickly can a service be restored.
* *Change fail percentage* - what percentages of changes to production fail (resulted in degraded service or require remediation like hot fixes, patches, roll backs).

eNPS used to measure customer "loyalty". Useful way to measure internal developer happiness.

You should also measure these blockers to continuous delivery:

* How many manual changes to production
* How long (time) feature branches stay open and un-merged
* How many PRs are merged with failed builds

## Architecture

Two main architectural characteristics

* *Testability* - most testing can be done without an integration environment (staging)
* *Deployability* - can deploy independent of other applications or services

Architectural approaches that enable testing strategy include:

* The use of bounded contexts and APIs as a way to decouple large domains into smaller, more loosely coupled units
* The use of test doubles and virtualization as a way to test services or components in isolation

High performers are more likely to have the following capabilities:

* Can do most testing without integrated environment
* Can deploy and release apps independently
* Micro services architecture

### Measurement

* The number of deploys per day per developer. This helps you see if adding more developers actually slows things down due to communication overhead, or scales linearly.

## Security

* [The Rugged Manifesto](http://ruggedsoftware.org/)
* Shift left on security

## Lean Management

* Limit WIP
* Visual displays show key quality and productivity metrics. Status of work, including defects
* Use data from application and infrastructure monitoring to make business decisions

## Lean Product Development

* Work in small batches
* Visualize the flow of work from business to customers
* Actively seek customer feedback and incorporate it

## Deployment Pain

3 factors causing painful or brittle deployment processes:

* Software not written with deployment in mind. Common symptom is when complex, orchestrated deployments are required due to the software expecting the environment and dependencies setup in a particular way. Gives little useful information on what is wrong and why it is failing to operate correctly
* Probability of failed deployments failing rises substantially when manual changes must be made to production environments as part of the deployment process. (Errors caused by typing things wrong, poor docs)
* Handoffs between teams (ops, dev, sec, dba)

To reduce deployment pain:

* Build systems that can be deployed easily into multiple environments. Detect and tolerate failure, allow component updates separately
* Ensure state of production can be reproduced in automated fashion from version control
* Intelligent application and platform so deployment can be simple as possible

Deployment pain highly correlated with burn out and bad culture.

## Leadership

Investing in the following to accelerate teams:

* Training budget
* Tech conferences
* Internal hack days for cross functional collaboration
* "Yak days" - work together to kill technical debt
* DevOps mini conferences. Talks and open spaces to work on particular topics
* Dedicated 20% time to work on own ideas

To improve/enable cross-functionality collaboration:

* Build trust with other teams. Keep promises, keep communication open and behave predictably
* Encourage people to move between teams and departments
* Seek, encourage and rewarding work that facilitates communication
