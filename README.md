# Go Helm Client

fork of [mittwald/go-helm-client](https://github.com/mittwald/go-helm-client).

## Why use this fork ?
- fixes issue which caused helm charts to be applied to default
  namespace, even when a namespace has been specified in chart spec. 
  read more at [mittwald/go-helm-client#104](https://github.com/mittwald/go-helm-client/issues/104)
  reference [commit](https://github.com/nxtcoder17/go-helm-client/commit/c115afe06519c714315cd42702bc61ade4839f8b)


## Installation
Install this library using `go get`:

    $ go get github.com/nxtcoder17/go-helm-client@release


### from upstream [README.md](https://github.com/mittwald/go-helm-client)
Go client library for accessing [Helm](https://github.com/helm/helm), enabling the user to programmatically change helm charts and releases.

This library is build upon [`helm`](https://github.com/helm/helm) and available under the MIT License.
 
![Compile & Test](https://github.com/nxtcoder17/go-helm-client/workflows/Compile%20&%20Test/badge.svg)
[![GitHub license](https://img.shields.io/github/license/nxtcoder17/go-helm-client.svg)](https://github.com/nxtcoder17/go-helm-client/blob/master/LICENSE)
[![Go Report Card](https://goreportcard.com/badge/github.com/nxtcoder17/go-helm-client)](https://goreportcard.com/report/github.com/nxtcoder17/go-helm-client)
[![Documentation](https://godoc.org/github.com/nxtcoder17/go-helm-client?status.svg)](https://pkg.go.dev/github.com/nxtcoder17/go-helm-client)

## Usage
Example usage of the client can be found in the [package examples](https://pkg.go.dev/github.com/nxtcoder17/go-helm-client?tab=doc#pkg-examples).

#### Private chart repository
When working with private repositories, you can utilize the `Username` and `Password` parameters of a chart entry to specify credentials.

An example of this can be found in the corresponding [example](https://pkg.go.dev/github.com/nxtcoder17/go-helm-client?tab=doc#example_HelmClient_AddOrUpdateChartRepo_private).

## Mock Client
This library includes a mock client [mock/interface_mock.go](mock/interface.go) which is generated by [mockgen](https://github.com/golang/mock).

Example usage of the mocked client can be found in [mock/mock_test.go](mock/mock_test.go).

If you made changes to [interface.go](./interface.go), you should issue the `make generate` command to trigger code generation.

## Documentation
For more specific documentation, please refer to the [godoc](https://pkg.go.dev/github.com/nxtcoder17/go-helm-client/) of this library.
