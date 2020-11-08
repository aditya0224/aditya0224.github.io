---
layout: post
title:  "Reliability"
author: "Adi Bhamidipati"
---

What is Reliability?
The application can be called Reliable if it holds the following

1. The application performs the function that the user expected.
2. The application can tolerate the user making mistakes or using the software in unexpted ways.
3. The Application Performance is good enough for the required use case, under the expected system load and data volume.
4. The Application prevents any unauthorized access and abuse.


Fault is a part of the system deviating from the specification or it's responsibility. Faults tends to lead to failure
Things that go wrong are called fault, a fault tolerant system[which can prevent faults instead of curing] are fault resilient systems
There are three types of faults
1. Hardware faults
RAM, hardware failurs
2. Software faults
 - Application can be taken down because of the long running processors which take down the whole application[dead locks], which uses high cpu and make system
 un responsive
3. Human errors:
 1. Configuration errors. Create admin dashboards and strict rules to avoid bad configurations
 2. Design the system so that modules can be de coupled and don't take the whole application down from small issues
 3. Tests, unit, integration and automation tests
 4. Roll back for bad deployments etc
 5. Monitoring for errors
 

