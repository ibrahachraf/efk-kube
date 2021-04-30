When running multiple services and applications on a Kubernetes cluster, a centralized, cluster-level logging stack can help you quickly sort through and analyze the heavy volume of log data produced by your Pods. One popular centralized logging solution is the Elasticsearch, Fluentd, and Kibana (EFK) stack.

Step 1 — Creating a Namespace :

Before we roll out an Elasticsearch cluster, we’ll first create a Namespace into which we’ll install all of our logging instrumentation.This Namespace will also allow us to quickly clean up and remove the logging stack without any loss of function to the Kubernetes cluster.
~~~~
$ nano kube-logging.yaml
~~~~
~~~~
kind: Namespace
apiVersion: v1
metadata:
  name: kube-logging
~~~~~~
