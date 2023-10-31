## Introduction

This project provides a basic demonstration of Hasura's remote schema
capabilities.

Our interest here is primarily about distributed tracing between Hasura (which
[supports B3 headers](https://hasura.io/docs/latest/observability/tracing/) for
propagation) and New Relic (which
[supports W3C headers](https://docs.newrelic.com/docs/distributed-tracing/concepts/how-new-relic-distributed-tracing-works/)
for propagation).

## Getting started

### Set your Hasura license key

To run this demo, you'll need a legitimate `HASURA_GRAPHQL_PRO_KEY`.

First, create your `hasura.env` file with the following commands:

```shell
cd examples/hasura
cp env/hasura.env.example env/hasura.env
```

Then overwrite `HASURA_GRAPHQL_PRO_KEY` with the proper value.

### Start Hasura

```shell
cd examples/hasura
make start
make console
```
