# Helm environment demo

This demo shows a helm structure that supports multiple versions of an app team's helm chart managed over different environments.
The `app-helm-chart` chart has two versions with a minor difference:
* version `0.1.0` has 1 pod of nginx
* version `0.2.0` has 2 pods of nginx

After deploying this demo, you will see that the `app-helm-chart-dev` namespace has 2 pods and the `app-helm-chart-prod` namespace has 1 pod.
This is all managed through argocd and additional helm charts to manage the individual environments.

## Run it
* Install OpenShift GitOps
* Install the demo app-of-apps from this repo

`oc apply -f app-of-apps.yaml`

## What is happening

Folders are

* `app-helm-chart` - this folder holds an example application helm chart, just deploying some nginx
* `dev` - this folder holds a thin Helm chart used to manage the dev environment
* `prod` - this folder holds a thin Helm chart used to manage the prod environment
* `chart-repo` - this folder holds all packaged helm charts (the various versions of app-helm-chart, dev, and prod)
* `demo` - this folder holds scaffolding for this demo
