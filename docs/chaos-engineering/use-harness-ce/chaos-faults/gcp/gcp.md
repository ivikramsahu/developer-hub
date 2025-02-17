---
id: gcp
title: Chaos faults for GCP
redirect_from:
- /docs/chaos-engineering/technical-reference/chaos-faults/gcp
- /docs/chaos-engineering/chaos-faults/gcp
---

<!-- Import statement for Custom Components -->

import FaultDetailsCard from "@site/src/components/ChaosEngineering/FaultDetailsCard";
import ExperimentListSection from "@site/src/components/ChaosEngineering/ExperimentListSection"
import { experiments } from "./experiments"

<!-- Heading Description -->

## Introduction

GCP faults disrupt the resources that run on a GCP cluster. Different faults disrupt various aspects of the GCP cluster, based on which GCP faults are categorized into different types.
Fault execution is triggered when the chaosengine resource is created. Chaosengines are embedded within the steps of a chaos fault, but you can also create the chaosengine manually, and the chaos operator reconciles this resource and triggers the fault execution.

<!-- Experiment List and Search Bar (every experiment added below, need to be added in this file also) -->

<ExperimentListSection experiments={experiments} />

<!-- Code for Fault Card starts from here -->

<FaultDetailsCard category="gcp">

### GCP SQL Instance Failover

GCP SQL Instance Failover disrupts the state of GCP SQL instance filtered using a name and project ID by triggering failover on the SQL instance.

<Accordion color="green">
<summary>Use cases</summary>

- Determines the resilience of the GKE infrastructure.
- Determines how quickly an SQL Instance can recover when one of the replicas trigger a failover.

</Accordion>

</FaultDetailsCard>

<FaultDetailsCard category="gcp">

### GCP VM disk loss by label

<!-- Need above heading in markdown ### for it to populate right navigation bar and generate links -->

It disrupts the state of GCP persistent disk volume filtered using a label by detaching the disk volume from its VM instance for a specific duration.

<!-- <Accordion color='green'/> has same usage as details but green in color -->

<Accordion color="green">
<summary>Use cases</summary>
    This fault can be used to determine the resilience of the GKE infrastructure. It helps determine how quickly a node can recover when a persistent disk volume is detached from the VM instance associated with it.
</Accordion>

<!-- ensure to enclose all markdown inside the <FaultDetailsCard/> tag-->

</FaultDetailsCard>

<!-- Code for Fault Card ends here -->

<!-- Code for Fault Card starts from here -->

<FaultDetailsCard category="gcp">

### GCP VM disk loss

<!-- Need above heading in markdown ### for it to populate right navigation bar and generate links -->

It disrupts the state of GCP persistent disk volume by detaching the disk volume from its VM instance using the disk name for a specific duration.

<!-- <Accordion color='green'/> has same usage as details but green in color -->

<Accordion color="green">
<summary>Use cases</summary>
    This fault can be used to determine the resilience of the GKE infrastructure. It helps determine how quickly a node can recover when a persistent disk volume is detached from the VM instance associated with it.
</Accordion>

<!-- ensure to enclose all markdown inside the <FaultDetailsCard/> tag-->

</FaultDetailsCard>

<!-- Code for Fault Card ends here -->

<FaultDetailsCard category="gcp">

### GCP VM instance stop by label

<!-- Need above heading in markdown ### for it to populate right navigation bar and generate links -->

It powers off GCP VM instances (that are filtered by a label) for a specific duration.

<!-- <Accordion color='green'/> has same usage as details but green in color -->

<Accordion color="green">
<summary>Use cases</summary>
    This fault determines the resilience of an application that runs on a VM instance when a VM instance unexpectedly stops (or fails).
</Accordion>

<!-- ensure to enclose all markdown inside the <FaultDetailsCard/> tag-->

</FaultDetailsCard>

<!-- Code for Fault Card ends here -->

<FaultDetailsCard category="gcp">

### GCP VM instance stop

<!-- Need above heading in markdown ### for it to populate right navigation bar and generate links -->

It powers off a GCP VM instance based on the instance name (or list of instance names) for a specific duration.

<!-- <Accordion color='green'/> has same usage as details but green in color -->

<Accordion color="green">
<summary>Use cases</summary>
This fault determines the resilience of an application that runs on a VM instance when a VM instance unexpectedly stops (or fails).
</Accordion>

<!-- ensure to enclose all markdown inside the <FaultDetailsCard/> tag-->

</FaultDetailsCard>

<!-- Code for Fault Card ends here -->

<FaultDetailsCard category="gcp">

### GCP VM service kill

<!-- Need above heading in markdown ### for it to populate right navigation bar and generate links -->

It shuts down a service on GCP VM instances (identifiable by name) for a specific duration.

<!-- <Accordion color='green'/> has same usage as details but green in color -->

<Accordion color="green">
<summary>Use cases</summary>
    This fault determines the resilience of a GKE node instance when a service on the instance unexpectedly stops (or fails).
</Accordion>

<!-- ensure to enclose all markdown inside the <FaultDetailsCard/> tag-->

</FaultDetailsCard>

