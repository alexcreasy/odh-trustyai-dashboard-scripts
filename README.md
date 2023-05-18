# Trusty AI / ODH Integration Demo

WIP

Run in order:
```
oc apply -f resources/odh-base.yaml

oc apply -f resources/odh-dashboard.yaml

oc apply -f resources/odh-modelserving.yaml

oc apply -f resources/trustyai.yaml

oc apply -f resources/namespace-trustyai-e2e-modelmesh.yaml

oc project trustyai-e2e-modelmesh

oc process -f resources/odh-data-connection-template.yaml --param-file=<env_file> | oc create -f -

oc apply -f resources/servingruntime-ovms.yaml

oc apply -f resources/inferenceservice-demo-loan-nn-onnx-alpha.yaml

oc apply -f resources/inferenceservice-demo-loan-nn-onnx-beta.yaml
```

Next run scripts for metric registration and to simulate deployment of the model (currently only in Rob's repo, coming soon).


