# SLcodec Senlab encoding/decoding javascript

Public code

## Requirement

* Javascript ES5 or Javascript ES6

## How to use (General)

1. 


2. 


## How to use (specific TTN version 3)

1. Add this few lines on top of the "payload formatter (Javascript)" page

```
function decodeUplink(input) {
    time_now = new Date().getTime(); // time of the payload
    message = {
        FPort: input.fPort,
        payload: toHexString(input.bytes),
        time: time_now
    }
    return {
        "data": {
            time_payload: time_now,
            decoded: decode(message)
        }
    }
}function
```
2. Copy/paste all functions bellow (in the same windows)
3. "Save changes"
4. Test the decoder:
   (SenlabT) Byte payload `014E326400BB0200` FPort `3`
   (SenlabH) Byte payload `03850C3C015C2F002F002F002F002F002F002F032F002F002F` FPort `3`
   (SenlabM) Byte payload `02D869822C0000000F0500` FPort `3`
