# Introduction

This is a fork of [fast-gateway]() with added support for forwarding request headers for websocket connections.

## Usage

One additional option in the `WebSocketRoute`:

```ts
interface WebSocketRoute {
  proxyType: 'websocket';
  proxyConfig?: {}; 
  passRequestHeaders?: boolean; // <-- this one, defaults to false
  prefix: string;
  target: string;
  subProtocols?: [];
  hooks?: WebSocketHooks;
}
```

If `passRequestHeaders` is set to `true`, the request headers will be forwarded to the target server. This is useful for downstream authentication purposes.


## More
- fast-gateway's original website and documentation: https://fgw.21no.de
