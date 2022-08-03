# OAuth 2.0

## Authorization Endpoint

TODO

## Token Endpoint

### Grant Type - Authorization Code

| Parameter | Required for confidential | Required for public | Value |
| - | - | - | - |
| `grant_type` | ✔️ | ✔️ | `authorization_code` |
| `code` | ✔️ | ✔️ | The code |
| `redirect_uri` | 🟠 | 🟠 | The redirect URI |
| `client_id` | ❌ (see [Authentication](#authentication)) | ✔️ | The client ID |

🟠 Only when also used on [Authorization Endpoint](authorization-endpoint).

#### Authentication 

| Parameter | Required for confidential | Required for public |
| - | - | - |
| `client_id` | ✔️ | ✔️ (to prevent client substitution) |
| `client_secret` | ✔️ | ❌ (never) |

### Grant Type - Password

| Parameter | Required for confidential | Required for public | Value |
| - | - | - | - |
| `grant_type` | ✔️ | ✔️ | `password` |
| `username` | ✔️ | ✔️ | The username |
| `password` | ✔️ | ✔️ | The password |
| `scope` | ❌ | ❌ | The scope |

#### Authentication 

| Parameter | Required for confidential | Required for public |
| - | - | - |
| `client_id` | ✔️ | ❌ |
| `client_secret` | ✔️ | ❌ (never) |

### Grant Type - Client Credentials

| Parameter | Required for confidential | Required for public | Value |
| - | - | - | - |
| `grant_type` | ✔️ | ✔️ | `client_credentials` |
| `scope` | ❌ | ❌ | The scope |

*Note: Always client authentication*

### Grant Type - Refresh Token

| Parameter | Required for confidential | Required for public | Value |
| - | - | - | - |
| `grant_type` | ✔️ | ✔️ | `refresh_token` |
| `scope` | ❌ | ❌ | The scope |

#### Authentication 

| Parameter | Required for confidential | Required for public |
| - | - | - |
| `client_id` | ✔️ | ❌ |
| `client_secret` | ✔️ | ❌ (never) |
