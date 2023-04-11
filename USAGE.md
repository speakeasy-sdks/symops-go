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
    s := sdk.New()

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