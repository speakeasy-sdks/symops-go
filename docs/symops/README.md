# Symops SDK

## Overview

This API allows you to retrieve events by event ID from Symops.

### Available Operations

* [GetEvent](#getevent) - Retrieve an event by event ID

## GetEvent

Retrieve an event by event ID

### Example Usage

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
        EventID: "provident",
    }

    res, err := s.Symops.GetEvent(ctx, req)
    if err != nil {
        log.Fatal(err)
    }

    if res.Event != nil {
        // handle response
    }
}
```
