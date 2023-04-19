---
layout: default
title: "Disaster recovery"
---

## Disaster recovery

In its commitment to transparency, Cake Labs is publishes this disaster recovery plan for the pricing API service. Note that contracts may include an [SLA](/docs/sla.md). This document is a recovery plan, not an SLA.

## DNS failure

Cake Labs uses a DNS provider with a 100% uptime guarantee. Should the DNS provider be unable to operate, then Cake Labs will migrate DNS to another provider if necessary, and it will apply for SLA credits with this provider.

## Datacenter failure

Cake Labs uses multiple datacenters around the world to mitigate the risks of datacenter failures having an impact on service.

Should a datacenter go offline, Cake Labs will review the situation to make sure that other datacenters are managing the increase in traffic, and Cake Labs will provision more resources in these datacenters if necessary.

In the extremely unlikely event that all service datacenters go offline, then Cake Labs will work to stand up servers on alternative datacenters.

## Inaccessible historical database

Cake Labs uses the extremely robust LMDB database system to ensure high uptime and a low risk of data corruption. Cake Labs makes regular backups of the pricing database, which can be restored quickly.

If the historical database becomes unavailable, Cake Labs will first make significant efforts to either continue providing spot pricing, or to make the spot pricing available again.

Then, Cake Labs will go through a database recovery procedure to recover past pricing data, and it will make all recovered data available again.
