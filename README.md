# Overview

The purpose of this resolver is to get the callers current public IP from <http://checkip.amazonaws.com/>.

## Install

```sh
pip install git+https://git@github.com/craighurley/sceptre-myip-resolver.git@1.0.0#egg=sceptre-myip-resolver
```

## Available Resolvers

### myip

Fetches the callers current public IP.

Syntax:

```yaml
parameter|sceptre_user_data:
    <name>: !myip
```

#### Example

Setup sceptre to retrieve the callers public IP:

```yaml
parameters:
    AllowedIp: !myip
```

Run sceptre and it will retrieve the callers public IP address and pass it to the CloudFormation _AllowedIp_ parameter.
