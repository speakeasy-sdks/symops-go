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
    res, err := s.GetEvent(ctx, operations.GetEventRequest{
        EventID: "corrupti",
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.Event != nil {
        // handle response
    }
}
```
<!-- End SDK Example Usage -->