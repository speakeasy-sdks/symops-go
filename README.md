<div align="center">
   <img src="https://user-images.githubusercontent.com/68016351/231297937-c9e20343-f037-4c65-96ac-06fb877fe121.png" width="200">
   <h1>Symops Go SDK</h1>
   <p>Secure your production infrastructure with code</p>
   <a href="https://github.com/speakeasy-sdks/symops-go/actions"><img src="https://img.shields.io/github/actions/workflow/status/speakeasy-sdks/symops-go/speakeasy_sdk_generation.yml?style=for-the-badge" /></a>
   <a href="https://docs.symops.com/reference"><img src="https://img.shields.io/static/v1?label=Docs&message=API Ref&color=000&style=for-the-badge" /></a>
</div>

<!-- Start SDK Installation -->
## SDK Installation

```bash
go get github.com/speakeasy-sdks/symops-go
```
<!-- End SDK Installation -->

## Authentication

To get access to the API and fetch an API key, please sign up for [access](https://docs.symops.com/docs). 

## SDK Example Usage
<!-- Start SDK Example Usage -->
```go
package main

import(
	"context"
	"log"
	"symops"
	"symops/pkg/models/operations"
)

func main() {
    s := symops.New()

    ctx := context.Background()    
    req := operations.GetEventRequest{
        EventID: "corrupti",
    }

    res, err := s.GetEvent(ctx, req)
    if err != nil {
        log.Fatal(err)
    }

    if res.Event != nil {
        // handle response
    }
}
```
<!-- End SDK Example Usage -->

<!-- Start SDK Available Operations -->
## Available Resources and Operations

### [Symops SDK](docs/symops/README.md)

* [GetEvent](docs/symops/README.md#getevent) - Retrieve an event by event ID
<!-- End SDK Available Operations -->

### Maturity

This SDK is in beta and therefore, we recommend pinning usage to a specific package version.
This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

### Contributions

While we value open-source contributions to this SDK, this library is generated and maintained programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release !

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
