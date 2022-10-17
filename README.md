# Change Data Capture with AMQ Streams

Resource configurations for quickly provisioning a MySQL change data capture scenario using AMQ Streams

## Provisioning Instructions

1. Deploy the AMQ Streams operator.
   ```bash
   oc apply -f openshift-operators/Subscription_amq-streams.yaml -n openshift-operators
   ```
2. Create a new namespace for the demo.
   ```bash
   oc new-project cdc-demo
   ```
3. Apply the demo manifest.
   ```bash
   oc apply -f cdc-demo/ -n cdc-demo
   ```