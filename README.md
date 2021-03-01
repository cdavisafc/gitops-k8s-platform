# gitops-platform

This repo contains the declarative config for an eks-d cluster with the gitops
platform installed. The gitops platform, just as everything else in here is
gitops'd.

Instructions:
* Stand-up an eks-d clsuter using wksctl and the manifests in the eksd-cluster folder
* kubectl apply the base components of the gitops runtime:
  * gitops-runtime/flux/gotk-components.yaml
  * gitops-runtime/gitops-pipelines/gitops-pipelines-pipeline.yaml
  * gitops-runtime/gitops-pipelines/self-source.yaml
* add any other part of your k8s platform into this repo (in a new folder recommended) and include a gitops pipeline for it in the gitops-pipelines-pipeline.yaml
* make mods to any of the platform components by committing in here.
