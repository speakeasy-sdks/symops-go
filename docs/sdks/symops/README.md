# Symops SDK

## Overview

Symops API: This API allows you to retrieve events by event ID from Symops.

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
    res, err := s.Symops.GetEvent(ctx, operations.GetEventRequest{
        EventID: "provident",
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.Event != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                                                | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `ctx`                                                                    | [context.Context](https://pkg.go.dev/context#Context)                    | :heavy_check_mark:                                                       | The context to use for the request.                                      |
| `request`                                                                | [operations.GetEventRequest](../../models/operations/geteventrequest.md) | :heavy_check_mark:                                                       | The request object to use for the request.                               |


### Response

**[*operations.GetEventResponse](../../models/operations/geteventresponse.md), error**

