# coralogix-operator

![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 0.1.0](https://img.shields.io/badge/AppVersion-0.1.0-informational?style=flat-square)

Coralogix Operator Helm Chart

**Homepage:** <https://github.com/coralogix/coralogix-operator>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| Coralogix | <platform@coralogix.com> |  |

## Source Code

* <https://github.com/coralogix/coralogix-operator>

## Requirements

Kubernetes: `>=1.16.0-0`

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` | ref: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/ |
| coralogixOperator | object | `{"image":{"repository":"coralogixrepo/coralogix-operator","tag":""},"region":"","resources":{},"securityContext":{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true}}` | Coralogix operator container config |
| coralogixOperator.image | object | `{"repository":"coralogixrepo/coralogix-operator","tag":""}` | Coralogix operator Image |
| coralogixOperator.region | string | `""` | Coralogix Account Region |
| coralogixOperator.resources | object | `{}` | resource config for Coralogix operator |
| coralogixOperator.securityContext | object | `{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true}` | Security context for Coralogix operator container |
| fullnameOverride | string | `""` | Provide a name to substitute for the full names of resources |
| imagePullSecrets | list | `[]` |  |
| kubeRbacProxy | object | `{"image":"gcr.io/kubebuilder/kube-rbac-proxy:v0.13.0","resources":{},"securityContext":{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true}}` | kube-rbac-proxy container config |
| kubeRbacProxy.image | string | `"gcr.io/kubebuilder/kube-rbac-proxy:v0.13.0"` | kube-rbac-proxy Image |
| kubeRbacProxy.resources | object | `{}` | resource config for kube-rbac-proxy |
| kubeRbacProxy.securityContext | object | `{"allowPrivilegeEscalation":false,"capabilities":{"drop":["ALL"]},"readOnlyRootFilesystem":true}` | Security context for kube-rbac-proxy container |
| nameOverride | string | `""` | Provide a name in place of kube-prometheus-stack for `app:` labels |
| nodeSelector | object | `{}` | ref: https://kubernetes.io/docs/user-guide/node-selection/ |
| podAnnotations | object | `{}` | Annotations to add to the operator pod |
| secret | object | `{"annotations":{},"create":true,"data":{"apiKey":""},"labels":{},"secretKeyReference":{}}` | Configuration for Coralogix operator secret |
| secret.annotations | object | `{}` | Annotations to add to the Coralogix operator secret |
| secret.create | bool | `true` | Indicates if the Coralogix operator secret should be created |
| secret.data | object | `{"apiKey":""}` | Coralogix operator secret data |
| secret.labels | object | `{}` | Labels to add to the Coralogix operator secret |
| secret.secretKeyReference | object | `{}` | secret.data and secret.secretKeyReference should be mutually exclusive. |
| securityContext | object | `{"fsGroup":2000,"runAsGroup":2000,"runAsNonRoot":true,"runAsUser":2000,"seccompProfile":{"type":"RuntimeDefault"}}` | ref: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/ |
| serviceAccount | object | `{"annotations":{},"create":true,"name":""}` | ref: https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/ |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.create | bool | `true` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | If not set and create is true, a name is generated using the fullname template |
| tolerations | list | `[]` | ref: https://kubernetes.io/docs/concepts/configuration/taint-and-toleration/ |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)