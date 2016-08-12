# Hawkular Metrics Grafana

Simple Dockerfile to run a grafana in docker with the [hawkular-grafana-datasource](https://github.com/hawkular/hawkular-grafana-datasource) baked in.  Based on the [grafana docker image](https://github.com/grafana/grafana-docker).


## Run in Openshift

```

oc create -f openshift/metrics-grafana-dc.yaml

# Also you will need to edit your scc/anyuid to contain a grafana service account...

echo '{
  "apiVersion": "v1",
  "kind": "ServiceAccount",
  "metadata": {
    "name": "grafana"
  }
}' | oc create -f -

```