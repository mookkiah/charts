# OWASP Security Knowledge Framework

[SKF-FLASK](https://github.com/blabla1337/skf-flask) Security Knowledge Framework is an expert system application that uses the OWASP Application Security Verification Standard with detailed code examples (secure coding principles) to help developers in pre-development and post-development phases and create applications that are secure by design.

## Introduction
This chart will deploy a skf-flask application in kubernetes cluster.

## Prerequisites

-   Kubernetes 1.9+
-   Developed and Tested with Kubernetes 1.14+

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
$ helm install --name my-release incubator/skf-flask
```

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```bash
$ helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

## Configuration

The following table lists the configurable parameters of the kibana chart and their default values.

| Parameter                                  | Description                                                            | Default                               |
| ------------------------------------------ | ---------------------------------------------------------------------- | ------------------------------------- |
| `affinity`                                 | node/pod affinities                                                    | None                                  |
| `env`                                      | Environment variables to configure skf-flask                           | `{}`                                  |
| `dbVolumeClaim`                            | PVC for storing the sqlite database outside the pod                    | `nil`                                 |
| `image.pullPolicy`                         | Image pull policy                                                      | `IfNotPresent`                        |
| `image.repository`                         | Image repository                                                       | `blabla1337/skf-flask`                |
| `image.tag`                                | Image tag                                                              | `stable`                              |
| `image.pullSecrets`                        | Specify image pull secrets                                             | `nil`                                 |
| `replicaCount`                             | desired number of pods                                                 | `1`                                   |

