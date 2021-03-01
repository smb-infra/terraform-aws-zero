# user_auth

User management and Identity / Access Proxy using Ory Kratos and Oathkeeper 

## Notes
This module uses helm-charts to create a user authentication suite (Kratos, Oathkeeper, Oathkeeper-measter) in your Kubernetes cluster through your Kubernetes Provider, to provide user identity and authentication.

## Pre-requisites
### jwks_secret_name
This is a Private key stored in secret-manager used to sign tokens for user sessions, it is created in the Zero apply step during [`pre-k8s.sh`](https://github.com/commitdev/zero-aws-eks-stack/blob/main/templates/scripts/pre-k8s.sh#L22-L32)

### auth database / secret 
This is a database and connection-credentials created for Kratos, it is created in the Zero apply step during [`pre-k8s.sh`](https://github.com/commitdev/zero-aws-eks-stack/blob/main/templates/scripts/pre-k8s.sh#L22-L32)


<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

No requirements.

## Providers

| Name | Version |
|------|---------|
| aws | n/a |
| helm | n/a |
| kubernetes | n/a |
| null | n/a |
| template | n/a |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| auth\_namespace | Namespace to use for auth resources | `string` | `"user-auth"` | no |
| backend\_service\_domain | Domain of the backend service | `string` | n/a | yes |
| frontend\_service\_domain | Domain of the frontend | `string` | n/a | yes |
| jwks\_secret\_name | The name of a secret in the auth namespace containing a JWKS file for Oathkeeper | `string` | n/a | yes |
| k8s\_local\_exec\_context | Custom resource (Oathkeeper Rules are created using local-exec with kubectl), if not specified it will target your current context from kubeconfig | `string` | `""` | no |
| project | The name of the project | `any` | n/a | yes |
| user\_auth\_mail\_from\_address | Mail from the user management system will come from this address | `string` | `""` | no |
| whitelisted\_return\_urls | URLs for init flow to specify and 302 redirects upon flow completion | `list(string)` | `[]` | no |

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->