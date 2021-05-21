# Route53 Dynamic DNS Updater

This uses the [sjmayotte/route53-dynamic-dns](https://hub.docker.com/r/sjmayotte/route53-dynamic-dns)
Docker image and utility to maintain DNS records for my home's dynamic IP
address.

## Usage

Refer to the [upstream project](https://hub.docker.com/r/sjmayotte/route53-dynamic-dns)
for detailed usage documentation.

The container expects a `.env` file to be provided with environment variables.
I've provided [`.env.example`](.env.example) for a reference.
The utility relies on an AWS access key with minimal rights to the Route53
zone. These are maintained in the Terraform codebase that manages the
`jbeard.dev` AWS resources, including Route53.

Once a `.env` file is configured, simply start the service with
`docker-compose`:

```shell
docker-compose up
```
