# localgateway-api

Rust crate `localgateway-api`: the LocalGateway management API client, generated
from the LocalGateway OpenAPI contract with openapi-generator 7.26.0.

The generated sources under `src/` must not be edited by hand; runtime
adaptations live in the separate `localgateway-sdk` crate, which depends on this
crate.

## Repository layout

This repository root is the crate root: `Cargo.toml` and `src/` live at the top
level, with no nested workspace or crate directory. Generated API documentation
lives under `docs/`; openapi-generator bookkeeping lives in
`.openapi-generator/`. Current version: `0.2.1`.

## Usage

```toml
[dependencies]
localgateway-api = { git = "https://github.com/HuanyuMark/localgateway-api", tag = "v0.2.1", default-features = false }
```

TLS is disabled by default because the client only talks to the loopback
gateway; enable the `native-tls` or `rustls` feature when needed.

## Dependencies

`localgateway-api` is the base crate of the Rust SDK. `localgateway-sdk` depends
on it, and `localgateway-provider` depends on `localgateway-sdk`. Both consumers
reference this crate through GitHub git + tag `v0.2.1`.

## Documentation

- Endpoints: [`docs/GatewayApi.md`](docs/GatewayApi.md),
  [`docs/ServicesApi.md`](docs/ServicesApi.md)
- Models: files under [`docs/`](docs/)
