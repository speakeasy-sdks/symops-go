# symops

<!-- Start SDK Installation -->
## SDK Installation

```bash
go get github.com/speakeasy-sdks/symops-go
```
<!-- End SDK Installation -->

## SDK Example Usage
<!-- Start SDK Example Usage -->
```go
package main

import (
    "context"
    "log"
    "symops"
    "symops/pkg/models/shared"
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

### Symops SDK

* `GetEvent` - Retrieve an event by event ID
<!-- End SDK Available Operations -->

### Maturity

This SDK is in beta and therefore, we recommend pinning usage to a specific package version.
This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

### Contributions

While we value open-source contributions to this SDK, this library is generated and maintained programmatically.
Feel free to open a PR or a Github issue as a proof of concept and we'll do our best to include it in a future release !

### SDK Created by [Speakeasy](https://docs.speakeasyapi.dev/docs/using-speakeasy/client-sdks)
