# Go Substrate RPC Client (GSRPC)

[![License: Apache v2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![GoDoc Reference](https://godoc.org/github.com/centrifuge/go-substrate-rpc-client?status.svg)](https://godoc.org/github.com/centrifuge/go-substrate-rpc-client)
[![Build Status](https://travis-ci.com/centrifuge/go-substrate-rpc-client.svg?branch=master)](https://travis-ci.com/centrifuge/go-substrate-rpc-client)
[![codecov](https://codecov.io/gh/centrifuge/go-substrate-rpc-client/branch/master/graph/badge.svg)](https://codecov.io/gh/centrifuge/go-substrate-rpc-client)
[![Go Report Card](https://goreportcard.com/badge/github.com/centrifuge/go-substrate-rpc-client)](https://goreportcard.com/report/github.com/centrifuge/go-substrate-rpc-client)

Substrate RPC client in Go. It provides APIs and types around Polkadot and any Substrate-based chain RPC calls.
This client is modelled after [polkadot-js/api](https://github.com/polkadot-js/api).

## Fork Notes
To provide ECDSA signature decoding whilst retaining `github.com/ChainSafe/go-schnorrkel v0.0.0-20210318173838-ccb5cd955283` indirect dependency, use [tag 4.0.2](releases/tag/v4.0.2).

Add to your project's `go.mod`:

```go
replace github.com/centrifuge/go-substrate-rpc-client/v4 v4.0.0 => github.com/qredo/go-substrate-rpc-client/v4 v4.0.1
```
Run `go mod tidy` in your project's root.

## State

This package is feature complete, but it is relatively new and might still contain bugs. We advice to use it with caution in production. It comes without any warranties, please refer to LICENCE for details.

## Documentation & Usage Examples

Please refer to https://godoc.org/github.com/centrifuge/go-substrate-rpc-client

## Contributing

1. Install dependencies by running `make` followed by `make install`
1. Run tests `make test`
1. Lint `make lint` (you can use `make lint-fix` to automatically fix issues)

## Run tests in a Docker container against the Substrate Default Docker image

1. Run the docker container `make test-dockerized`

## Run tests locally against the Substrate Default Docker image

1. Start the Substrate Default Docker image: `make run-substrate-docker`
1. In another terminal, run the tests against that image: `make test`
1. Visit https://polkadot.js.org/apps for inspection

## Run tests locally against any substrate endpoint

1. Set the endpoint: `export RPC_URL="http://example.com:9933"`
1. Run the tests `make test`
