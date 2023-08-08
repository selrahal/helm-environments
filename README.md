# Helm environment demo

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
