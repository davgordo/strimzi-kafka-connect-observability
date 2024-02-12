# Change Data Capture with AMQ Streams

Resource configurations for quickly provisioning a MySQL change data capture scenario using AMQ Streams

## Provisioning Instructions

1. Provision namespaces for the CDC demo.
   ```bash
   oc new-project cdc-demo
   oc new-project cdc-prometheus
   oc new-project cdc-jaeger
   oc new-project cdc-upstream
   ```
2. Provision operators.
   ```bash
   oc new-project openshift-distributed-tracing
   oc apply -f operators/
   ```
3. Provision observability platform components.
   ```bash
   oc apply -f cdc-prometheus/ -n cdc-prometheus
   oc apply -f cdc-jaeger/ -n cdc-jaeger
   ```
4. Provision the demo CDC scenario.
   ```bash
   oc apply -f cdc-demo/ -n cdc-demo
   ```
5. Provision the upstream data producer
   ```
   oc apply -f cdc-upstream/ -n cdc-upstream
   ```