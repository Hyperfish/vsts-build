# VSTS build agent Helm chart for Kubernetes

A [helm](https://helm.sh/) chart for the [VSTS](https://visualstudio.microsoft.com/team-services/) linux build agent. 

## Pre-reqs:

* a working kubernetes cluster
* a VSTS account & a personal access token for your account
* kubectl and helm installed

## Install

Clone this repo:
`git clone git@github.com:Hyperfish/vsts-build.git`

Open up the values.yaml file and update the following properties:

* VSTS_ACCOUNT – this is the name of your VSTS account e.g. “contoso”.
* VSTS_POOL – this is the name of the agent pool you would like your agents registered in.
* VSTS_TOKEN – this is your personal access token from VSTS that has been given at least the Agent Pools (read, manage) scope.
* replicaCount – set this to how many agents you want deployed.

Install:
`helm install .`

Check your VSTS build pool that you specified in the values.yaml file. You should see your new agents listed.
