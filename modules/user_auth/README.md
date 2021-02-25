# user_auth

User management and Identity / Access Proxy using Ory Kratos and Oathkeeper 

## Notes

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
| auth\_domain | Domain to use for authentication | `string` | n/a | yes |
| auth\_namespace | Namespace to use for auth resources | `string` | `"user-auth"` | no |
| backend\_service\_domain | Domain of the backend service | `string` | n/a | yes |
| frontend\_service\_domain | Domain of the frontend | `string` | n/a | yes |
| jwks\_secret\_name | jwks\_secret\_name | `string` | n/a | yes |
| k8s\_local\_exec\_context | Custom resource (Oathkeeper Rules are created using local-exec with kubectl), if not specified it will target your current context from kubeconfig | `string` | `""` | no |
| project | The name of the project | `any` | n/a | yes |
| user\_auth\_mail\_from\_address | Mail from the user management system will come from this address | `string` | `""` | no |

## Outputs

No output.

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
