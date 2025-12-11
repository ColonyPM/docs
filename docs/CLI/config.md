# Configuration File

CPM uses a YAML configuration file to store connection settings and credentials.

## Location

| Platform | Path |
|----------|------|
| Linux | `~/.config/cpm/config.yaml` |
| macOS | `~/.config/cpm/config.yaml` |
| Windows | `%APPDATA%\cpm\config.yaml` |

You can override the default location by setting the `XDG_CONFIG_HOME` environment variable.

## Setup

Create the config directory and file:

```bash
mkdir -p ~/.config/cpm
touch ~/.config/cpm/config.yaml
```

## Configuration Reference

```yaml
colonies:
  host: "localhost"        # Colonies server hostname
  port: 50080              # Colonies server port (1-65535)
  tls: false               # Enable TLS for server connection
  colony_name: "dev"       # Name of your colony
  colony_prvkey: "..."     # Colony private key (COLONIES_COLONY_PRVKEY)
  prvkey: "..."            # Your user private key (COLONIES_PRVKEY)

s3:
  endpoint: "localhost:9000"  # S3-compatible endpoint URL
  accesskey: "..."            # S3 access key
  secretkey: "..."            # S3 secret key
  region: ""                  # S3 region (can be empty for MinIO)
  bucket: "colonies-prod"     # S3 bucket name
  tls: false                  # Enable TLS for S3
  skip_verify: false          # Skip TLS certificate verification

minio:
  user: "admin"        # MinIO username
  password: "..."      # MinIO password
```

## Colonies Environment Variables

CPM uses a subset of the environment variables defined by [Colonies](https://github.com/colonyos/colonies). The table below shows which variables are used:

| Environment Variable | Config Field | Used |
|---------------------|--------------|------|
| `COLONIES_SERVER_HOST` | `colonies.host` | Yes |
| `COLONIES_SERVER_PORT` | `colonies.port` | Yes |
| `COLONIES_SERVER_TLS` | `colonies.tls` | Yes |
| `COLONIES_COLONY_NAME` | `colonies.colony_name` | Yes |
| `COLONIES_COLONY_PRVKEY` | `colonies.colony_prvkey` | Yes |
| `COLONIES_PRVKEY` | `colonies.prvkey` | Yes |
| `COLONIES_SERVER_ID` | - | No |
| `COLONIES_SERVER_PRVKEY` | - | No |
| `COLONIES_COLONY_ID` | - | No |
| `COLONIES_ID` | - | No |
| `COLONIES_EXECUTOR_TYPE` | - | No |
| `COLONIES_EXECUTOR_NAME` | - | No |
| `AWS_S3_ENDPOINT` | `s3.endpoint` | Yes |
| `AWS_S3_ACCESSKEY` | `s3.accesskey` | Yes |
| `AWS_S3_SECRETKEY` | `s3.secretkey` | Yes |
| `AWS_S3_REGION_KEY` | `s3.region` | Yes |
| `AWS_S3_BUCKET` | `s3.bucket` | Yes |
| `AWS_S3_TLS` | `s3.tls` | Yes |
| `AWS_S3_SKIPVERIFY` | `s3.skip_verify` | Yes |
| `MINIO_USER` | `minio.user` | Yes |
| `MINIO_PASSWORD` | `minio.password` | Yes |

Variables not used by CPM are either server-side configuration or handled internally.

## Required Fields

All fields in the configuration reference are required. If any field is missing, CPM will display an error:

```
missing required config: colonies.host
```

## Validation

CPM validates the configuration on startup:

- All required fields must be present
- `colonies.port` must be between 1 and 65535

## Example

A complete configuration for local development:

```yaml
colonies:
  host: "localhost"
  port: 50080
  tls: false
  colony_name: "dev"
  colony_prvkey: "ba949fa134981372d6da62b6a56f336ab4d843b22c02a4257dcf7d0d73097514"
  prvkey: "ddf7f7791208083b6a9ed975a72684f6406a269cfa36f1b1c32045c0a71fff05"

s3:
  endpoint: "localhost:9000"
  accesskey: "RrXN2vcLeHjBptG8a3Ay"
  secretkey: "ivwLB0Luqomq65nNVmoo8fTBgxXgNvqYGC50VQN6"
  region: ""
  bucket: "colonies-prod"
  tls: false
  skip_verify: false

minio:
  user: "admin"
  password: "admin12345"
```
