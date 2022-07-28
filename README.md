# BYON Demo

This repo is designed to create an environment to demo BYON.

## How to Deploy

Deploy the OpenDataHub Operator

```
oc apply -k opendatahub-operator/overlays/stable
```

Once the operator has finished deploying, deploy the ODH instance:

```
oc apply -k opendatahub-instance/overlays/default
```

The ODH instance should be deployed in the `byon-demo` namespace.

To access the dashboard run the following command:

```
oc get route odh-dashboard -o=jsonpath='{.spec.host}' -n byon-demo
```
