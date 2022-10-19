# Change Data Capture with AMQ Streams

Resource configurations for quickly provisioning a MySQL change data capture scenario using AMQ Streams

## Provisioning Instructions

1. Deploy the AMQ Streams operator.
   ```bash
   oc apply -f operators/
   ```
2. Create a new namespace for the CDC demo.
   ```bash
   oc new-project cdc-demo
   ```
3. Apply the demo manifest.
   ```bash
   oc apply -f cdc-demo/ -n cdc-demo
   ```
4. Create a new namespace for Prometheus.
   ```bash
   oc new-project cdc-prometheus
   ```
5. Apply the monitoring manifest
   ```bash
   oc apply -f cdc-prometheus/ -n cdc-prometheus
   ```