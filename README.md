# kafka-marketplace-plans

This repo holds default values for Kafka strimzi custom resources. 

Use cases:
- expose Kafka strimzi as a managed service with open service broker
- provide default patterns that can be used out-of-the-box

## Repo structure

This repo contains skeleton for OSB service offerings:
- kafka-dedicated: each service instance provisions a standalone dedicated Kafka cluster
- kafka-shared: each service instance provisions a Kafka topic in a shared Kafka cluster

The following files support the two OSB service offerings: 
```
├── kafka-dedicated-osb-service-definition.json: Fragment of OSB service catalog for the "Dedicated Kafka" service offering
├── kafka-dedicated-instance: Helm chart associated with `cf create-service kafka-dedicated small my-kafka-cluster` ux
├── kafka-dedicated-binding:  Helm chart associated with `cf bind-service APP_NAME my-kafka-cluster` ux

├── kafka-shared-osb-service-definition.json
├── kafka-shared-cluster: Helm chart which gathers prerequisites to using the `kafka-shared` service offering 
├── kafka-shared-instance: Helm chart associated with `cf create-service kafka-shared small my-kafka-topic` ux
├── kafka-shared-binding: Helm chart associated with `cf bind-service APP_NAME my-kafka-topic` ux
```